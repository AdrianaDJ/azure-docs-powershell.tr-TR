---
title: Az 2.0.0 için geçiş kılavuzu
description: Bu geçiş kılavuzu, Azure PowerShell Az sürüm 2.0'da yapılan yeni değişikliklerin listesini içerir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 5f15d1a4f1e8416d7214aceb78494867fe4aad52
ms.sourcegitcommit: a4e527d3deba004007cfa22fa536e8255dd23b37
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67516734"
---
# <a name="migration-guide-for-az-200"></a><span data-ttu-id="8075e-103">Az 2.0.0 için Geçiş Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="8075e-103">Migration Guide for Az 2.0.0</span></span>

<span data-ttu-id="8075e-104">Bu belgede Az modülünün 1.0.0 ile 2.0.0 sürümleri arasındaki değişiklikler açıklanır</span><span class="sxs-lookup"><span data-stu-id="8075e-104">This document describes the changes between the 1.0.0 and 2.0.0 versions of Az</span></span> 

## <a name="table-of-contents"></a><span data-ttu-id="8075e-105">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="8075e-105">Table of Contents</span></span>
- [<span data-ttu-id="8075e-106">Modüldeki yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="8075e-106">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="8075e-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8075e-107">Az.Compute</span></span>](#azcompute)
  - [<span data-ttu-id="8075e-108">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8075e-108">Az.HDInsight</span></span>](#azhdinsight)
  - [<span data-ttu-id="8075e-109">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8075e-109">Az.Storage</span></span>](#azstorage)

## <a name="module-breaking-changes"></a><span data-ttu-id="8075e-110">Modüldeki yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="8075e-110">Module breaking changes</span></span>

### <a name="azcompute"></a><span data-ttu-id="8075e-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8075e-111">Az.Compute</span></span>

- <span data-ttu-id="8075e-112">`New-AzAvailabilitySet` ve `Update-AzAvailabilitySet` cmdlet'lerinden `Managed` parametresi kaldırıldı, artık ```Sku = Aligned``` kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="8075e-112">Removed `Managed` Parameter from `New-AzAvailabilitySet` and `Update-AzAvailabilitySet` cmdlets in favor of using ```Sku = Aligned```</span></span>

  #### <a name="before"></a><span data-ttu-id="8075e-113">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-113">Before</span></span>

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-114">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-114">After</span></span>

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- <span data-ttu-id="8075e-115">Tutarlılık sağlamak için `Update-AzImage` cmdlet'inde 'ByName' ve 'ByResourceId' parametre kümelerinden `Image` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8075e-115">For consistency, removed `Image` parameter from 'ByName' and 'ByResourceId' parameter sets in `Update-AzImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="8075e-116">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-116">Before</span></span>

  <span data-ttu-id="8075e-117">Aşağıdaki kodun işlevsel olduğuna ama geçirilen ImageName değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="8075e-117">Note that the below code is functional, but the passed-in ImageName is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-118">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-118">After</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- <span data-ttu-id="8075e-119">Tutarlılık sağlamak için `Restart-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8075e-119">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Restart-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="8075e-120">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-120">Before</span></span>

  <span data-ttu-id="8075e-121">Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="8075e-121">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-122">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-122">After</span></span>

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="8075e-123">Tutarlılık sağlamak için `Start-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8075e-123">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Start-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="8075e-124">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-124">Before</span></span>

  <span data-ttu-id="8075e-125">Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="8075e-125">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-126">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-126">After</span></span>

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="8075e-127">Tutarlılık sağlamak için `Stop-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8075e-127">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Stop-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="8075e-128">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-128">Before</span></span>

  <span data-ttu-id="8075e-129">Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="8075e-129">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-130">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-130">After</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="8075e-131">Tutarlılık sağlamak için `Remove-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8075e-131">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Remove-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="8075e-132">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-132">Before</span></span>

  <span data-ttu-id="8075e-133">Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="8075e-133">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-134">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-134">After</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- <span data-ttu-id="8075e-135">Tutarlılık sağlamak için `Set-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8075e-135">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Set-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="8075e-136">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-136">Before</span></span>

  <span data-ttu-id="8075e-137">Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="8075e-137">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-138">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-138">After</span></span>

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- <span data-ttu-id="8075e-139">Tutarlılık sağlamak için `Save-AzVMImage` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8075e-139">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Save-AzVMImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="8075e-140">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-140">Before</span></span>
  <span data-ttu-id="8075e-141">Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="8075e-141">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a><span data-ttu-id="8075e-142">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-142">After</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- <span data-ttu-id="8075e-143">`PSVirtualMachineScaleSetVM` içinde `ProtectFromScaleIn` özelliğini kapsüllemek için ProtectionPolicy özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8075e-143">Added ProtectionPolicy property to encapsulate `ProtectFromScaleIn` property in `PSVirtualMachineScaleSetVM`</span></span>

  #### <a name="before"></a><span data-ttu-id="8075e-144">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-144">Before</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-145">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-145">After</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- <span data-ttu-id="8075e-146">`EncryptionSettings` özelliğini `PSDisk` içine almak için ```EncryptionSettingsCollection``` Özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8075e-146">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSDisk`</span></span>

  #### <a name="before"></a><span data-ttu-id="8075e-147">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-147">Before</span></span>

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

  #### <a name="after"></a><span data-ttu-id="8075e-148">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-148">After</span></span>

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

- <span data-ttu-id="8075e-149">`EncryptionSettings` özelliğini `PSSnapshot` içine almak için ```EncryptionSettingsCollection``` Özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8075e-149">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSSnapshot`</span></span>

  #### <a name="before"></a><span data-ttu-id="8075e-150">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-150">Before</span></span>

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

  #### <a name="after"></a><span data-ttu-id="8075e-151">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-151">After</span></span>

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

- <span data-ttu-id="8075e-152">`PSVirtualMachineScaleSet` içinden `VirtualMachineProfile` özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8075e-152">Removed `VirtualMachineProfile` property from `PSVirtualMachineScaleSet`</span></span>

  #### <a name="before"></a><span data-ttu-id="8075e-153">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-153">Before</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-154">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-154">After</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- <span data-ttu-id="8075e-155">`Set-AzVMBootDiagnostic` cmdlet'inin `Set-AzVMBootDiagnostics` diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8075e-155">Cmdlet `Set-AzVMBootDiagnostic` removed alias to `Set-AzVMBootDiagnostics`</span></span>

  #### <a name="before"></a><span data-ttu-id="8075e-156">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-156">Before</span></span>

  <span data-ttu-id="8075e-157">Kullanım dışı bırakılan diğer ad kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="8075e-157">Using deprecated alias</span></span>

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-158">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-158">After</span></span>

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- <span data-ttu-id="8075e-159">`Export-AzLogAnalyticThrottledRequest` cmdlet'inin `Export-AzLogAnalyticThrottledRequests` diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8075e-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` removed alias to `Export-AzLogAnalyticThrottledRequests`</span></span>

  #### <a name="before"></a><span data-ttu-id="8075e-160">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-160">Before</span></span>

  <span data-ttu-id="8075e-161">Kullanım dışı bırakılan diğer ad kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="8075e-161">Using deprectaed alias</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-162">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-162">After</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a><span data-ttu-id="8075e-163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8075e-163">Az.HDInsight</span></span>

- <span data-ttu-id="8075e-164">`Grant-AzHDInsightHttpServicesAccess` ve `Revoke-AzHDInsightHttpServicesAccess` cmdlet'leri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8075e-164">Removed the `Grant-AzHDInsightHttpServicesAccess` and `Revoke-AzHDInsightHttpServicesAccess` cmdlets.</span></span> <span data-ttu-id="8075e-165">Tüm HDInsight kümelerinde HTTP erişimi her zaman etkin olduğundan artık bunlar gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="8075e-165">These are no longer necessary because HTTP access is always enabled on all HDInsight clusters.</span></span>
- <span data-ttu-id="8075e-166">Yeni `Set-AzHDInsightGatewayCredential` cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="8075e-166">Added a new `Set-AzHDInsightGatewayCredential`  cmdlet.</span></span> <span data-ttu-id="8075e-167">Ağ geçidi HTTP kullanıcı adını ve parolasını değiştirmek için bu cmdlet'i kullanın (`Grant-AzHDInsightHttpServicesAccess` cmdlet'inin yerini aldı).</span><span class="sxs-lookup"><span data-stu-id="8075e-167">Use this cmdlet to change the gateway HTTP username and password (replaces `Grant-AzHDInsightHttpServicesAccess`).</span></span>
- <span data-ttu-id="8075e-168">`Get-AzHDInsightJobOutput` cmdlet'i depolama anahtarına ayrıntılı rol tabanlı erişimi destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8075e-168">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
    - <span data-ttu-id="8075e-169">HDInsight Küme Operatörü, Katkıda Bulunan veya Sahip rolleri olan kullanıcılar etkilenmeyecek.</span><span class="sxs-lookup"><span data-stu-id="8075e-169">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
    - <span data-ttu-id="8075e-170">Yalnızca Okuyucu rolüne sahip kullanıcıların `DefaultStorageAccountKey` parametresini açık olarak belirtmesi gerekecek.</span><span class="sxs-lookup"><span data-stu-id="8075e-170">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

<span data-ttu-id="8075e-171">Bu rol tabanlı erişim değişiklikleri hakkında daha fazla bilgi için bkz. [aka.ms/hdi-config-update](http://aka.ms/hdi-config-update)</span><span class="sxs-lookup"><span data-stu-id="8075e-171">For more information about these role-based access changes, see [aka.ms/hdi-config-update](http://aka.ms/hdi-config-update)</span></span>

  #### <a name="before"></a><span data-ttu-id="8075e-172">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-172">Before</span></span>

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-173">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-173">After</span></span>

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a><span data-ttu-id="8075e-174">Get-AzHDInsightJobOutput cmdlet'i için yalnızca Okuyucu rolü olan kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="8075e-174">Users with only Reader role for cmdlet Get-AzHDInsightJobOutput</span></span>

  ####  <a name="before"></a><span data-ttu-id="8075e-175">Önce</span><span class="sxs-lookup"><span data-stu-id="8075e-175">Before</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a><span data-ttu-id="8075e-176">Sonra</span><span class="sxs-lookup"><span data-stu-id="8075e-176">After</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a><span data-ttu-id="8075e-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8075e-177">Az.Storage</span></span>

- <span data-ttu-id="8075e-178">Blob, Kuyruk ve Dosya cmdlet'lerinden döndürülen türlerin `Microsoft.WindowsAzure.Storage` olan ad alanları `Microsoft.Azure.Storage` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8075e-178">Namespaces for types returned from Blob, Queue, and File cmdlets have changed their namespace from `Microsoft.WindowsAzure.Storage` to `Microsoft.Azure.Storage`.</span></span>  <span data-ttu-id="8075e-179">Bu hataya neden olan değişiklik ilkesine göre teknik açıdan hataya neden olan bir değişiklik olmasa da, bu cmdlet'lerden döndürülen nesnelerle etkileşim kurmak için Storage .Net SDK'sındaki yöntemleri kullanan kodlarda bazı değişiklikler yapmak gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="8075e-179">While this is not technically a breaking change according to the breaking change policy, it may require some changes in code that uses the methods from the Storage .Net SDK to interact with the objects returned from these cmdlets.</span></span>

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a><span data-ttu-id="8075e-180">Örnek 1:  Kuyruğa bir ileti ekleyin (CloudQueueMessage nesnesi ad alanını değiştirin)</span><span class="sxs-lookup"><span data-stu-id="8075e-180">Example 1:  Add a message to a Queue (change CloudQueueMessage object namespace)</span></span>

  <span data-ttu-id="8075e-181">Önce:</span><span class="sxs-lookup"><span data-stu-id="8075e-181">Before:</span></span> 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  <span data-ttu-id="8075e-182">Sonra:</span><span class="sxs-lookup"><span data-stu-id="8075e-182">After:</span></span>

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a><span data-ttu-id="8075e-183">Örnek 2:  AccessCondition ile Blob/Dosya Özniteliklerini getirin (AccessCondition nesnesi ad alanını değiştirin)</span><span class="sxs-lookup"><span data-stu-id="8075e-183">Example 2:  Fetch Blob/File Attributes with AccessCondition (change AccessCondition object namespace)</span></span>

  <span data-ttu-id="8075e-184">Önce:</span><span class="sxs-lookup"><span data-stu-id="8075e-184">Before:</span></span> 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  <span data-ttu-id="8075e-185">Sonra:</span><span class="sxs-lookup"><span data-stu-id="8075e-185">After:</span></span>

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- <span data-ttu-id="8075e-186">Teknik açıdan hataya neden olan bir değişiklik olmasa da, `New/Get/Set-AzStorageAccount` cmdlet'lerinden döndürülen Depolama Hesaplarının Sku.Name özelliğinde aşağıdaki gibi bazı çıkış farklılıkları göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="8075e-186">While not technically a breaking change, you will notice output differences in the Sku.Name property of Storage Accounts returned from  `New/Get/Set-AzStorageAccount` changes are as follows.</span></span> <span data-ttu-id="8075e-187">(Değişiklik sonrasında, çıkış ve giriş SkuName adları uyumlu olur.)</span><span class="sxs-lookup"><span data-stu-id="8075e-187">(After the change, output and input SkuName are aligned.)</span></span>
  - <span data-ttu-id="8075e-188">"StandardLRS" -> "Standard_LRS";</span><span class="sxs-lookup"><span data-stu-id="8075e-188">"StandardLRS" -> "Standard_LRS";</span></span>
  - <span data-ttu-id="8075e-189">"StandardGRS" -> "Standard_GRS";</span><span class="sxs-lookup"><span data-stu-id="8075e-189">"StandardGRS" -> "Standard_GRS";</span></span>
  - <span data-ttu-id="8075e-190">"StandardRAGRS" -> "Standard_RAGRS";</span><span class="sxs-lookup"><span data-stu-id="8075e-190">"StandardRAGRS" -> "Standard_RAGRS";</span></span>
  - <span data-ttu-id="8075e-191">"StandardZRS" -> "Standard_ZRS";</span><span class="sxs-lookup"><span data-stu-id="8075e-191">"StandardZRS" -> "Standard_ZRS";</span></span>
  - <span data-ttu-id="8075e-192">"PremiumLRS" -> "Premium_LRS";</span><span class="sxs-lookup"><span data-stu-id="8075e-192">"PremiumLRS" -> "Premium_LRS";</span></span>

- <span data-ttu-id="8075e-193">Kind belirtmeden depolama hesabı oluştururken varsayılan hizmet davranışı değişti.</span><span class="sxs-lookup"><span data-stu-id="8075e-193">The default service behavior when creating a storage account withous specifying a Kind has changed.</span></span>  <span data-ttu-id="8075e-194">Önceki sürümlerde `Kind` belirtilmeden bir depolama hesabı oluşturulduğunda Depolama hesabında Kind değeri olarak `Storage` kullanılıyordu; yeni sürümde varsayılan `Kind` değeri `StorageV2` oldu.</span><span class="sxs-lookup"><span data-stu-id="8075e-194">In previous versions, when a storage account was created with no `Kind` specified, the Storage account Kind of `Storage` was used, in the new version `StorageV2` is the default `Kind` value.</span></span> <span data-ttu-id="8075e-195">Kind değeri 'Storage' olan bir V1 Depolama hesabı oluşturmanız gerekiyorsa '-Kind Storage' parametresini ekleyin</span><span class="sxs-lookup"><span data-stu-id="8075e-195">If you need to create a V1 Storage account with Kind 'Storage', add parameter '-Kind Storage'</span></span>

  #### <a name="example--create-a-storage-account-default-kind-change"></a><span data-ttu-id="8075e-196">Örnek: Depolama hesabı oluşturun (Varsayılan Kind değişikliği)</span><span class="sxs-lookup"><span data-stu-id="8075e-196">Example : Create a storage Account (Default Kind change)</span></span>  

  <span data-ttu-id="8075e-197">Önce:</span><span class="sxs-lookup"><span data-stu-id="8075e-197">Before:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  <span data-ttu-id="8075e-198">Sonra:</span><span class="sxs-lookup"><span data-stu-id="8075e-198">After:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```