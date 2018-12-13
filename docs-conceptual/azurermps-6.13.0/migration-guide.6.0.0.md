---
title: Microsoft Azure PowerShell 6.0.0 için hataya neden olan değişiklikler
description: Bu geçiş kılavuzu, Azure PowerShell sürüm 6 yayınında yapılan ve hataya neden olan değişikliklerin listesini içerir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 39d9fa6e354c3c3448053c9cdc98fdc7f55b068d
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/13/2018
ms.locfileid: "53217414"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a><span data-ttu-id="5a98e-103">Microsoft Azure PowerShell 6.0.0 için hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-103">Breaking changes for Microsoft Azure PowerShell 6.0.0</span></span>

<span data-ttu-id="5a98e-104">Bu belge, Microsoft Azure PowerShell cmdlet’lerini kullananlar için hem bozucu değişiklik bildirimi hem de geçiş kılavuzu olarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="5a98e-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="5a98e-105">Her bölümde hem bozucu değişikliğin yapılma nedeni hem de en kolay geçiş yolu açıklanır.</span><span class="sxs-lookup"><span data-stu-id="5a98e-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="5a98e-106">Bağlamla ilgili daha ayrıntılı bilgi edinmek için lütfen her bir değişiklikle ilişkili çekme isteğine başvurun.</span><span class="sxs-lookup"><span data-stu-id="5a98e-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="5a98e-107">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="5a98e-107">Table of Contents</span></span>

