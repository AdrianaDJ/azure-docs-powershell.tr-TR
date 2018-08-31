---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 6043d17df1b5e91521bad31e65372c10ee6a5c6a
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250018"
---
# <a name="release-notes"></a><span data-ttu-id="edf93-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="edf93-103">Release notes</span></span>

<span data-ttu-id="edf93-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="edf93-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="680---august-2018"></a><span data-ttu-id="edf93-105">6.8.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="edf93-105">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="edf93-106">Genel</span><span class="sxs-lookup"><span data-stu-id="edf93-106">General</span></span>
* <span data-ttu-id="edf93-107">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-107">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="edf93-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="edf93-108">AzureRM.Profile</span></span>
* <span data-ttu-id="edf93-109">Connect-AzureRmAccount sırasında döndürülen belirteçlere sona erme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-109">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="edf93-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="edf93-110">AzureRM.Compute</span></span>
* <span data-ttu-id="edf93-111">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-111">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="edf93-112">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-112">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="edf93-113">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-113">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="edf93-114">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="edf93-114">AzureRM.IotHub</span></span>
* <span data-ttu-id="edf93-115">New-AzureRmIotHubExportDevices ve New-AzureRmIotHubImportDevices için düzeltme örnekleri</span><span class="sxs-lookup"><span data-stu-id="edf93-115">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="edf93-116">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="edf93-116">AzureRM.Network</span></span>
* <span data-ttu-id="edf93-117">Varsayılan model gösterimi tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-117">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="edf93-118">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="edf93-118">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="edf93-119">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-119">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="edf93-120">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="edf93-120">AzureRM.Resources</span></span>
* <span data-ttu-id="edf93-121">Marketten yönetilen uygulamayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-121">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="edf93-122">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="edf93-122">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="edf93-123">Sorunlar için düzeltme</span><span class="sxs-lookup"><span data-stu-id="edf93-123">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="edf93-124">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="edf93-124">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="edf93-125">Çoklu değer yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="edf93-125">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="edf93-126">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="edf93-126">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="edf93-127">Alt ağ yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="edf93-127">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="edf93-128">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="edf93-128">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="edf93-129">Profillerde Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="edf93-129">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="edf93-130">Profillerde Beklenen durum kodu aralığı desteği</span><span class="sxs-lookup"><span data-stu-id="edf93-130">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="edf93-131">Uç noktalarda Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="edf93-131">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="edf93-132">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="edf93-132">AzureRM.Websites</span></span>
* <span data-ttu-id="edf93-133">Varsayılan kaynak gruplarının yanlış ayarlanmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-133">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="edf93-134">6.7.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="edf93-134">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="edf93-135">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="edf93-135">AzureRM.Profile</span></span>
* <span data-ttu-id="edf93-136">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-136">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="edf93-137">Bağlam çakışmasını önlemek için varsayılan bağlam adına kullanıcı kimliği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-137">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="edf93-138">Bağlam #6398 seçerken sorunlara neden olan Clear-AzureRmContext ile ilgili sorunlar giderildi</span><span class="sxs-lookup"><span data-stu-id="edf93-138">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="edf93-139">'Connect-AzureRmAccount' için kiracı etki alanının '-TenantId' parametresine geçirilmesi etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-139">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="edf93-140">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="edf93-140">Azure.Storage</span></span>
* <span data-ttu-id="edf93-141">Azure Dosya Paylaşımı kotasındaki 5 TB'lık sınır kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="edf93-141">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="edf93-142">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="edf93-142">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="edf93-143">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="edf93-143">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="edf93-144">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-144">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="edf93-145">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="edf93-145">Azure.AnalysisServices</span></span>
* <span data-ttu-id="edf93-146">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-146">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="edf93-147">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="edf93-147">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="edf93-148">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-148">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="edf93-149">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="edf93-149">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="edf93-150">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-150">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="edf93-151">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="edf93-151">AzureRM.Automation</span></span>
* <span data-ttu-id="edf93-152">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-152">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="edf93-153">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="edf93-153">AzureRM.Backup</span></span>
* <span data-ttu-id="edf93-154">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-154">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="edf93-155">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="edf93-155">AzureRM.Batch</span></span>
* <span data-ttu-id="edf93-156">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-156">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="edf93-157">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="edf93-157">AzureRM.Billing</span></span>
* <span data-ttu-id="edf93-158">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="edf93-159">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="edf93-159">AzureRM.Cdn</span></span>
* <span data-ttu-id="edf93-160">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="edf93-161">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="edf93-161">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="edf93-162">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="edf93-163">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="edf93-163">AzureRM.Compute</span></span>
* <span data-ttu-id="edf93-164">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-164">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="edf93-165">New-AzureRmVmssConfig’e EvictionPolicy parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-165">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="edf93-166">Hiçbir konum belirtilmediyse New-AzureRmVm’nin DiskFileParameterSet parametresinde varsayılan konum kullanılıyor.</span><span class="sxs-lookup"><span data-stu-id="edf93-166">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="edf93-167">Save-AzureRmVMImage cmdlet'inde parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-167">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="edf93-168">Singlepass ile ilgili bazı senaryolarda Get-AzureRmVMDiskEncryptionStatus cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-168">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="edf93-169">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="edf93-169">AzureRM.Consumption</span></span>
* <span data-ttu-id="edf93-170">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="edf93-171">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="edf93-171">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="edf93-172">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="edf93-173">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="edf93-173">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="edf93-174">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="edf93-175">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="edf93-175">AzureRM.DataFactories</span></span>
* <span data-ttu-id="edf93-176">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="edf93-177">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="edf93-177">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="edf93-178">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="edf93-179">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="edf93-179">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="edf93-180">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="edf93-181">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="edf93-181">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="edf93-182">DebugPreference Powershell komut satırından ayarlandığında hata ayıklama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-182">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="edf93-183">Set-AzureRmDataLakeStoreItemAcl örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-183">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="edf93-184">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-184">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="edf93-185">Set-AzureRmDataLakeStoreItemAclEntry örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-185">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="edf93-186">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="edf93-186">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="edf93-187">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="edf93-188">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="edf93-188">AzureRM.Dns</span></span>
* <span data-ttu-id="edf93-189">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="edf93-190">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="edf93-190">AzureRM.EventGrid</span></span>
* <span data-ttu-id="edf93-191">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="edf93-192">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="edf93-192">AzureRM.EventHub</span></span>
* <span data-ttu-id="edf93-193">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="edf93-194">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="edf93-194">AzureRM.HDInsight</span></span>
* <span data-ttu-id="edf93-195">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="edf93-196">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="edf93-196">AzureRM.Insights</span></span>
* <span data-ttu-id="edf93-197">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="edf93-198">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="edf93-198">AzureRM.IotHub</span></span>
* <span data-ttu-id="edf93-199">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="edf93-200">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="edf93-200">AzureRM.KeyVault</span></span>
* <span data-ttu-id="edf93-201">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="edf93-202">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="edf93-202">AzureRM.LogicApp</span></span>
* <span data-ttu-id="edf93-203">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-203">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="edf93-204">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="edf93-204">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="edf93-205">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-205">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="edf93-206">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="edf93-206">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="edf93-207">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="edf93-208">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="edf93-208">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="edf93-209">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="edf93-210">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="edf93-210">AzureRM.Media</span></span>
* <span data-ttu-id="edf93-211">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="edf93-212">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="edf93-212">AzureRM.Network</span></span>
* <span data-ttu-id="edf93-213">Set-AzureRmLocalNetworkGateway örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-213">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="edf93-214">Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey ve New-AzureRmVirtualNetworkGatewayConnection için örnek ve açıklamalar eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-214">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="edf93-215">Remove-AzureRmVirtualNetworkGatewayIpConfig ve Reset-AzureRmVirtualNetworkGateway örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-215">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="edf93-216">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-216">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="edf93-217">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-217">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="edf93-218">Set-AzureRmVirtualNetworkGatewayConnection örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-218">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="edf93-219">ApplicationSecurityGroup, RouteTable ve Usage için en son kod oluşturucu kullanılarak cmdlet’ler yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="edf93-219">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="edf93-220">Varolmayan bir alt ağ alma girişiminde bulunulduğunda Get-AzureRmVirtualNetworkSubnetConfig cmdlet'inin hata iletisi netleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-220">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="edf93-221">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="edf93-221">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="edf93-222">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-222">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="edf93-223">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="edf93-223">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="edf93-224">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="edf93-225">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="edf93-225">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="edf93-226">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="edf93-227">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="edf93-227">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="edf93-228">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="edf93-229">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="edf93-229">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="edf93-230">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="edf93-231">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="edf93-231">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="edf93-232">Get-AzureRmRecoveryServicesBackItem cmdlet’ine ilke filtresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-232">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="edf93-233">Komut, verilen ilke kimliği tarafından korunan yedekleme öğelerinin listesini döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="edf93-233">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="edf93-234">Microsoft.Azure.Management.RecoveryServices.Backup, sürüm 3.0.0 önizlemesine güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-234">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="edf93-235">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-235">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="edf93-236">Restore-AzureRmRecoveryServicesBackupItem’e TargetResourceGroupName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-236">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="edf93-237">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="edf93-237">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="edf93-238">Yönetilen disklerle yapılan VM yedeklemesi için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="edf93-238">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="edf93-239">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="edf93-239">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="edf93-240">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="edf93-241">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="edf93-241">AzureRM.RedisCache</span></span>
* <span data-ttu-id="edf93-242">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="edf93-243">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="edf93-243">AzureRM.Relay</span></span>
* <span data-ttu-id="edf93-244">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="edf93-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="edf93-245">AzureRM.Resources</span></span>
* <span data-ttu-id="edf93-246">Abonelik kapsamındaki şablon dağıtımı destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="edf93-246">Support template deployment at subscription scope.</span></span> <span data-ttu-id="edf93-247">Yeni Cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="edf93-247">Add new Cmdlets:</span></span>
    - <span data-ttu-id="edf93-248">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="edf93-248">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="edf93-249">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="edf93-249">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="edf93-250">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="edf93-250">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="edf93-251">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="edf93-251">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="edf93-252">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="edf93-252">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="edf93-253">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="edf93-253">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="edf93-254">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="edf93-254">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="edf93-255">Set-AzureRmResource’a bağlam geçirilirken hata oluşmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-255">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="edf93-256">New-AzureRmResourceGroupDeployment cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-256">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="edf93-257">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-257">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="edf93-258">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="edf93-258">AzureRM.Scheduler</span></span>
