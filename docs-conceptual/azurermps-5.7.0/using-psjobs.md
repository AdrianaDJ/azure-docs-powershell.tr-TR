---
title: PowerShell işlerini kullanarak cmdlet’leri paralel olarak çalıştırma
description: -AsJob parametresini kullanarak cmdlet’leri paralel olarak çalıştırma yönergeleri.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: d2ffd6cc4c5e70c53ab60b1280384faac9b45867
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534720"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a>PowerShell işlerini kullanarak cmdlet’leri paralel olarak çalıştırma

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

PowerShell, [PowerShell İşleri](/powershell/module/microsoft.powershell.core/about/about_jobs) ile zaman uyumsuz eylemi destekler.
Azure PowerShell, Azure’a ağ çağrıları yapma ve bunlar için bekleme açısından yüksek bir bağımlılığa sahiptir. Bir geliştirici olarak sıklıkla bir betikte Azure’a birden çok engellemeyen çağrı yapmak istediğinizi veya REPL’de geçerli oturumu engellemeden Azure kaynakları oluşturmak istediğinizi fark edebilirsiniz. Azure PowerShell, bu gereksinimleri karşılamak için birinci sınıf [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) desteği sağlar.

## <a name="context-persistence-and-psjobs"></a>Bağlam Kalıcılığı ve PSJob’lar

PSJob’lar ayrı işlemlerde çalıştırılır ve bu da Azure bağlantınız hakkındaki bilgilerin oluşturduğunuz işlerle düzgün bir şekilde paylaşılması gerektiği anlamına gelir. `Connect-AzureRmAccount` ile Azure hesabınızı PowerShell oturumunuza bağladıktan sonra bağlamı bir işe geçirebilirsiniz.

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

Daha sonra, iş tamamlandığında `Receive-Job` ile işin sonucunu edinebilirsiniz.

> [!NOTE]
> `Receive-Job`, `-AsJob` bayrağı yokmuş gibi cmdlet’ten sonucu döndürür.
> Örneğin, `Receive-Job` cmdlet’inin `Do-Action -AsJob` sonucu `Do-Action` sonucuyla aynı türdedir.

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

Aynı anda birden çok VM oluşturun.

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

Bu örnekte, `Wait-Job` cmdlet’i işler çalıştırılırken betiğin duraklatılmasına yol açar. Tüm işler tamamladıktan sonra betik yürütülmeye devam eder. Bu, paralel olarak çalışan birden çok iş oluşturmanıza ve devam etmeden önce bunların tamamlanmasını beklemenize imkan tanır.

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
