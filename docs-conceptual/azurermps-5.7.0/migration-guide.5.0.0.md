---
title: Microsoft Azure PowerShell 5.0.0 için bozucu değişiklikler
description: Bu geçiş kılavuzu, Azure PowerShell sürüm 5 yayınında yapılan ve hataya neden olan değişikliklerin listesini içerir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: f8dc413a91876e53e62d25cc38ac3b3ef6afda8e
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2019
ms.locfileid: "65534585"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="0529c-103">Microsoft Azure PowerShell 5.0.0 için bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-103">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="0529c-104">Bu belge, Microsoft Azure PowerShell cmdlet’lerini kullananlar için hem bozucu değişiklik bildirimi hem de geçiş kılavuzu olarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="0529c-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="0529c-105">Her bölümde hem bozucu değişikliğin yapılma nedeni hem de en kolay geçiş yolu açıklanır.</span><span class="sxs-lookup"><span data-stu-id="0529c-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="0529c-106">Bağlamla ilgili daha ayrıntılı bilgi edinmek için lütfen her bir değişiklikle ilişkili çekme isteğine başvurun.</span><span class="sxs-lookup"><span data-stu-id="0529c-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="0529c-107">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="0529c-107">Table of Contents</span></span>

- [<span data-ttu-id="0529c-108">ApiManagement cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-108">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="0529c-109">Batch cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-109">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="0529c-110">İşlem cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-110">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="0529c-111">EventHub cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-111">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="0529c-112">Insights cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-112">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="0529c-113">Ağ cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-113">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="0529c-114">Kaynaklar cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-114">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="0529c-115">ServiceBus Cmdlet’lerinde Bozucu Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-115">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="0529c-116">ApiManagement cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-116">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="0529c-117">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="0529c-117">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="0529c-118">"UserName" ve "Password" parametreleri bir PSCredential ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-118">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="0529c-119">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="0529c-119">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="0529c-120">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="0529c-121">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="0529c-121">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="0529c-122">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-122">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="0529c-123">Batch cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-123">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="0529c-124">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="0529c-124">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="0529c-125">`Password` parametresi bir Secure dizesi ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="0529c-126">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="0529c-126">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="0529c-127">`Password` parametresi bir Secure dizesi ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="0529c-128">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="0529c-128">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="0529c-129">`Password` parametresi bir Secure dizesi ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-129">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="0529c-130">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="0529c-130">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="0529c-131">`RunElevated` anahtarı kaldırılıp `UserIdentity` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0529c-131">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="0529c-132">Bundan `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` ve `PSJobReleaseTask` üzerindeki `RunElevated` özelliği de etkilenir.</span><span class="sxs-lookup"><span data-stu-id="0529c-132">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="0529c-133">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="0529c-133">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="0529c-134">`PSMultiInstanceSettings` oluşturucusu artık gerekli bir `numberOfInstances` parametresi almak yerine gerekli bir `coordinationCommandLine` parametresi alır.</span><span class="sxs-lookup"><span data-stu-id="0529c-134">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="0529c-135">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="0529c-135">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="0529c-136">`PSCloudTask` üzerinde `RunElevated` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-136">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="0529c-137">`RunElevated` yerine `UserIdentity` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0529c-137">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="0529c-138">Bundan `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` ve `PSJobReleaseTask` üzerindeki `RunElevated` özelliği de etkilenir.</span><span class="sxs-lookup"><span data-stu-id="0529c-138">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="0529c-139">**Birden çok tür**</span><span class="sxs-lookup"><span data-stu-id="0529c-139">**Multiple types**</span></span>

- <span data-ttu-id="0529c-140">`PSExitConditions` üzerinde `SchedulingError` özelliği `PreProcessingError` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-140">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="0529c-141">**Birden çok tür**</span><span class="sxs-lookup"><span data-stu-id="0529c-141">**Multiple types**</span></span>

- <span data-ttu-id="0529c-142">`PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` ve `PSTaskExecutionInformation` üzerinde `SchedulingError` özelliği `FailureInformation` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-142">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="0529c-143">Her görev hatası için `FailureInformation` döndürülür.</span><span class="sxs-lookup"><span data-stu-id="0529c-143">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="0529c-144">Buna, önceki tüm zamanlama hata durumlarının yanı sıra yeni çıktı dosyaları özelliğinden sıfır olmayan görev çıkış kodları ve karşıya dosya yükleme hataları dahildir.</span><span class="sxs-lookup"><span data-stu-id="0529c-144">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="0529c-145">Bu türün yapısı aynı kaldığından, türü kullanırken kod değişikliği yapmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="0529c-145">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="0529c-146">Ayrıca şunlar da etkilenir: Get-AzureBatchPool, Get-AzureBatchSubtask ve Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="0529c-146">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="0529c-147">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="0529c-147">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="0529c-148">`TargetDedicated` kaldırılıp `TargetDedicatedComputeNodes` ve `TargetLowPriorityComputeNodes` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0529c-148">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="0529c-149">`TargetDedicatedComputeNodes` öğesinin `TargetDedicated` şeklinde bir diğer adı vardır.</span><span class="sxs-lookup"><span data-stu-id="0529c-149">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="0529c-150">Ayrıca şu da etkilenir: Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="0529c-150">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="0529c-151">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="0529c-151">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="0529c-152">`PSCloudPool` üzerinde `TargetDedicated` ve `CurrentDedicated` özellikleri `TargetDedicatedComputeNodes` ve `CurrentDedicatedComputeNodes` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-152">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="0529c-153">**Type PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="0529c-153">**Type PSCloudPool**</span></span>

- <span data-ttu-id="0529c-154">`PSCloudPool` üzerinde `ResizeError` ve `ResizeErrors` yeniden adlandırıldı ve artık bir koleksiyon.</span><span class="sxs-lookup"><span data-stu-id="0529c-154">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="0529c-155">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="0529c-155">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="0529c-156">`PSPoolSpecification` üzerinde `TargetDedicated` özelliği `TargetDedicatedComputeNodes` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-156">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="0529c-157">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="0529c-157">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="0529c-158">`Name` kaldırılıp `Path` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0529c-158">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="0529c-159">`Path` öğesinin `Name` şeklinde bir diğer adı vardır.</span><span class="sxs-lookup"><span data-stu-id="0529c-159">`Path` has an alias `Name`.</span></span>

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="0529c-160">Ayrıca şunlar da etkilenir: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="0529c-160">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="0529c-161">**PSNodeFile** Türü</span><span class="sxs-lookup"><span data-stu-id="0529c-161">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="0529c-162">`PSNodeFile` üzerinde `Name` özelliği `Path` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-162">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="0529c-163">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="0529c-163">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="0529c-164">`PSSubtaskInformation` öğesinin `PreviousState` ve `State` özellikleri artık `TaskState` türünde değil, `SubtaskState` türündedir.</span><span class="sxs-lookup"><span data-stu-id="0529c-164">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="0529c-165">Alt görevlerin `Active` durumunda olması mümkün olmadığından, `SubtaskState` öğesinin `TaskState` öğesinden farklı olarak `Active` değeri yoktur.</span><span class="sxs-lookup"><span data-stu-id="0529c-165">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="0529c-166">İşlem cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-166">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="0529c-167">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="0529c-167">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="0529c-168">"UserName" ve "Password" parametreleri bir PSCredential ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-168">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="0529c-169">EventHub cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-169">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="0529c-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-171">'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-171">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-172">Lütfen 'New-AzureRmEventHubAuthorizationRule' cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="0529c-172">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="0529c-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-174">'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-174">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-175">Lütfen 'Get-AzureRmEventHubAuthorizationRule' cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="0529c-175">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="0529c-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-177">'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-177">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-178">Lütfen 'Set-AzureRmEventHubAuthorizationRule' cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="0529c-178">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="0529c-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-180">'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-180">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-181">Lütfen 'Remove-AzureRmEventHubAuthorizationRule' cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="0529c-181">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="0529c-182">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="0529c-182">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="0529c-183">'New-AzureRmEventHubNamespaceKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-183">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-184">Lütfen 'New-AzureRmEventHubKey' cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="0529c-184">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="0529c-185">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="0529c-185">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="0529c-186">'Get-AzureRmEventHubNamespaceKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-186">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-187">Lütfen 'Get-AzureRmEventHubKey' cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="0529c-187">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="0529c-188">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="0529c-188">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="0529c-189">NamespceAttributes’tan 'Status' ve 'Enabled' özelliği kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="0529c-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="0529c-190">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="0529c-190">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="0529c-191">NamespceAttributes’tan 'Status' ve 'Enabled' özelliği kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="0529c-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="0529c-192">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="0529c-192">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="0529c-193">NamespceAttributes’tan 'Status' ve 'Enabled' özelliği kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="0529c-193">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="0529c-194">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="0529c-194">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="0529c-195">ConsumerGroupAttributes’tan 'EventHubPath' özelliği kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="0529c-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="0529c-196">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="0529c-196">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="0529c-197">ConsumerGroupAttributes’tan 'EventHubPath' özelliği kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="0529c-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="0529c-198">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="0529c-198">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="0529c-199">ConsumerGroupAttributes’tan 'EventHubPath' özelliği kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="0529c-199">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="0529c-200">Insights cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-200">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="0529c-201">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-201">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="0529c-202">**Add-AzureRMLogAlertRule** cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="0529c-202">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="0529c-203">Bu işlevsellik Etkinlik Günlüğü Uyarılarına geçirildiğinden, 1 Ekim’den sonra bu cmdlet’in kullanılmasının herhangi bir etkisi olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="0529c-203">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="0529c-204">Daha fazla bilgi için lütfen bkz. https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="0529c-204">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="0529c-205">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="0529c-205">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="0529c-206">**Get-AzureRMUsage** cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="0529c-206">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="0529c-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="0529c-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="0529c-208">Çıkış değişikliği: EventData nesnesinden (bu cmdlet’ler tarafından döndürülür) EventChannels alanı artık sabit bir değer (Admin,Operation) döndürdüğünden kullanım dışı bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="0529c-208">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="0529c-209">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-209">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="0529c-210">Çıkış değişikliği: Kullanıcı deneyiminin geliştirilmesi için bu cmdlet’in çıkışı, özellikler alanı kaldırılarak düzleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="0529c-210">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="0529c-211">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="0529c-211">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="0529c-212">Çıkış değişikliği: AutoscaleSettingResourceName alanı her zaman Name alanına eşit olduğundan kullanımdan kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="0529c-212">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell-interactive
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="0529c-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="0529c-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="0529c-214">Çıkış değişikliği: Çıkışın türü, istek kimliğini ve durum kodunu içeren tek bir nesne döndürecek şekilde değiştirilecek.</span><span class="sxs-lookup"><span data-stu-id="0529c-214">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell-interactive
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="0529c-215">Ağ cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-215">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="0529c-216">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="0529c-216">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="0529c-217">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="0529c-218">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="0529c-218">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="0529c-219">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="0529c-220">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="0529c-220">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="0529c-221">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-221">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="0529c-222">Kaynaklar cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-222">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="0529c-223">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="0529c-223">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="0529c-224">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="0529c-225">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="0529c-225">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="0529c-226">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="0529c-227">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="0529c-227">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="0529c-228">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="0529c-229">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="0529c-229">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="0529c-230">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="0529c-231">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="0529c-231">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="0529c-232">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="0529c-233">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="0529c-233">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="0529c-234">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0529c-234">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="0529c-235">ServiceBus cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0529c-235">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="0529c-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-237">'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-237">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-238">Lütfen 'Get-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-238">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="0529c-239">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="0529c-239">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="0529c-240">'Get-AzureRmServiceBusTopicKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-240">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-241">Lütfen 'Get-AzureRmServiceBusKey' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-241">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="0529c-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-243">'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-243">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-244">Lütfen 'New-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-244">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="0529c-245">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="0529c-245">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="0529c-246">'New-AzureRmServiceBusTopicKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-246">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-247">Lütfen 'New-AzureRmServiceBusKey' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-247">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="0529c-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-249">'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-249">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-250">Lütfen 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-250">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="0529c-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-252">'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-252">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-253">Lütfen 'Set-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-253">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="0529c-254">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="0529c-254">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="0529c-255">'New-AzureRmServiceBusNamespaceKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-255">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-256">Lütfen 'New-AzureRmServiceBusKey' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-256">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="0529c-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-258">'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-258">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-259">Lütfen 'Get-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-259">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="0529c-260">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="0529c-260">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="0529c-261">'Get-AzureRmServiceBusQueueKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-261">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-262">Lütfen 'Get-AzureRmServiceBusKey' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-262">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="0529c-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-264">'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-264">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-265">Lütfen 'New-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-265">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="0529c-266">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="0529c-266">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="0529c-267">'New-AzureRmServiceBusQueueKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-267">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-268">Lütfen 'New-AzureRmServiceBusKey' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-268">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="0529c-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-270">'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-270">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-271">Lütfen 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-271">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="0529c-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-273">'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-273">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-274">Lütfen 'Set-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-274">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="0529c-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-276">'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-276">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-277">Lütfen 'Get-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-277">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="0529c-278">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="0529c-278">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="0529c-279">'Get-AzureRmServiceBusNamespaceKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-279">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-280">Lütfen 'Get-AzureRmServiceBusKey' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-280">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="0529c-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-282">'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-282">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-283">Lütfen 'New-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-283">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="0529c-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-285">'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-285">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-286">Lütfen 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-286">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="0529c-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="0529c-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="0529c-288">'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0529c-288">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="0529c-289">Lütfen 'Set-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0529c-289">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="0529c-290">**NamespaceAttributes Türü**</span><span class="sxs-lookup"><span data-stu-id="0529c-290">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="0529c-291">Aşağıdaki özellikler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0529c-291">The following properties have been removed</span></span>
    - <span data-ttu-id="0529c-292">Etkin</span><span class="sxs-lookup"><span data-stu-id="0529c-292">Enabled</span></span>
    - <span data-ttu-id="0529c-293">Durum</span><span class="sxs-lookup"><span data-stu-id="0529c-293">Status</span></span>
   
```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="0529c-294">**QueueAttribute Türü**</span><span class="sxs-lookup"><span data-stu-id="0529c-294">**Type QueueAttribute**</span></span>
- <span data-ttu-id="0529c-295">Aşağıdaki özellikler eski olarak işaretlendi:</span><span class="sxs-lookup"><span data-stu-id="0529c-295">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="0529c-296">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="0529c-296">EnableBatchedOperations</span></span>
    - <span data-ttu-id="0529c-297">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="0529c-297">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="0529c-298">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="0529c-298">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="0529c-299">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="0529c-299">SupportOrdering</span></span>

```powershell-interactive
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a><span data-ttu-id="0529c-300">**TopicAttribute Türü**</span><span class="sxs-lookup"><span data-stu-id="0529c-300">**Type TopicAttribute**</span></span>
- <span data-ttu-id="0529c-301">Aşağıdaki özellikler eski olarak işaretlendi:</span><span class="sxs-lookup"><span data-stu-id="0529c-301">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="0529c-302">Konum</span><span class="sxs-lookup"><span data-stu-id="0529c-302">Location</span></span>
    - <span data-ttu-id="0529c-303">IsExpress</span><span class="sxs-lookup"><span data-stu-id="0529c-303">IsExpress</span></span>
    - <span data-ttu-id="0529c-304">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="0529c-304">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="0529c-305">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="0529c-305">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="0529c-306">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="0529c-306">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="0529c-307">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="0529c-307">EntityAvailabilityStatus</span></span>

```powershell-interactive
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="0529c-308">**SubscriptionAttribute Türü**</span><span class="sxs-lookup"><span data-stu-id="0529c-308">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="0529c-309">Aşağıdaki özellikler eski olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="0529c-309">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="0529c-310">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="0529c-310">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="0529c-311">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="0529c-311">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="0529c-312">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="0529c-312">IsReadOnly</span></span>
    - <span data-ttu-id="0529c-313">Konum</span><span class="sxs-lookup"><span data-stu-id="0529c-313">Location</span></span>
   
```powershell-interactive
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```