---
title: Az 2.0.0 için geçiş kılavuzu
description: Bu geçiş kılavuzu, Azure PowerShell Az sürüm 2.0'da yapılan yeni değişikliklerin listesini içerir.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: d6dac1514fffa140f6d785be9a1a0e8be58476eb
ms.sourcegitcommit: ec731e58b7de3eb14df6d3bf308df92154125bbb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2020
ms.locfileid: "95005849"
---
# <a name="migration-guide-for-az-200"></a><span data-ttu-id="b5f02-103">Az 2.0.0 için Geçiş Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="b5f02-103">Migration Guide for Az 2.0.0</span></span>

<span data-ttu-id="b5f02-104">Bu belgede Az modülünün 1.0.0 ile 2.0.0 sürümleri arasındaki değişiklikler açıklanır</span><span class="sxs-lookup"><span data-stu-id="b5f02-104">This document describes the changes between the 1.0.0 and 2.0.0 versions of Az</span></span> 

## <a name="table-of-contents"></a><span data-ttu-id="b5f02-105">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="b5f02-105">Table of Contents</span></span>
- [<span data-ttu-id="b5f02-106">Modüldeki yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="b5f02-106">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="b5f02-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b5f02-107">Az.Compute</span></span>](#azcompute)
  - [<span data-ttu-id="b5f02-108">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b5f02-108">Az.HDInsight</span></span>](#azhdinsight)
  - [<span data-ttu-id="b5f02-109">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b5f02-109">Az.Storage</span></span>](#azstorage)

## <a name="module-breaking-changes"></a><span data-ttu-id="b5f02-110">Modüldeki yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="b5f02-110">Module breaking changes</span></span>

### <a name="azcompute"></a><span data-ttu-id="b5f02-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b5f02-111">Az.Compute</span></span>

- <span data-ttu-id="b5f02-112">`New-AzAvailabilitySet` ve `Update-AzAvailabilitySet` cmdlet'lerinden `Managed` parametresi kaldırıldı, artık ```Sku = Aligned``` kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="b5f02-112">Removed `Managed` Parameter from `New-AzAvailabilitySet` and `Update-AzAvailabilitySet` cmdlets in favor of using ```Sku = Aligned```</span></span>

  #### <a name="before"></a><span data-ttu-id="b5f02-113">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-113">Before</span></span>

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-114">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-114">After</span></span>

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- <span data-ttu-id="b5f02-115">Tutarlılık sağlamak için `Update-AzImage` cmdlet'inde 'ByName' ve 'ByResourceId' parametre kümelerinden `Image` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="b5f02-115">For consistency, removed `Image` parameter from 'ByName' and 'ByResourceId' parameter sets in `Update-AzImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="b5f02-116">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-116">Before</span></span>

  <span data-ttu-id="b5f02-117">Aşağıdaki kodun işlevsel olduğuna ama geçirilen ImageName değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="b5f02-117">Note that the below code is functional, but the passed-in ImageName is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-118">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-118">After</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- <span data-ttu-id="b5f02-119">Tutarlılık sağlamak için `Restart-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="b5f02-119">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Restart-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="b5f02-120">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-120">Before</span></span>

  <span data-ttu-id="b5f02-121">Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="b5f02-121">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-122">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-122">After</span></span>

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="b5f02-123">Tutarlılık sağlamak için `Start-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="b5f02-123">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Start-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="b5f02-124">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-124">Before</span></span>

  <span data-ttu-id="b5f02-125">Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="b5f02-125">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-126">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-126">After</span></span>

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="b5f02-127">Tutarlılık sağlamak için `Stop-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="b5f02-127">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Stop-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="b5f02-128">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-128">Before</span></span>

  <span data-ttu-id="b5f02-129">Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="b5f02-129">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-130">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-130">After</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="b5f02-131">Tutarlılık sağlamak için `Remove-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="b5f02-131">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Remove-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="b5f02-132">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-132">Before</span></span>

  <span data-ttu-id="b5f02-133">Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="b5f02-133">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-134">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-134">After</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- <span data-ttu-id="b5f02-135">Tutarlılık sağlamak için `Set-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="b5f02-135">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Set-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="b5f02-136">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-136">Before</span></span>

  <span data-ttu-id="b5f02-137">Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="b5f02-137">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-138">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-138">After</span></span>

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- <span data-ttu-id="b5f02-139">Tutarlılık sağlamak için `Save-AzVMImage` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="b5f02-139">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Save-AzVMImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="b5f02-140">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-140">Before</span></span>
  <span data-ttu-id="b5f02-141">Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="b5f02-141">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a><span data-ttu-id="b5f02-142">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-142">After</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- <span data-ttu-id="b5f02-143">`PSVirtualMachineScaleSetVM` içinde `ProtectFromScaleIn` özelliğini kapsüllemek için ProtectionPolicy özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="b5f02-143">Added ProtectionPolicy property to encapsulate `ProtectFromScaleIn` property in `PSVirtualMachineScaleSetVM`</span></span>

  #### <a name="before"></a><span data-ttu-id="b5f02-144">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-144">Before</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-145">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-145">After</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- <span data-ttu-id="b5f02-146">`EncryptionSettings` özelliğini `PSDisk` içine almak için ```EncryptionSettingsCollection``` Özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="b5f02-146">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSDisk`</span></span>

  #### <a name="before"></a><span data-ttu-id="b5f02-147">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-147">Before</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-148">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-148">After</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="b5f02-149">`EncryptionSettings` özelliğini `PSSnapshot` içine almak için ```EncryptionSettingsCollection``` Özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="b5f02-149">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSSnapshot`</span></span>

  #### <a name="before"></a><span data-ttu-id="b5f02-150">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-150">Before</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-151">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-151">After</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="b5f02-152">`PSVirtualMachineScaleSet` içinden `VirtualMachineProfile` özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="b5f02-152">Removed `VirtualMachineProfile` property from `PSVirtualMachineScaleSet`</span></span>

  #### <a name="before"></a><span data-ttu-id="b5f02-153">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-153">Before</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-154">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-154">After</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- <span data-ttu-id="b5f02-155">`Set-AzVMBootDiagnostic` cmdlet'inin `Set-AzVMBootDiagnostics` diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="b5f02-155">Cmdlet `Set-AzVMBootDiagnostic` removed alias to `Set-AzVMBootDiagnostics`</span></span>

  #### <a name="before"></a><span data-ttu-id="b5f02-156">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-156">Before</span></span>

  <span data-ttu-id="b5f02-157">Kullanım dışı bırakılan diğer ad kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="b5f02-157">Using deprecated alias</span></span>

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-158">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-158">After</span></span>

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- <span data-ttu-id="b5f02-159">`Export-AzLogAnalyticThrottledRequest` cmdlet'inin `Export-AzLogAnalyticThrottledRequests` diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="b5f02-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` removed alias to `Export-AzLogAnalyticThrottledRequests`</span></span>

  #### <a name="before"></a><span data-ttu-id="b5f02-160">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-160">Before</span></span>

  <span data-ttu-id="b5f02-161">Kullanım dışı bırakılan diğer ad kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="b5f02-161">Using deprectaed alias</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-162">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-162">After</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a><span data-ttu-id="b5f02-163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b5f02-163">Az.HDInsight</span></span>

- <span data-ttu-id="b5f02-164">`Grant-AzHDInsightHttpServicesAccess` ve `Revoke-AzHDInsightHttpServicesAccess` cmdlet'leri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="b5f02-164">Removed the `Grant-AzHDInsightHttpServicesAccess` and `Revoke-AzHDInsightHttpServicesAccess` cmdlets.</span></span> <span data-ttu-id="b5f02-165">Tüm HDInsight kümelerinde HTTP erişimi her zaman etkin olduğundan artık bunlar gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="b5f02-165">These are no longer necessary because HTTP access is always enabled on all HDInsight clusters.</span></span>
- <span data-ttu-id="b5f02-166">Yeni `Set-AzHDInsightGatewayCredential` cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="b5f02-166">Added a new `Set-AzHDInsightGatewayCredential`  cmdlet.</span></span> <span data-ttu-id="b5f02-167">Ağ geçidi HTTP kullanıcı adını ve parolasını değiştirmek için bu cmdlet'i kullanın (`Grant-AzHDInsightHttpServicesAccess` cmdlet'inin yerini aldı).</span><span class="sxs-lookup"><span data-stu-id="b5f02-167">Use this cmdlet to change the gateway HTTP username and password (replaces `Grant-AzHDInsightHttpServicesAccess`).</span></span>
- <span data-ttu-id="b5f02-168">`Get-AzHDInsightJobOutput` cmdlet'i depolama anahtarına ayrıntılı rol tabanlı erişimi destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b5f02-168">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
    - <span data-ttu-id="b5f02-169">HDInsight Küme Operatörü, Katkıda Bulunan veya Sahip rolleri olan kullanıcılar etkilenmeyecek.</span><span class="sxs-lookup"><span data-stu-id="b5f02-169">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
    - <span data-ttu-id="b5f02-170">Yalnızca Okuyucu rolüne sahip kullanıcıların `DefaultStorageAccountKey` parametresini açık olarak belirtmesi gerekecek.</span><span class="sxs-lookup"><span data-stu-id="b5f02-170">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

<span data-ttu-id="b5f02-171">Bu rol tabanlı erişim değişiklikleri hakkında daha fazla bilgi için bkz. [aka.ms/hdi-config-update](/azure/hdinsight/hdinsight-migrate-granular-access-cluster-configurations)</span><span class="sxs-lookup"><span data-stu-id="b5f02-171">For more information about these role-based access changes, see [aka.ms/hdi-config-update](/azure/hdinsight/hdinsight-migrate-granular-access-cluster-configurations)</span></span>

  #### <a name="before"></a><span data-ttu-id="b5f02-172">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-172">Before</span></span>

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-173">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-173">After</span></span>

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a><span data-ttu-id="b5f02-174">Get-AzHDInsightJobOutput cmdlet'i için yalnızca Okuyucu rolü olan kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="b5f02-174">Users with only Reader role for cmdlet Get-AzHDInsightJobOutput</span></span>

  ####  <a name="before"></a><span data-ttu-id="b5f02-175">Önce</span><span class="sxs-lookup"><span data-stu-id="b5f02-175">Before</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a><span data-ttu-id="b5f02-176">Sonra</span><span class="sxs-lookup"><span data-stu-id="b5f02-176">After</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a><span data-ttu-id="b5f02-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b5f02-177">Az.Storage</span></span>

- <span data-ttu-id="b5f02-178">Blob, Kuyruk ve Dosya cmdlet'lerinden döndürülen türlerin `Microsoft.WindowsAzure.Storage` olan ad alanları `Microsoft.Azure.Storage` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="b5f02-178">Namespaces for types returned from Blob, Queue, and File cmdlets have changed their namespace from `Microsoft.WindowsAzure.Storage` to `Microsoft.Azure.Storage`.</span></span>  <span data-ttu-id="b5f02-179">Bu hataya neden olan değişiklik ilkesine göre teknik açıdan hataya neden olan bir değişiklik olmasa da, bu cmdlet'lerden döndürülen nesnelerle etkileşim kurmak için Storage .Net SDK'sındaki yöntemleri kullanan kodlarda bazı değişiklikler yapmak gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="b5f02-179">While this is not technically a breaking change according to the breaking change policy, it may require some changes in code that uses the methods from the Storage .Net SDK to interact with the objects returned from these cmdlets.</span></span>

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a><span data-ttu-id="b5f02-180">Örnek 1:  Kuyruğa bir ileti ekleyin (CloudQueueMessage nesnesi ad alanını değiştirin)</span><span class="sxs-lookup"><span data-stu-id="b5f02-180">Example 1:  Add a message to a Queue (change CloudQueueMessage object namespace)</span></span>

  <span data-ttu-id="b5f02-181">Önce:</span><span class="sxs-lookup"><span data-stu-id="b5f02-181">Before:</span></span> 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  <span data-ttu-id="b5f02-182">Sonra:</span><span class="sxs-lookup"><span data-stu-id="b5f02-182">After:</span></span>

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a><span data-ttu-id="b5f02-183">Örnek 2:  AccessCondition ile Blob/Dosya Özniteliklerini getirin (AccessCondition nesnesi ad alanını değiştirin)</span><span class="sxs-lookup"><span data-stu-id="b5f02-183">Example 2:  Fetch Blob/File Attributes with AccessCondition (change AccessCondition object namespace)</span></span>

  <span data-ttu-id="b5f02-184">Önce:</span><span class="sxs-lookup"><span data-stu-id="b5f02-184">Before:</span></span> 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  <span data-ttu-id="b5f02-185">Sonra:</span><span class="sxs-lookup"><span data-stu-id="b5f02-185">After:</span></span>

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- <span data-ttu-id="b5f02-186">Teknik açıdan hataya neden olan bir değişiklik olmasa da, `New/Get/Set-AzStorageAccount` cmdlet'lerinden döndürülen Depolama Hesaplarının Sku.Name özelliğinde aşağıdaki gibi bazı çıkış farklılıkları göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="b5f02-186">While not technically a breaking change, you will notice output differences in the Sku.Name property of Storage Accounts returned from  `New/Get/Set-AzStorageAccount` changes are as follows.</span></span> <span data-ttu-id="b5f02-187">(Değişiklik sonrasında, çıkış ve giriş SkuName adları uyumlu olur.)</span><span class="sxs-lookup"><span data-stu-id="b5f02-187">(After the change, output and input SkuName are aligned.)</span></span>
  - <span data-ttu-id="b5f02-188">"StandardLRS" -> "Standard_LRS";</span><span class="sxs-lookup"><span data-stu-id="b5f02-188">"StandardLRS" -> "Standard_LRS";</span></span>
  - <span data-ttu-id="b5f02-189">"StandardGRS" -> "Standard_GRS";</span><span class="sxs-lookup"><span data-stu-id="b5f02-189">"StandardGRS" -> "Standard_GRS";</span></span>
  - <span data-ttu-id="b5f02-190">"StandardRAGRS" -> "Standard_RAGRS";</span><span class="sxs-lookup"><span data-stu-id="b5f02-190">"StandardRAGRS" -> "Standard_RAGRS";</span></span>
  - <span data-ttu-id="b5f02-191">"StandardZRS" -> "Standard_ZRS";</span><span class="sxs-lookup"><span data-stu-id="b5f02-191">"StandardZRS" -> "Standard_ZRS";</span></span>
  - <span data-ttu-id="b5f02-192">"PremiumLRS" -> "Premium_LRS";</span><span class="sxs-lookup"><span data-stu-id="b5f02-192">"PremiumLRS" -> "Premium_LRS";</span></span>

- <span data-ttu-id="b5f02-193">Kind belirtmeden depolama hesabı oluştururken varsayılan hizmet davranışı değişti.</span><span class="sxs-lookup"><span data-stu-id="b5f02-193">The default service behavior when creating a storage account withous specifying a Kind has changed.</span></span>  <span data-ttu-id="b5f02-194">Önceki sürümlerde `Kind` belirtilmeden bir depolama hesabı oluşturulduğunda Depolama hesabında Kind değeri olarak `Storage` kullanılıyordu; yeni sürümde varsayılan `Kind` değeri `StorageV2` oldu.</span><span class="sxs-lookup"><span data-stu-id="b5f02-194">In previous versions, when a storage account was created with no `Kind` specified, the Storage account Kind of `Storage` was used, in the new version `StorageV2` is the default `Kind` value.</span></span> <span data-ttu-id="b5f02-195">Kind değeri 'Storage' olan bir V1 Depolama hesabı oluşturmanız gerekiyorsa '-Kind Storage' parametresini ekleyin</span><span class="sxs-lookup"><span data-stu-id="b5f02-195">If you need to create a V1 Storage account with Kind 'Storage', add parameter '-Kind Storage'</span></span>

  #### <a name="example--create-a-storage-account-default-kind-change"></a><span data-ttu-id="b5f02-196">Örnek: Depolama hesabı oluşturun (Varsayılan Kind değişikliği)</span><span class="sxs-lookup"><span data-stu-id="b5f02-196">Example : Create a storage Account (Default Kind change)</span></span>  

  <span data-ttu-id="b5f02-197">Önce:</span><span class="sxs-lookup"><span data-stu-id="b5f02-197">Before:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  <span data-ttu-id="b5f02-198">Sonra:</span><span class="sxs-lookup"><span data-stu-id="b5f02-198">After:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```