- [<span data-ttu-id="5a98e-108">Hataya neden olan genel değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-108">General breaking changes</span></span>](#general-breaking-changes)
    - [<span data-ttu-id="5a98e-109">Gereken en düşük PowerShell sürümü 5.0’a yükseldi</span><span class="sxs-lookup"><span data-stu-id="5a98e-109">Minimum PowerShell version required bumped to 5.0</span></span>](#minimum-powershell-version-required-bumped-to-50)
    - [<span data-ttu-id="5a98e-110">Varsayılan olarak etkinleştirilen bağlam otomatik kaydı</span><span class="sxs-lookup"><span data-stu-id="5a98e-110">Context autosaved enabled by default</span></span>](#context-autosave-enabled-by-default)
    - [<span data-ttu-id="5a98e-111">Etiket diğer adlarının kaldırılması</span><span class="sxs-lookup"><span data-stu-id="5a98e-111">Removal of Tags alias</span></span>](#removal-of-tags-alias)
- [<span data-ttu-id="5a98e-112">AzureRM.Compute cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-112">Breaking changes to AzureRM.Compute cmdlets</span></span>](#breaking-changes-to-azurermcompute-cmdlets)
- [<span data-ttu-id="5a98e-113">AzureRM.DataLakeStore cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-113">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [<span data-ttu-id="5a98e-114">AzureRM.Dns cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-114">Breaking changes to AzureRM.Dns cmdlets</span></span>](#breaking-changes-to-azurermdns-cmdlets)
- [<span data-ttu-id="5a98e-115">AzureRM.Insights cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-115">Breaking changes to AzureRM.Insights cmdlets</span></span>](#breaking-changes-to-azurerminsights-cmdlets)
- [<span data-ttu-id="5a98e-116">AzureRM.KeyVault cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-116">Breaking changes to AzureRM.KeyVault cmdlets</span></span>](#breaking-changes-to-azurermkeyvault-cmdlets)
- [<span data-ttu-id="5a98e-117">AzureRM.Network cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-117">Breaking changes to AzureRM.Network cmdlets</span></span>](#breaking-changes-to-azurermnetwork-cmdlets)
- [<span data-ttu-id="5a98e-118">AzureRM.RedisCache cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-118">Breaking changes to AzureRM.RedisCache cmdlets</span></span>](#breaking-changes-to-azurermrediscache-cmdlets)
- [<span data-ttu-id="5a98e-119">AzureRM.Resources cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-119">Breaking changes to AzureRM.Resources cmdlets</span></span>](#breaking-changes-to-azurermresources-cmdlets)
- [<span data-ttu-id="5a98e-120">AzureRM.Storage cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-120">Breaking changes to AzureRM.Storage cmdlets</span></span>](#breaking-changes-to-azurermstorage-cmdlets)
- [<span data-ttu-id="5a98e-121">Kaldırılan modüller</span><span class="sxs-lookup"><span data-stu-id="5a98e-121">Removed modules</span></span>](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a><span data-ttu-id="5a98e-122">Hataya neden olan genel değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-122">General breaking changes</span></span>

### <a name="minimum-powershell-version-required-bumped-to-50"></a><span data-ttu-id="5a98e-123">Gereken en düşük PowerShell sürümü 5.0’a yükseldi</span><span class="sxs-lookup"><span data-stu-id="5a98e-123">Minimum PowerShell version required bumped to 5.0</span></span>

<span data-ttu-id="5a98e-124">Daha önce, Azure PowerShell’in herhangi bir cmdlet’i çalıştırması için _en az_ PowerShell 3.0 sürümü gerekliydi.</span><span class="sxs-lookup"><span data-stu-id="5a98e-124">Previously, Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.</span></span> <span data-ttu-id="5a98e-125">Sonraları bu gereksinim PowerShell 5.0 sürümüne yükseltilecektir.</span><span class="sxs-lookup"><span data-stu-id="5a98e-125">Moving forward, this requirement will be raised to version 5.0 of PowerShell.</span></span> <span data-ttu-id="5a98e-126">PowerShell 5.0’a yükseltme yapma hakkında bilgi için lütfen [bu tabloya](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell) bakın.</span><span class="sxs-lookup"><span data-stu-id="5a98e-126">For information on upgrading to PowerShell 5.0, please see [this table](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

### <a name="context-autosave-enabled-by-default"></a><span data-ttu-id="5a98e-127">Varsayılan olarak etkinleştirilen bağlam otomatik kaydı</span><span class="sxs-lookup"><span data-stu-id="5a98e-127">Context autosave enabled by default</span></span>

<span data-ttu-id="5a98e-128">Bağlam otomatik kaydı, yeni ve farklı PowerShell oturumları arasında kullanılabilen Azure oturum açma bilgilerinin depolanmasıdır.</span><span class="sxs-lookup"><span data-stu-id="5a98e-128">Context autosave is the storage of Azure sign in information that can be used between new and different PowerShell sessions.</span></span> <span data-ttu-id="5a98e-129">Bağlam otomatik kaydı hakkında daha fazla bilgi için lütfen [bu belgeye](https://docs.microsoft.com/powershell/azure/context-persistence) bakın.</span><span class="sxs-lookup"><span data-stu-id="5a98e-129">For more information on context autosave, please see [this document](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="5a98e-130">Daha önce bağlam otomatik kaydı varsayılan olarak devre dışıydı. Diğer bir deyişle, Azure kimlik doğrulama bilgileri bağlam kalıcılığını etkinleştiren `Enable-AzureRmContextAutosave` cmdlet’i çalıştırılana kadar oturumlar arasında depolanmıyordu.</span><span class="sxs-lookup"><span data-stu-id="5a98e-130">Previously by default, context autosave was disabled, which meant the user's Azure authentication information was not stored between sessions until they ran the `Enable-AzureRmContextAutosave` cmdlet to turn on context persistence.</span></span> <span data-ttu-id="5a98e-131">Sonraları, bağlam otomatik kaydı varsayılan olarak etkin duruma geldi ve _bağlam otomatik kaydı ayarları olmayan_ kullanıcıların bağlamları sonraki oturum açmada depolanmaya başladı.</span><span class="sxs-lookup"><span data-stu-id="5a98e-131">Moving forward, context autosave will be enabled by default, which means that users _with no saved context autosave settings_ will have their context stored the next time they sign in.</span></span> <span data-ttu-id="5a98e-132">Kullanıcılar `Disable-AzureRmContextAutosave` cmdlet'ini kullanarak bu işlevselliği kullanmamayı seçebilir.</span><span class="sxs-lookup"><span data-stu-id="5a98e-132">Users can opt out of this functionality by using the `Disable-AzureRmContextAutosave` cmdlet.</span></span>

<span data-ttu-id="5a98e-133">_Not_: Daha önce bağlam otomatik kaydını devre dışı bırakmış veya bağlam otomatik kaydı etkin olan kullanıcılar ve mevcut bağlamlar bu değişiklikten etkilenmeyecektir</span><span class="sxs-lookup"><span data-stu-id="5a98e-133">_Note_: users that previously disabled context autosave or users with context autosave enabled and existing contexts will not be affected by this change</span></span>

### <a name="removal-of-tags-alias"></a><span data-ttu-id="5a98e-134">Etiket diğer adlarının kaldırılması</span><span class="sxs-lookup"><span data-stu-id="5a98e-134">Removal of Tags alias</span></span>

<span data-ttu-id="5a98e-135">`Tag` parametresinin `Tags` diğer adı, çok sayıda cmdlet'ten kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="5a98e-135">The alias `Tags` for the `Tag` parameter has been removed across numerous cmdlets.</span></span> <span data-ttu-id="5a98e-136">Bu değişiklikten etkilenen modüllerin (ve karşılık gelen cmdlet'lerin) listesi aşağıda verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="5a98e-136">Below is a list of modules (and the corresponding cmdlets) affected by this:</span></span>

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a><span data-ttu-id="5a98e-137">AzureRM.Compute cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-137">Breaking changes to AzureRM.Compute cmdlets</span></span>

<span data-ttu-id="5a98e-138">**Çeşitli**</span><span class="sxs-lookup"><span data-stu-id="5a98e-138">**Miscellaneous**</span></span>
- <span data-ttu-id="5a98e-139">`PSDisk` ve `PSSnapshot` türlerinde iç içe yerleştirilmiş sku name özelliğinin `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-139">The sku name property nested in types `PSDisk` and `PSSnapshot` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell-interactive
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- <span data-ttu-id="5a98e-140">`PSVirtualMachine`, `PSVirtualMachineScaleSet` ve `PSImage` türlerinde iç içe yerleştirilmiş storage account type özelliğinin `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-140">The storage account type property nested in types `PSVirtualMachine`, `PSVirtualMachineScaleSet` and `PSImage` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell-interactive
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

<span data-ttu-id="5a98e-141">**Add-AzureRmImageDataDisk**</span><span class="sxs-lookup"><span data-stu-id="5a98e-141">**Add-AzureRmImageDataDisk**</span></span>
- <span data-ttu-id="5a98e-142">`StorageAccountType` parametresinin kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-142">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5a98e-143">**Add-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="5a98e-143">**Add-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="5a98e-144">`StorageAccountType` parametresinin kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-144">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5a98e-145">**Add-AzureRmVmssDataDisk**</span><span class="sxs-lookup"><span data-stu-id="5a98e-145">**Add-AzureRmVmssDataDisk**</span></span>
- <span data-ttu-id="5a98e-146">`StorageAccountType` parametresinin kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-146">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5a98e-147">**New-AzureRmAvailabilitySet**</span><span class="sxs-lookup"><span data-stu-id="5a98e-147">**New-AzureRmAvailabilitySet**</span></span>
- <span data-ttu-id="5a98e-148">`Managed` parametresi kaldırılarak `Sku` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-148">The parameter `Managed` was removed in favor of `Sku`</span></span>

```powershell-interactive
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

<span data-ttu-id="5a98e-149">**New-AzureRmDiskConfig**</span><span class="sxs-lookup"><span data-stu-id="5a98e-149">**New-AzureRmDiskConfig**</span></span>
- <span data-ttu-id="5a98e-150">`SkuName` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-150">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5a98e-151">**New-AzureRmDiskUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="5a98e-151">**New-AzureRmDiskUpdateConfig**</span></span>
- <span data-ttu-id="5a98e-152">`SkuName` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-152">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5a98e-153">**New-AzureRmSnapshotConfig**</span><span class="sxs-lookup"><span data-stu-id="5a98e-153">**New-AzureRmSnapshotConfig**</span></span>
- <span data-ttu-id="5a98e-154">`SkuName` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-154">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5a98e-155">**New-AzureRmSnapshotUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="5a98e-155">**New-AzureRmSnapshotUpdateConfig**</span></span>
- <span data-ttu-id="5a98e-156">`SkuName` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-156">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5a98e-157">**Set-AzureRmImageOsDisk**</span><span class="sxs-lookup"><span data-stu-id="5a98e-157">**Set-AzureRmImageOsDisk**</span></span>
- <span data-ttu-id="5a98e-158">`StorageAccountType` parametresinin kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-158">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5a98e-159">**Set-AzureRmVMAEMExtension**</span><span class="sxs-lookup"><span data-stu-id="5a98e-159">**Set-AzureRmVMAEMExtension**</span></span>
- <span data-ttu-id="5a98e-160">`DisableWAD` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-160">The parameter `DisableWAD` was removed</span></span>
    -  <span data-ttu-id="5a98e-161">Windows Azure Tanılama varsayılan olarak devre dışıdır</span><span class="sxs-lookup"><span data-stu-id="5a98e-161">Windows Azure Diagnostics is disabled by default</span></span>

<span data-ttu-id="5a98e-162">**Set-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="5a98e-162">**Set-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="5a98e-163">`StorageAccountType` parametresinin kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-163">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5a98e-164">**Set-AzureRmVMOSDisk**</span><span class="sxs-lookup"><span data-stu-id="5a98e-164">**Set-AzureRmVMOSDisk**</span></span>
- <span data-ttu-id="5a98e-165">`StorageAccountType` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-165">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5a98e-166">**Set-AzureRmVmssStorageProfile**</span><span class="sxs-lookup"><span data-stu-id="5a98e-166">**Set-AzureRmVmssStorageProfile**</span></span>
- <span data-ttu-id="5a98e-167">`ManagedDisk` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-167">The accepted values for parameter `ManagedDisk` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="5a98e-168">**Update-AzureRmVmss**</span><span class="sxs-lookup"><span data-stu-id="5a98e-168">**Update-AzureRmVmss**</span></span>
- <span data-ttu-id="5a98e-169">`ManagedDiskStorageAccountType` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-169">The accepted values for parameter `ManagedDiskStorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a><span data-ttu-id="5a98e-170">AzureRM.DataLakeStore cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-170">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>

<span data-ttu-id="5a98e-171">**Export-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="5a98e-171">**Export-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="5a98e-172">`PerFileThreadCount` ve `ConcurrentFileCount` parametreleri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="5a98e-172">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="5a98e-173">Lütfen bundan sonra `Concurrency` parametresini kullanın</span><span class="sxs-lookup"><span data-stu-id="5a98e-173">Please use the `Concurrency` parameter moving forward</span></span>

```powershell-interactive
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

<span data-ttu-id="5a98e-174">**Import-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="5a98e-174">**Import-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="5a98e-175">`PerFileThreadCount` ve `ConcurrentFileCount` parametreleri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="5a98e-175">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="5a98e-176">Lütfen bundan sonra `Concurrency` parametresini kullanın</span><span class="sxs-lookup"><span data-stu-id="5a98e-176">Please use the `Concurrency` parameter moving forward</span></span>

```powershell-interactive
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

<span data-ttu-id="5a98e-177">**Remove-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="5a98e-177">**Remove-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="5a98e-178">`Clean` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-178">Parameter `Clean` was removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a><span data-ttu-id="5a98e-179">AzureRM.Dns cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-179">Breaking changes to AzureRM.Dns cmdlets</span></span>

<span data-ttu-id="5a98e-180">**New-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="5a98e-180">**New-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="5a98e-181">`Force` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-181">The parameter `Force` was removed</span></span>

<span data-ttu-id="5a98e-182">**Remove-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="5a98e-182">**Remove-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="5a98e-183">`Force` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-183">The parameter `Force` was removed</span></span>

<span data-ttu-id="5a98e-184">**Remove-AzureRmDnsZone**</span><span class="sxs-lookup"><span data-stu-id="5a98e-184">**Remove-AzureRmDnsZone**</span></span>
- <span data-ttu-id="5a98e-185">`Force` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-185">The parameter `Force` was removed</span></span>

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a><span data-ttu-id="5a98e-186">AzureRM.Insights cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-186">Breaking changes to AzureRM.Insights cmdlets</span></span>

<span data-ttu-id="5a98e-187">**Add-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="5a98e-187">**Add-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="5a98e-188">`AutoscaleProfiles` ve `Notifications` parametre diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-188">The parameter aliases `AutoscaleProfiles` and `Notifications` were removed</span></span>

<span data-ttu-id="5a98e-189">**Add-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="5a98e-189">**Add-AzureRmLogProfile**</span></span>
- <span data-ttu-id="5a98e-190">`Categories` ve `Locations` parametre diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-190">The parameter aliases `Categories` and `Locations` were removed</span></span>

<span data-ttu-id="5a98e-191">**Add-AzureRmMetricAlertRule**</span><span class="sxs-lookup"><span data-stu-id="5a98e-191">**Add-AzureRmMetricAlertRule**</span></span>
- <span data-ttu-id="5a98e-192">`Actions` parametre diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-192">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="5a98e-193">**Add-AzureRmWebtestAlertRule**</span><span class="sxs-lookup"><span data-stu-id="5a98e-193">**Add-AzureRmWebtestAlertRule**</span></span>
- <span data-ttu-id="5a98e-194">`Actions` parametre diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-194">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="5a98e-195">**Get-AzureRmLog**</span><span class="sxs-lookup"><span data-stu-id="5a98e-195">**Get-AzureRmLog**</span></span>
- <span data-ttu-id="5a98e-196">`MaxRecords` ve `MaxEvents` parametre diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-196">The parameter aliases `MaxRecords` and `MaxEvents` were removed</span></span>

<span data-ttu-id="5a98e-197">**Get-AzureRmMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="5a98e-197">**Get-AzureRmMetricDefinition**</span></span>
- <span data-ttu-id="5a98e-198">`MetricNames` parametre diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-198">The parameter alias `MetricNames` was removed</span></span>

<span data-ttu-id="5a98e-199">**New-AzureRmAlertRuleEmail**</span><span class="sxs-lookup"><span data-stu-id="5a98e-199">**New-AzureRmAlertRuleEmail**</span></span>
- <span data-ttu-id="5a98e-200">`CustomEmails` ve `SendToServiceOwners` parametre diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-200">The parameter aliases `CustomEmails` and `SendToServiceOwners` were removed</span></span>

<span data-ttu-id="5a98e-201">**New-AzureRmAlertRuleWebhook**</span><span class="sxs-lookup"><span data-stu-id="5a98e-201">**New-AzureRmAlertRuleWebhook**</span></span>
- <span data-ttu-id="5a98e-202">`Properties` parametre diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-202">The parameter alias `Properties` was removed</span></span>

<span data-ttu-id="5a98e-203">**New-AzureRmAutoscaleNotification**</span><span class="sxs-lookup"><span data-stu-id="5a98e-203">**New-AzureRmAutoscaleNotification**</span></span>
- <span data-ttu-id="5a98e-204">`CustomEmails`, `SendEmailToSubscriptionCoAdministrators` ve `Webhooks` parametre diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-204">The parameter aliases `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` and `Webhooks` were removed</span></span>

<span data-ttu-id="5a98e-205">**New-AzureRmAutoscaleProfile**</span><span class="sxs-lookup"><span data-stu-id="5a98e-205">**New-AzureRmAutoscaleProfile**</span></span>
- <span data-ttu-id="5a98e-206">`Rules`, `ScheduleDays`, `ScheduleHours` ve `ScheduleMinutes` parametre diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-206">The parameter aliases `Rules`, `ScheduleDays`, `ScheduleHours` and `ScheduleMinutes` were removed</span></span>

<span data-ttu-id="5a98e-207">**New-AzureRmAutoscaleWebhook**</span><span class="sxs-lookup"><span data-stu-id="5a98e-207">**New-AzureRmAutoscaleWebhook**</span></span>
- <span data-ttu-id="5a98e-208">`Properties` parametre diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-208">The parameter alias `Properties` was removed</span></span>

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a><span data-ttu-id="5a98e-209">AzureRM.KeyVault cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-209">Breaking changes to AzureRM.KeyVault cmdlets</span></span>

<span data-ttu-id="5a98e-210">**Add-AzureKeyVaultCertificate**</span><span class="sxs-lookup"><span data-stu-id="5a98e-210">**Add-AzureKeyVaultCertificate**</span></span>
- <span data-ttu-id="5a98e-211">`CertificatePolicy` parametresi zorunlu hale geldi.</span><span class="sxs-lookup"><span data-stu-id="5a98e-211">The `CertificatePolicy` parameter has become mandatory.</span></span>

<span data-ttu-id="5a98e-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span><span class="sxs-lookup"><span data-stu-id="5a98e-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span></span>
- <span data-ttu-id="5a98e-213">Cmdlet artık erişim belirtecini oluşturan tek parametreleri kabul etmez; bunun yerine cmdlet, `Service` veya `Permissions` gibi açık belirteç parametrelerini, başka bir yerde tanımlanmış örnek bir erişim belirtecine karşılık gelen genel bir `TemplateUri` parametresi ile değiştirir (büyük olasılıkla Depolama PowerShell cmdlet’lerini kullanarak veya Depolama belgelerine uygun şekilde el ile oluşturarak.) Cmdlet `ValidityPeriod` parametresini korur.</span><span class="sxs-lookup"><span data-stu-id="5a98e-213">The cmdlet no longer accepts individual parameters that compose the access token; instead, the cmdlet replaces explicit token parameters, such as `Service` or `Permissions`, with a generic `TemplateUri` parameter, corresponding to a sample access token defined elsewhere (presumably using Storage PowerShell cmdlets, or composed manually according to the Storage documentation.) The cmdlet retains the `ValidityPeriod` parameter.</span></span>

<span data-ttu-id="5a98e-214">Azure Depolama için paylaşılan erişim belirteçleri oluşturma hakkında daha fazla bilgi için lütfen belgeler sayfasına sırasıyla bakın:</span><span class="sxs-lookup"><span data-stu-id="5a98e-214">For more information on composing shared access tokens for Azure Storage, please refer to the documentation pages, respectively:</span></span>
- [<span data-ttu-id="5a98e-215">Hizmet SAS oluşturma</span><span class="sxs-lookup"><span data-stu-id="5a98e-215">Constructing a Service SAS</span></span>](https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)
- [<span data-ttu-id="5a98e-216">Hesap SAS oluşturma</span><span class="sxs-lookup"><span data-stu-id="5a98e-216">Constructing an Account SAS</span></span>](https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)

```powershell-interactive
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

<span data-ttu-id="5a98e-217">**Set-AzureKeyVaultCertificateIssuer**</span><span class="sxs-lookup"><span data-stu-id="5a98e-217">**Set-AzureKeyVaultCertificateIssuer**</span></span>
- <span data-ttu-id="5a98e-218">`IssuerProvider` parametresi zorunlu hale geldi.</span><span class="sxs-lookup"><span data-stu-id="5a98e-218">The `IssuerProvider` parameter has become mandatory.</span></span>

<span data-ttu-id="5a98e-219">**Undo-AzureKeyVaultCertificateRemoval**</span><span class="sxs-lookup"><span data-stu-id="5a98e-219">**Undo-AzureKeyVaultCertificateRemoval**</span></span>
- <span data-ttu-id="5a98e-220">Bu cmdlet’in `CertificateBundle` olan çıktısı `PSKeyVaultCertificate` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="5a98e-220">The output of this cmdlet has changed from `CertificateBundle` to `PSKeyVaultCertificate`.</span></span>

<span data-ttu-id="5a98e-221">**Undo-AzureRmKeyVaultRemoval**</span><span class="sxs-lookup"><span data-stu-id="5a98e-221">**Undo-AzureRmKeyVaultRemoval**</span></span>
- <span data-ttu-id="5a98e-222">`ResourceGroupName`, `InputObject` parametre kümesinden kaldırıldı ve onun yerine `InputObject` parametresinin `ResourceId` özelliği elde edildi.</span><span class="sxs-lookup"><span data-stu-id="5a98e-222">`ResourceGroupName` has been removed from the `InputObject` parameter set, and is instead obtained from the `InputObject` parameter's `ResourceId` property.</span></span>

<span data-ttu-id="5a98e-223">**Set-AzureRmKeyVaultAccessPolicy**</span><span class="sxs-lookup"><span data-stu-id="5a98e-223">**Set-AzureRmKeyVaultAccessPolicy**</span></span>
- <span data-ttu-id="5a98e-224">`all` izni `PermissionsToKeys`, `PermissionsToSecrets` ve `PermissionsToCertificates` içinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="5a98e-224">The `all` permission was removed from `PermissionsToKeys`, `PermissionsToSecrets`, and `PermissionsToCertificates`.</span></span>

<span data-ttu-id="5a98e-225">**Genel**</span><span class="sxs-lookup"><span data-stu-id="5a98e-225">**General**</span></span>
- <span data-ttu-id="5a98e-226">`ValueFromPipelineByPropertyName` özelliği, `InputObject` ile kanal oluşturmanın etkin olduğu tüm cmdlet'lerden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="5a98e-226">The `ValueFromPipelineByPropertyName` property was removed from all cmdlets where piping by `InputObject` was enabled.</span></span>  <span data-ttu-id="5a98e-227">Etkilenen cmdlet'ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5a98e-227">The cmdlets affected are:</span></span>
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="5a98e-228">`ConfirmImpact` düzeyleri tüm cmdlet'lerden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="5a98e-228">`ConfirmImpact` levels were removed from all cmdlets.</span></span>  <span data-ttu-id="5a98e-229">Etkilenen cmdlet'ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5a98e-229">The cmdlets affected are:</span></span>
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="5a98e-230">`IKeyVaultDataServiceClient`, tüm Certificate işlemleri SDK türleri yerine PSTypes döndürecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="5a98e-230">The `IKeyVaultDataServiceClient` was updated so all Certificate operations return PSTypes instead of SDK types.</span></span> <span data-ttu-id="5a98e-231">Buna aşağıdakiler dahildir:</span><span class="sxs-lookup"><span data-stu-id="5a98e-231">This includes:</span></span>
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a><span data-ttu-id="5a98e-232">AzureRM.Network cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-232">Breaking changes to AzureRM.Network cmdlets</span></span>


<span data-ttu-id="5a98e-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="5a98e-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="5a98e-234">`ProbeEnabled` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-234">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="5a98e-235">**Add-AzureRmVirtualNetworkPeering**</span><span class="sxs-lookup"><span data-stu-id="5a98e-235">**Add-AzureRmVirtualNetworkPeering**</span></span>
- <span data-ttu-id="5a98e-236">`AlloowGatewayTransit` parametre diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-236">The parameter alias `AlloowGatewayTransit` was removed</span></span>

<span data-ttu-id="5a98e-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="5a98e-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="5a98e-238">`ProbeEnabled` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-238">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="5a98e-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="5a98e-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="5a98e-240">`ProbeEnabled` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-240">The parameter `ProbeEnabled` was removed</span></span>

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a><span data-ttu-id="5a98e-241">AzureRM.RedisCache cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-241">Breaking changes to AzureRM.RedisCache cmdlets</span></span>

<span data-ttu-id="5a98e-242">**New-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="5a98e-242">**New-AzureRmRedisCache**</span></span>
- <span data-ttu-id="5a98e-243">`Subnet` ve `VirtualNetwork` parametreleri kaldırılarak `SubnetId` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-243">The parameters `Subnet` and `VirtualNetwork` were removed in favor of `SubnetId`</span></span>
- <span data-ttu-id="5a98e-244">`RedisVersion` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-244">The parameter `RedisVersion` was removed</span></span>
- <span data-ttu-id="5a98e-245">`MaxMemoryPolicy` parametresi kaldırılarak `RedisConfiguration` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-245">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell-interactive
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

<span data-ttu-id="5a98e-246">**Set-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="5a98e-246">**Set-AzureRmRedisCache**</span></span>
- <span data-ttu-id="5a98e-247">`MaxMemoryPolicy` parametresi kaldırılarak `RedisConfiguration` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="5a98e-247">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell-interactive
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a><span data-ttu-id="5a98e-248">AzureRM.Resources cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-248">Breaking changes to AzureRM.Resources cmdlets</span></span>

<span data-ttu-id="5a98e-249">**Find-AzureRmResource**</span><span class="sxs-lookup"><span data-stu-id="5a98e-249">**Find-AzureRmResource**</span></span>
- <span data-ttu-id="5a98e-250">Bu cmdlet kaldırıldı ve işlevsellik `Get-AzureRmResource` içine taşındı</span><span class="sxs-lookup"><span data-stu-id="5a98e-250">This cmdlet was removed and the functionality was moved into `Get-AzureRmResource`</span></span>

```powershell-interactive
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

<span data-ttu-id="5a98e-251">**Find-AzureRmResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="5a98e-251">**Find-AzureRmResourceGroup**</span></span>
- <span data-ttu-id="5a98e-252">Bu cmdlet kaldırıldı ve işlevsellik `Get-AzureRmResourceGroup` içine taşındı</span><span class="sxs-lookup"><span data-stu-id="5a98e-252">This cmdlet was removed and the functionality was moved into `Get-AzureRmResourceGroup`</span></span>

```powershell-interactive
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

<span data-ttu-id="5a98e-253">**Get-AzureRmRoleDefinition**</span><span class="sxs-lookup"><span data-stu-id="5a98e-253">**Get-AzureRmRoleDefinition**</span></span>
- <span data-ttu-id="5a98e-254">`AtScopeAndBelow` parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="5a98e-254">Parameter `AtScopeAndBelow` was removed.</span></span>

```powershell-interactive

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a><span data-ttu-id="5a98e-255">AzureRM.Storage cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5a98e-255">Breaking changes to AzureRM.Storage cmdlets</span></span>

<span data-ttu-id="5a98e-256">**New-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="5a98e-256">**New-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="5a98e-257">`EnableEncryptionService` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-257">The parameter `EnableEncryptionService` was removed</span></span>

<span data-ttu-id="5a98e-258">**Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="5a98e-258">**Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="5a98e-259">`EnableEncryptionService` ve `DisableEncryptionService` parametreleri kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5a98e-259">The parameters `EnableEncryptionService` and `DisableEncryptionService` were removed</span></span>

## <a name="removed-modules"></a><span data-ttu-id="5a98e-260">Kaldırılan modüller</span><span class="sxs-lookup"><span data-stu-id="5a98e-260">Removed modules</span></span>

### `AzureRM.ServerManagement`

<span data-ttu-id="5a98e-261">Sunucu Yönetim Araçları hizmeti [geçen yıl kullanımdan kaldırıldı](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/) ve sonuç olarak SMT için karşılık gelen `AzureRM.ServerManagement` modülü, `AzureRM` içinden kaldırıldı ve bundan sonra gönderilmeyecek.</span><span class="sxs-lookup"><span data-stu-id="5a98e-261">The Server Management Tools service was [retired last year](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), and as a result, the corresponding module for SMT, `AzureRM.ServerManagement`, was removed from `AzureRM` and will stop shipping moving forward.</span></span>

### `AzureRM.SiteRecovery`

<span data-ttu-id="5a98e-262">`AzureRM.SiteRecovery` modülünün yerini, `AzureRM.SiteRecovery` modülünün işlevsel bir alt kümesi olup eşdeğer cmdlet’lerden oluşan yeni bir küme içeren `AzureRM.RecoveryServices.SiteRecovery` alacak.</span><span class="sxs-lookup"><span data-stu-id="5a98e-262">The `AzureRM.SiteRecovery` module is being superseded by `AzureRM.RecoveryServices.SiteRecovery`, which is a functional superset of the `AzureRM.SiteRecovery` module and includes a new set of equivalent cmdlets.</span></span> <span data-ttu-id="5a98e-263">Eski ve yeni cmdlet'lerin eşlemelerini içeren tam liste aşağıda bulunabilir:</span><span class="sxs-lookup"><span data-stu-id="5a98e-263">The full list of mappings from old to new cmdlets can be found below:</span></span>

| <span data-ttu-id="5a98e-264">Kullanım dışı bırakılan cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a98e-264">Deprecated cmdlet</span></span>                                        | <span data-ttu-id="5a98e-265">Eşdeğer cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a98e-265">Equivalent cmdlet</span></span>                                                | <span data-ttu-id="5a98e-266">Diğer adlar</span><span class="sxs-lookup"><span data-stu-id="5a98e-266">Aliases</span></span>                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