* <span data-ttu-id="edf93-259">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="edf93-260">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="edf93-260">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="edf93-261">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="edf93-262">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="edf93-262">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="edf93-263">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="edf93-264">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="edf93-264">AzureRM.Sql</span></span>
* <span data-ttu-id="edf93-265">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="edf93-266">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="edf93-266">AzureRM.Storage</span></span>
* <span data-ttu-id="edf93-267">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="edf93-268">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="edf93-268">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="edf93-269">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-269">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="edf93-270">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="edf93-270">AzureRM.Tags</span></span>
* <span data-ttu-id="edf93-271">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-271">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="edf93-272">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="edf93-272">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="edf93-273">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-273">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="edf93-274">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="edf93-274">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="edf93-275">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-275">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="edf93-276">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="edf93-276">AzureRM.Websites</span></span>
* <span data-ttu-id="edf93-277">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="edf93-278">6.6.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="edf93-278">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="edf93-279">Genel</span><span class="sxs-lookup"><span data-stu-id="edf93-279">General</span></span>
* <span data-ttu-id="edf93-280">Tüm yardım dosyaları tam parametre türleriyle doğru giriş/çıkış türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-280">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="edf93-281">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="edf93-281">AzureRM.Profile</span></span>
* <span data-ttu-id="edf93-282">Kaynağın geçerli yapılandırmasının hedef kaynakla uyumlu olduğunu doğrulayabilmek için Common.Strategy kitaplığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-282">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="edf93-283">Common.Storage'a ps1xml türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-283">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="edf93-284">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="edf93-284">Azure.Storage</span></span>
* <span data-ttu-id="edf93-285">DefaultProfile’dan Depolama Bağlamı almak için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-285">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="edf93-286">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-286">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="edf93-287">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="edf93-287">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="edf93-288">https://github.com/Azure/azure-powershell/issues/6370 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-288">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="edf93-289">PsApiManagementApi'yi ApiContract'e çevirmek için Automapper hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-289">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="edf93-290">https://github.com/Azure/azure-powershell/issues/6515 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-290">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="edf93-291">Kodlama Türü ile aşırı yüklemeyi önlemek için File.Save hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-291">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="edf93-292">https://github.com/Azure/azure-powershell/issues/6560 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-292">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="edf93-293">apiId üzerindeki desen özel durumunu düzelten 4.0.3 Nuget sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-293">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="edf93-294">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="edf93-294">AzureRM.Compute</span></span>
* <span data-ttu-id="edf93-295">PremiumLRS depolama hesap türü yeniden adlandırması nedeniyle New-AzureRmVm'de DiskFileParameterSet kullanılarak sanal makine oluşturmanın başarısız olmasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-295">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="edf93-296">Invoke-AzureRmVMRunCommand cmdlet'i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-296">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="edf93-297">Abonelikteki tüm kullanılabilir kümelerin listelenebilmesi için Get-AzureRmAvailabilitySet güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-297">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="edf93-298">(ResouceGroupName parametresi artık isteğe bağlı.)</span><span class="sxs-lookup"><span data-stu-id="edf93-298">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="edf93-299">Uygun sanal makinelerde Hızlandırılmış Ağı etkinleştirmek için 'New-AzureRmVm' cmdlet'inin SimpleParameterSet öğesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-299">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="edf93-300">Kullanıcının belirttiği LB zaten mevcut olduğunda vmss oluşturmanın başarısız olması için New-AzureRmVmss basit parametre kümesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-300">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="edf93-301">New-AzureRmDisk örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-301">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="edf93-302">'New-AzureRmVM' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-302">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="edf93-303">Set-AzureRmVMOSDisk açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-303">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="edf93-304">Yazımı ve ön eki düzeltmek amacıyla Set-AzureRmVMBginfoExtension için Örnek 1 güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-304">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="edf93-305">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="edf93-305">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="edf93-306">ADF .Net SDK sürümü 1.1.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-306">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="edf93-307">Veri fabrikaları arasında paylaşılan şirket içinde barındırılan tümleştirme çalışma zamanı desteği.</span><span class="sxs-lookup"><span data-stu-id="edf93-307">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="edf93-308">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine yeni -SharedIntegrationRuntimeResourceId parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-308">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="edf93-309">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine isteğe bağlı yeni -LinkedDataFactoryName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-309">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="edf93-310">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="edf93-310">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="edf93-311">DataPlane SDK'sı (Microsoft.Azure.DataLake.Store) sürümü 1.1.9'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-311">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="edf93-312">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="edf93-312">AzureRM.EventHub</span></span>
* <span data-ttu-id="edf93-313">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-313">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="edf93-314">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="edf93-314">AzureRM.Insights</span></span>
* <span data-ttu-id="edf93-315">Yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-315">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="edf93-316">Microsoft.Azure.Management.Monitor SDK 0.19.1-preview kullanımı</span><span class="sxs-lookup"><span data-stu-id="edf93-316">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="edf93-317">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="edf93-317">AzureRM.KeyVault</span></span>
* <span data-ttu-id="edf93-318">Set-AzureRmKeyVaultAccessPolicy'de yönlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-318">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="edf93-319">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="edf93-319">AzureRM.Network</span></span>
* <span data-ttu-id="edf93-320">LoadBalancerInboundNatPoolConfig cmdlet'leri için örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-320">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="edf93-321">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="edf93-321">AzureRM.Resources</span></span>
* <span data-ttu-id="edf93-322">'Get-AzureRmResource' için hem etiket adı hem de değer sağlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-322">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="edf93-323">'Set-AzureRmResource' için yönlendirme senaryosu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-323">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="edf93-324">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="edf93-324">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="edf93-325">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-325">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="edf93-326">birkaç sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-326">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="edf93-327">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="edf93-327">AzureRM.Sql</span></span>
* <span data-ttu-id="edf93-328">Aşağıdaki cmdlet'lere Sunucu Gelişmiş Tehdit Koruması desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="edf93-328">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="edf93-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="edf93-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="edf93-330">Aşağıdaki cmdlet'lere Güvenlik Açığı Değerlendirme desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="edf93-330">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="edf93-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="edf93-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="edf93-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="edf93-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="edf93-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="edf93-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="edf93-334">Remove-AzureRmSqlServerFirewallRulecmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-334">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="edf93-335">Get-AzureSqlSyncGroupLog içinde ABD temelli olmayan kültürde yanlış tarih saat işlemesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-335">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="edf93-336">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="edf93-336">AzureRM.Storage</span></span>
* <span data-ttu-id="edf93-337">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-337">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="edf93-338">Tablo görünümünde StorageAccount cmdlet'i çıkışı gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="edf93-338">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="edf93-339">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edf93-339">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="edf93-340">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edf93-340">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="edf93-341">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edf93-341">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="edf93-342">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="edf93-342">AzureRM.Tags</span></span>
* <span data-ttu-id="edf93-343">Tag cmdlet'inin yardımında hatayı deyim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="edf93-343">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="edf93-344">6.5.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="edf93-344">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="edf93-345">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="edf93-345">AzureRM.Profile</span></span>
* <span data-ttu-id="edf93-346">'Get-AzureRmContextAutosaveSetting' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-346">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="edf93-347">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="edf93-347">Azure.Storage</span></span>
* <span data-ttu-id="edf93-348">Salt yazılır Sas belirteciyle Karşıya Yükleme Blobu veya Dosyası desteği</span><span class="sxs-lookup"><span data-stu-id="edf93-348">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="edf93-349">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="edf93-349">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="edf93-350">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="edf93-350">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="edf93-351">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="edf93-351">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="edf93-352">AS'ye gerekli ResourceGroupName özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-352">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="edf93-353">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="edf93-353">AzureRM.Automation</span></span>
* <span data-ttu-id="edf93-354">'New-AzureRMAutomationSchedule' için yardım güncelleştirildi ve örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-354">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="edf93-355">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="edf93-355">AzureRM.Compute</span></span>
* <span data-ttu-id="edf93-356">Update/New-AzureRmAvailabilitySet komutlarına -Tag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-356">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="edf93-357">'Add-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-357">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="edf93-358">'Remove-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-358">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="edf93-359">'Set-AzureRmVMAccessExtension' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-359">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="edf93-360">New-AzureRmVmss için SimpleParameterSet güncelleştirilerek SinglePlacementGroup varsayılan olarak false değerine ayarlandı ve kullanıcının tek yerleşim grubunda VMSS oluşturmasına olanak tanıyan 'SinglePlacementGroup' geçiş parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-360">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="edf93-361">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="edf93-361">AzureRM.EventHub</span></span>
* <span data-ttu-id="edf93-362">PSEventHubDRConfigurationAttributes sınıfına, çoğaltma işlemi devam ederken bekleyen çoğaltma işlemlerinin sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-362">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="edf93-363">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="edf93-363">AzureRM.KeyVault</span></span>
* <span data-ttu-id="edf93-364">Set-AzureRmKeyVaultAccessPolicy için hata iletisi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-364">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="edf93-365">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="edf93-365">AzureRM.LogicApp</span></span>
* <span data-ttu-id="edf93-366">New-AzureRmLogicApp’te "parametre kümesi çözümlenemedi" hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-366">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="edf93-367">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="edf93-367">AzureRM.Network</span></span>
* <span data-ttu-id="edf93-368">Set/Add-AzureRmVirtualNetworkPeering için birden çok Kiracıdaki Sanal Makineler arasında eşleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-368">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="edf93-369">Aşağıdaki cmdlet’ler Application Gateway için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-369">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="edf93-370">New-AzureRmApplicationGateway : EnableFIPS bayrağı ve Zones desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-370">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="edf93-371">New-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-371">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="edf93-372">Set-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-372">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="edf93-373">RouteTable cmdlet’leri en son oluşturucu sürümüyle yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="edf93-373">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="edf93-374">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="edf93-374">AzureRM.Relay</span></span>
* <span data-ttu-id="edf93-375">Markdown dosyaları güncelleştirildi, örnekteki parametre adı sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="edf93-375">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="edf93-376">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="edf93-376">AzureRM.Resources</span></span>
* <span data-ttu-id="edf93-377">Roleassignment ve roledefinition cmdlet’leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="edf93-377">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="edf93-378">Disk belleğinin parçası olarak yapılan ek roledefinition çağrıları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="edf93-378">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="edf93-379">Get-AzureRmRoleAssignment cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-379">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="edf93-380">-ExpandPrincipalGroups komut parametresi işlevselliği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-380">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="edf93-381">'-ResourceType' parametresinin büyük/küçük harfe duyarlı olduğu 'Get-AzureRmResource' sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-381">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="edf93-382">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="edf93-382">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="edf93-383">Liste cmdlet’lerine top ve skip parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-383">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="edf93-384">Standard'dan Premium NameSpace'e geçiş cmdlet’leri eklendi :</span><span class="sxs-lookup"><span data-stu-id="edf93-384">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="edf93-385">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="edf93-385">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="edf93-386">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="edf93-386">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="edf93-387">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="edf93-387">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="edf93-388">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="edf93-388">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="edf93-389">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="edf93-389">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="edf93-390">PSServiceBusDRConfigurationAttributes sınıfına, çoğaltma işlemi sürerken beklemede olan çoğaltma işlemi sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-390">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="edf93-391">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="edf93-391">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="edf93-392">'New-AzureRmServiceFabricCluster' için örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-392">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="edf93-393">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="edf93-393">AzureRM.Sql</span></span>
* <span data-ttu-id="edf93-394">Müşterilerin Sql Server örneğine veya Yönetilen Örneğe TDE Sertifikası ekleyebilmeleri için yeni Management.Sql Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-394">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="edf93-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="edf93-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="edf93-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="edf93-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="edf93-397">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="edf93-397">AzureRM.Websites</span></span>
* <span data-ttu-id="edf93-398">Artık `Set-AzureRmWebApp -AssignIdentity` ve `Set-AzureRmWebAppSlot -AssignIdentity` false olarak ayarlandığında site object.Removing önizleme etiketinden Identity özelliğini kaldırıyor.</span><span class="sxs-lookup"><span data-stu-id="edf93-398">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="edf93-399">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-399">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="edf93-400">`Set-AzureRmWebApp -PhpVersion` geçerli bir php sürümü off değerini destekliyor</span><span class="sxs-lookup"><span data-stu-id="edf93-400">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="edf93-401">6.4.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="edf93-401">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="edf93-402">Genel</span><span class="sxs-lookup"><span data-stu-id="edf93-402">General</span></span>
* <span data-ttu-id="edf93-403">Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-403">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="edf93-404">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="edf93-404">AzureRM.Profile</span></span>
* <span data-ttu-id="edf93-405">Temel çıkış türlerine Ps1Xml özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-405">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="edf93-406">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="edf93-406">AzureRM.Compute</span></span>
* <span data-ttu-id="edf93-407">VMSS için IP Etiketi özelliği</span><span class="sxs-lookup"><span data-stu-id="edf93-407">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="edf93-408">'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-408">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="edf93-409">New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-409">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="edf93-410">VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-410">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="edf93-411">New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-411">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="edf93-412">VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği</span><span class="sxs-lookup"><span data-stu-id="edf93-412">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="edf93-413">Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-413">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="edf93-414">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="edf93-414">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="edf93-415">Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:</span><span class="sxs-lookup"><span data-stu-id="edf93-415">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="edf93-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="edf93-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="edf93-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="edf93-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="edf93-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="edf93-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="edf93-419">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="edf93-419">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="edf93-420">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-420">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="edf93-421">Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-421">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="edf93-422">Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-422">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="edf93-423">DataLake cmdlet'lerinin test konumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-423">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="edf93-424">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="edf93-424">AzureRM.EventHub</span></span>
* <span data-ttu-id="edf93-425">Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-425">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="edf93-426">New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-426">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="edf93-427">Varsayılan Parametre kümesi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="edf93-427">Provided Default Parameter set.</span></span>
* <span data-ttu-id="edf93-428">Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-428">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="edf93-429">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="edf93-429">AzureRM.KeyVault</span></span>
* <span data-ttu-id="edf93-430">Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-430">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="edf93-431">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="edf93-431">AzureRM.Network</span></span>
* <span data-ttu-id="edf93-432">Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="edf93-432">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="edf93-433">ARM aracılığıyla ExpressRoute Partner API'leri özelliği için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-433">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="edf93-434">Get-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-434">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="edf93-435">Set-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-435">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="edf93-436">Add-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-436">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="edf93-437">Get-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-437">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="edf93-438">Remove-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-438">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="edf93-439">Get-AzureRMExpressRouteCrossConnectionArpTable eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-439">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="edf93-440">Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-440">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="edf93-441">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-441">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="edf93-442">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="edf93-442">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="edf93-443">Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-443">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="edf93-444">Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="edf93-444">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="edf93-445">Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edf93-445">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="edf93-446">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="edf93-446">AzureRM.Resources</span></span>
* <span data-ttu-id="edf93-447">Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="edf93-447">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="edf93-448">Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-448">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="edf93-449">Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-449">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="edf93-450">control parametresine -Effective ve -All anahtarları eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-450">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="edf93-451">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-451">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="edf93-452">Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-452">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="edf93-453">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-453">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="edf93-454">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-454">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="edf93-455">Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-455">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="edf93-456">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-456">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="edf93-457">'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-457">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="edf93-458">'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-458">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="edf93-459">'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-459">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="edf93-460">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="edf93-460">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="edf93-461">Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-461">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="edf93-462">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="edf93-462">AzureRM.Sql</span></span>
* <span data-ttu-id="edf93-463">New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-463">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="edf93-464">Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-464">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="edf93-465">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="edf93-465">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="edf93-466">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="edf93-466">AzureRM.Profile</span></span>
* <span data-ttu-id="edf93-467">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-467">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="edf93-468">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="edf93-468">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="edf93-469">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="edf93-469">Azure.Storage</span></span>
* <span data-ttu-id="edf93-470">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-470">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="edf93-471">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="edf93-471">AzureRM.Compute</span></span>
* <span data-ttu-id="edf93-472">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-472">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="edf93-473">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-473">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="edf93-474">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="edf93-474">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="edf93-475">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="edf93-475">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="edf93-476">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="edf93-476">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="edf93-477">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="edf93-477">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="edf93-478">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="edf93-478">Start-AzureRmVM</span></span>
    - <span data-ttu-id="edf93-479">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="edf93-479">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="edf93-480">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="edf93-480">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="edf93-481">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="edf93-481">Set-AzureRmVM</span></span>
    - <span data-ttu-id="edf93-482">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="edf93-482">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="edf93-483">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="edf93-483">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="edf93-484">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="edf93-484">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="edf93-485">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="edf93-485">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="edf93-486">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="edf93-486">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="edf93-487">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="edf93-487">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="edf93-488">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="edf93-488">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="edf93-489">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="edf93-489">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="edf93-490">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="edf93-490">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="edf93-491">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="edf93-491">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="edf93-492">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="edf93-492">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="edf93-493">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="edf93-493">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="edf93-494">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="edf93-494">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="edf93-495">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="edf93-495">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="edf93-496">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="edf93-496">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="edf93-497">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="edf93-497">AzureRM.EventGrid</span></span>
