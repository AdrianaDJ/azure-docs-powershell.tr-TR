---
title: PowerShell işlerini kullanarak cmdlet’leri paralel olarak çalıştırma
description: -AsJob parametresini kullanarak cmdlet’leri paralel olarak çalıştırma yönergeleri.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: c411c097202366e8141b47fcbf764884a0e6e034
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820808"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="64b6b-103">PowerShell işlerini kullanarak cmdlet’leri paralel olarak çalıştırma</span><span class="sxs-lookup"><span data-stu-id="64b6b-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="64b6b-104">PowerShell, [PowerShell İşleri](/powershell/module/microsoft.powershell.core/about/about_jobs) ile zaman uyumsuz eylemi destekler.</span><span class="sxs-lookup"><span data-stu-id="64b6b-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="64b6b-105">Azure PowerShell, Azure’a ağ çağrıları yapma ve bunlar için bekleme açısından yüksek bir bağımlılığa sahiptir.</span><span class="sxs-lookup"><span data-stu-id="64b6b-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="64b6b-106">Bir geliştirici olarak sıklıkla bir betikte Azure’a birden çok engellemeyen çağrı yapmak istediğinizi veya REPL’de geçerli oturumu engellemeden Azure kaynakları oluşturmak istediğinizi fark edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64b6b-106">As a developer, you may often find yourself looking to make multiple non-blocking calls to Azure in a script, or you may find that you want to create Azure resources in the REPL without blocking the current session.</span></span> <span data-ttu-id="64b6b-107">Azure PowerShell, bu gereksinimleri karşılamak için birinci sınıf [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) desteği sağlar.</span><span class="sxs-lookup"><span data-stu-id="64b6b-107">To address these needs, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="64b6b-108">Bağlam Kalıcılığı ve PSJob’lar</span><span class="sxs-lookup"><span data-stu-id="64b6b-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="64b6b-109">PSJob’lar ayrı işlemlerde çalıştırılır ve bu da Azure bağlantınız hakkındaki bilgilerin oluşturduğunuz işlerle düzgün bir şekilde paylaşılması gerektiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="64b6b-109">PSJobs are run in separate processes, which means that information about your Azure connection must be properly shared with the jobs you create.</span></span> <span data-ttu-id="64b6b-110">`Connect-AzureRmAccount` ile Azure hesabınızı PowerShell oturumunuza bağladıktan sonra bağlamı bir işe geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64b6b-110">Upon connecting your Azure account to your PowerShell session with `Connect-AzureRmAccount`, you can pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="64b6b-111">Bununla birlikte, bağlamınızın `Enable-AzureRmContextAutosave` ile otomatik olarak kaydedilmesini tercih ettiyseniz bağlam otomatik olarak tüm oluşturduğunuz işlerle paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="64b6b-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="64b6b-112">`-AsJob` ile Otomatik İşler</span><span class="sxs-lookup"><span data-stu-id="64b6b-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="64b6b-113">Azure PowerShell, uzun süre çalışan bazı cmdlet’lerde kolaylık olarak bir `-AsJob` anahtarı da sağlar.</span><span class="sxs-lookup"><span data-stu-id="64b6b-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="64b6b-114">`-AsJob` anahtarı, PSJob oluşturmayı daha da kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="64b6b-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="64b6b-115">Dilediğiniz zaman `Get-Job` ve `Get-AzureRmVM` ile işi ve ilerleme durumunu inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64b6b-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

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

<span data-ttu-id="64b6b-116">Daha sonra, iş tamamlandığında `Receive-Job` ile işin sonucunu edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64b6b-116">Subsequently, upon completion, you can obtain the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="64b6b-117">`Receive-Job`, `-AsJob` bayrağı yokmuş gibi cmdlet’ten sonucu döndürür.</span><span class="sxs-lookup"><span data-stu-id="64b6b-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="64b6b-118">Örneğin, `Do-Action -AsJob` cmdlet’inin `Receive-Job` sonucu `Do-Action` sonucuyla aynı türdedir.</span><span class="sxs-lookup"><span data-stu-id="64b6b-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

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

## <a name="example-scenarios"></a><span data-ttu-id="64b6b-119">Örnek Senaryolar</span><span class="sxs-lookup"><span data-stu-id="64b6b-119">Example Scenarios</span></span>

<span data-ttu-id="64b6b-120">Aynı anda birden çok VM oluşturun.</span><span class="sxs-lookup"><span data-stu-id="64b6b-120">Create multiple VMs at once.</span></span>

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

<span data-ttu-id="64b6b-121">Bu örnekte, `Wait-Job` cmdlet’i işler çalıştırılırken betiğin duraklatılmasına yol açar.</span><span class="sxs-lookup"><span data-stu-id="64b6b-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="64b6b-122">Tüm işler tamamladıktan sonra betik yürütülmeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="64b6b-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="64b6b-123">Bu, paralel olarak çalışan birden çok iş oluşturmanıza ve devam etmeden önce bunların tamamlanmasını beklemenize imkan tanır.</span><span class="sxs-lookup"><span data-stu-id="64b6b-123">This allows you to create several jobs running in parallel then wait for completion before continuing.</span></span>

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
