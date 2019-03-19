---
title: PowerShell işlerini kullanarak cmdlet’leri paralel olarak çalıştırma
description: -AsJob parametresini kullanarak cmdlet’leri paralel olarak çalıştırma yönergeleri.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 65d3a1d206d7318173a87a4e53c579155a85426c
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882638"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a>PowerShell işlerini kullanarak cmdlet’leri paralel olarak çalıştırma

PowerShell, [PowerShell İşleri](/powershell/module/microsoft.powershell.core/about/about_jobs) ile zaman uyumsuz eylemi destekler.
Azure PowerShell, Azure’a ağ çağrıları yapma ve bunlar için bekleme açısından yüksek bir bağımlılığa sahiptir. Sık sık engelleyici olmayan çağrılar yapmanız gerektiğini fark edebilirsiniz. Bu gereksinimi karşılamak için Azure PowerShell birinci sınıf [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) desteği sağlar.

## <a name="context-persistence-and-psjobs"></a>Bağlam Kalıcılığı ve PSJob’lar

PSJob'lar ayrı işlemler olarak çalıştığından, Azure bağlantınızın onlarla paylaşılması gerekir. `Connect-AzAccount` ile Azure hesabınızda oturum açtıktan sonra, bağlamı bir işe geçirin.

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzContext),$creds
```

Bununla birlikte, bağlamınızın `Enable-AzContextAutosave` ile otomatik olarak kaydedilmesini tercih ettiyseniz bağlam otomatik olarak tüm oluşturduğunuz işlerle paylaşılır.

```azurepowershell-interactive
Enable-AzContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a>`-AsJob` ile Otomatik İşler

Azure PowerShell, uzun süre çalışan bazı cmdlet’lerde kolaylık olarak bir `-AsJob` anahtarı da sağlar.
`-AsJob` anahtarı, PSJob oluşturmayı daha da kolaylaştırır.

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzVM -Name MyVm -Credential $creds -AsJob
```

Dilediğiniz zaman `Get-Job` ve `Get-AzVM` ile işi ve ilerleme durumunu inceleyebilirsiniz.

```azurepowershell-interactive
Get-Job $job
Get-AzVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzVM' AzureLongRunningJob`1 Running True        localhost New-AzVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

İş tamamlandığında, `Receive-Job` ile işin sonucunu alın.

> [!NOTE]
> `Receive-Job`, `-AsJob` bayrağı yokmuş gibi cmdlet’ten sonucu döndürür.
> Örneğin, `Do-Action -AsJob` cmdlet’inin `Receive-Job` sonucu `Do-Action` sonucuyla aynı türdedir.

```azurepowershell-interactive
$vm = Receive-Job $job
$vm
```

```output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a>Örnek Senaryolar

Bir kerede birkaç VM oluşturun:

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzVM
```

Bu örnekte, `Wait-Job` cmdlet’i işler çalıştırılırken betiğin duraklatılmasına yol açar. Tüm işler tamamladıktan sonra betik yürütülmeye devam eder. Birkaç iş paralel çalıştırılır, sonra betik devam etmeden önce tamamlanmasını bekler.

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```