* <span data-ttu-id="edf93-498">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="edf93-498">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="edf93-499">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="edf93-499">AzureRM.KeyVault</span></span>
* <span data-ttu-id="edf93-500">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-500">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="edf93-501">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="edf93-501">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="edf93-502">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="edf93-502">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="edf93-503">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="edf93-503">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="edf93-504">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-504">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="edf93-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="edf93-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="edf93-506">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-506">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="edf93-507">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="edf93-507">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="edf93-508">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="edf93-508">AzureRM.Sql</span></span>
* <span data-ttu-id="edf93-509">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-509">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="edf93-510">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="edf93-510">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="edf93-511">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-511">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="edf93-512">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="edf93-512">AzureRM.Websites</span></span>
* <span data-ttu-id="edf93-513">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-513">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="edf93-514">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-514">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="edf93-515">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="edf93-515">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="edf93-516">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="edf93-516">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="edf93-517">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-517">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="edf93-518">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="edf93-518">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="edf93-519">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="edf93-519">AzureRM.Profile</span></span>
* <span data-ttu-id="edf93-520">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-520">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="edf93-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="edf93-521">AzureRM.Compute</span></span>
* <span data-ttu-id="edf93-522">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="edf93-522">VMSS VM Update feature</span></span>
    - <span data-ttu-id="edf93-523">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-523">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="edf93-524">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-524">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="edf93-525">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="edf93-525">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="edf93-526">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="edf93-526">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="edf93-527">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-527">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="edf93-528">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-528">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="edf93-529">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-529">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="edf93-530">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-530">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="edf93-531">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="edf93-531">AzureRM.KeyVault</span></span>
