---
title: PowerShell işlerini kullanarak cmdlet’leri paralel olarak çalıştırma
description: -AsJob parametresini kullanarak cmdlet’leri paralel olarak çalıştırma yönergeleri.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 8a05d8ff8344870e2daac130135b921b192f0f5d
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241347"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a>PowerShell işlerini kullanarak cmdlet’leri paralel olarak çalıştırma

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

PowerShell, [PowerShell İşleri](/powershell/module/microsoft.powershell.core/about/about_jobs) ile zaman uyumsuz eylemi destekler.
Azure PowerShell, Azure’a ağ çağrıları yapma ve bunlar için bekleme açısından yüksek bir bağımlılığa sahiptir. Sık sık engelleyici olmayan çağrılar yapmanız gerektiğini fark edebilirsiniz. Bu gereksinimi karşılamak için Azure PowerShell birinci sınıf [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) desteği sağlar.

## <a name="context-persistence-and-psjobs"></a>Bağlam Kalıcılığı ve PSJob’lar

PSJob'lar ayrı işlemler olarak çalıştığından, Azure bağlantınızın onlarla paylaşılması gerekir. `Connect-AzureRmAccount` ile Azure hesabınızda oturum açtıktan sonra, bağlamı bir işe geçirin.

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

Bununla birlikte, bağlamınızın `Enable-AzureRmContextAutosave` ile otomatik olarak kaydedilmesini tercih ettiyseniz bağlam otomatik olarak tüm oluşturduğunuz işlerle paylaşılır.

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a>`-AsJob` ile Otomatik İşler

Azure PowerShell, uzun süre çalışan bazı cmdlet’lerde kolaylık olarak bir `-AsJob` anahtarı da sağlar.
`-AsJob` anahtarı, PSJob oluşturmayı daha da kolaylaştırır.

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

Dilediğiniz zaman `Get-Job` ve `Get-AzureRmVM` ile işi ve ilerleme durumunu inceleyebilirsiniz.

```azurepowershell-interactive
Get-Job $job
Get-AzureRmVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

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
    New-AzureRmVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzureRmVM
```

Bu örnekte, `Wait-Job` cmdlet’i işler çalıştırılırken betiğin duraklatılmasına yol açar. Tüm işler tamamladıktan sonra betik yürütülmeye devam eder. Birkaç iş paralel çalıştırılır, sonra betik devam etmeden önce tamamlanmasını bekler.

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
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
