---
title: PowerShell işlerini kullanarak cmdlet’leri paralel olarak çalıştırma
description: -AsJob parametresini kullanarak cmdlet’leri paralel olarak çalıştırma yönergeleri.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 825a07e01194a07b747712a62384c7f162e63d7d
ms.sourcegitcommit: a4e527d3deba004007cfa22fa536e8255dd23b37
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67516496"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="44f90-103">PowerShell işlerini kullanarak cmdlet’leri paralel olarak çalıştırma</span><span class="sxs-lookup"><span data-stu-id="44f90-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="44f90-104">PowerShell, [PowerShell İşleri](/powershell/module/microsoft.powershell.core/about/about_jobs) ile zaman uyumsuz eylemi destekler.</span><span class="sxs-lookup"><span data-stu-id="44f90-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="44f90-105">Azure PowerShell, Azure’a ağ çağrıları yapma ve bunlar için bekleme açısından yüksek bir bağımlılığa sahiptir.</span><span class="sxs-lookup"><span data-stu-id="44f90-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="44f90-106">Sık sık engelleyici olmayan çağrılar yapmanız gerektiğini fark edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44f90-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="44f90-107">Bu gereksinimi karşılamak için Azure PowerShell birinci sınıf [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) desteği sağlar.</span><span class="sxs-lookup"><span data-stu-id="44f90-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="44f90-108">Bağlam Kalıcılığı ve PSJob’lar</span><span class="sxs-lookup"><span data-stu-id="44f90-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="44f90-109">PSJob'lar ayrı işlemler olarak çalıştığından, Azure bağlantınızın onlarla paylaşılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="44f90-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="44f90-110">`Connect-AzAccount` ile Azure hesabınızda oturum açtıktan sonra, bağlamı bir işe geçirin.</span><span class="sxs-lookup"><span data-stu-id="44f90-110">After signing in to your Azure account with `Connect-AzAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList (Get-AzContext),$creds
```

<span data-ttu-id="44f90-111">Bununla birlikte, bağlamınızın `Enable-AzContextAutosave` ile otomatik olarak kaydedilmesini tercih ettiyseniz bağlam otomatik olarak tüm oluşturduğunuz işlerle paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="44f90-111">However, if you have chosen to have your context automatically saved with `Enable-AzContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin} -ArgumentList $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="44f90-112">`-AsJob` ile Otomatik İşler</span><span class="sxs-lookup"><span data-stu-id="44f90-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="44f90-113">Azure PowerShell, uzun süre çalışan bazı cmdlet’lerde kolaylık olarak bir `-AsJob` anahtarı da sağlar.</span><span class="sxs-lookup"><span data-stu-id="44f90-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="44f90-114">`-AsJob` anahtarı, PSJob oluşturmayı daha da kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="44f90-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="44f90-115">Dilediğiniz zaman `Get-Job` ve `Get-AzVM` ile işi ve ilerleme durumunu inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44f90-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzVM`.</span></span>

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

<span data-ttu-id="44f90-116">İş tamamlandığında, `Receive-Job` ile işin sonucunu alın.</span><span class="sxs-lookup"><span data-stu-id="44f90-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="44f90-117">`Receive-Job`, `-AsJob` bayrağı yokmuş gibi cmdlet’ten sonucu döndürür.</span><span class="sxs-lookup"><span data-stu-id="44f90-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="44f90-118">Örneğin, `Do-Action -AsJob` cmdlet’inin `Receive-Job` sonucu `Do-Action` sonucuyla aynı türdedir.</span><span class="sxs-lookup"><span data-stu-id="44f90-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

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

## <a name="example-scenarios"></a><span data-ttu-id="44f90-119">Örnek Senaryolar</span><span class="sxs-lookup"><span data-stu-id="44f90-119">Example Scenarios</span></span>

<span data-ttu-id="44f90-120">Bir kerede birkaç VM oluşturun:</span><span class="sxs-lookup"><span data-stu-id="44f90-120">Create several VMs at once:</span></span>

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

<span data-ttu-id="44f90-121">Bu örnekte, `Wait-Job` cmdlet’i işler çalıştırılırken betiğin duraklatılmasına yol açar.</span><span class="sxs-lookup"><span data-stu-id="44f90-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="44f90-122">Tüm işler tamamladıktan sonra betik yürütülmeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="44f90-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="44f90-123">Birkaç iş paralel çalıştırılır, sonra betik devam etmeden önce tamamlanmasını bekler.</span><span class="sxs-lookup"><span data-stu-id="44f90-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

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