* <span data-ttu-id="edf93-532">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-532">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="edf93-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="edf93-533">AzureRM.Network</span></span>
* <span data-ttu-id="edf93-534">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-534">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="edf93-535">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="edf93-535">AzureRM.Resources</span></span>
* <span data-ttu-id="edf93-536">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-536">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="edf93-537">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="edf93-537">AzureRM.Scheduler</span></span>
* <span data-ttu-id="edf93-538">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-538">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="edf93-539">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="edf93-539">AzureRM.Sql</span></span>
* <span data-ttu-id="edf93-540">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="edf93-540">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="edf93-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="edf93-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="edf93-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="edf93-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="edf93-543">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="edf93-543">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="edf93-544">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="edf93-544">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="edf93-545">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="edf93-545">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="edf93-546">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="edf93-546">AzureRM.Websites</span></span>
* <span data-ttu-id="edf93-547">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-547">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="edf93-548">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="edf93-548">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="edf93-549">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="edf93-549">AzureRM.Profile</span></span>
* <span data-ttu-id="edf93-550">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="edf93-550">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="edf93-551">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="edf93-551">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="edf93-552">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="edf93-552">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="edf93-553">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="edf93-553">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="edf93-554">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-554">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="edf93-555">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-555">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="edf93-556">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-556">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="edf93-557">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-557">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="edf93-558">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-558">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="edf93-559">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-559">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="edf93-560">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-560">Added support for MSI identity</span></span>
* <span data-ttu-id="edf93-561">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="edf93-561">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="edf93-562">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="edf93-562">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="edf93-563">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="edf93-563">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="edf93-564">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="edf93-564">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="edf93-565">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="edf93-565">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="edf93-566">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="edf93-566">AzureRM.Batch</span></span>
* <span data-ttu-id="edf93-567">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="edf93-567">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="edf93-568">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="edf93-568">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="edf93-569">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="edf93-569">AzureRM.Consumption</span></span>
* <span data-ttu-id="edf93-570">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="edf93-570">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="edf93-571">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="edf93-571">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="edf93-572">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="edf93-572">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="edf93-573">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="edf93-573">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="edf93-574">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="edf93-574">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="edf93-575">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="edf93-575">AzureRM.Network</span></span>
* <span data-ttu-id="edf93-576">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="edf93-576">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="edf93-577">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-577">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="edf93-578">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="edf93-578">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="edf93-579">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-579">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="edf93-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="edf93-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="edf93-581">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="edf93-581">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="edf93-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="edf93-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="edf93-583">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="edf93-583">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="edf93-584">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="edf93-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="edf93-585">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="edf93-585">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="edf93-586">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="edf93-586">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="edf93-587">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="edf93-587">AzureRM.Sql</span></span>
* <span data-ttu-id="edf93-588">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="edf93-588">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="edf93-589">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="edf93-589">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="edf93-590">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="edf93-590">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="edf93-591">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="edf93-591">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="edf93-592">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="edf93-592">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="edf93-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="edf93-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="edf93-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="edf93-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="edf93-595">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="edf93-595">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="edf93-596">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="edf93-596">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="edf93-597">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="edf93-597">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="edf93-598">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="edf93-598">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="edf93-599">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="edf93-599">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
