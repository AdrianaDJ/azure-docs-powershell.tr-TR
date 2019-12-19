---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: f77d901169b0d98b2425a2e50d33a1789150b770
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182562"
---
## <a name="320---december-2019"></a><span data-ttu-id="8e343-103">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-103">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="8e343-104">Genel</span><span class="sxs-lookup"><span data-stu-id="8e343-104">General</span></span>
* <span data-ttu-id="8e343-105">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-105">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8e343-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-106">Az.Accounts</span></span>
* <span data-ttu-id="8e343-107">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="8e343-107">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="8e343-108">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="8e343-108">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8e343-109">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8e343-109">Az.Batch</span></span>
* <span data-ttu-id="8e343-110">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-110">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8e343-111">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e343-111">Az.DataFactory</span></span>
* <span data-ttu-id="8e343-112">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-112">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8e343-113">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8e343-113">Az.FrontDoor</span></span>
* <span data-ttu-id="8e343-114">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-114">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="8e343-115">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-115">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8e343-116">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8e343-116">Az.HealthcareApis</span></span>
* <span data-ttu-id="8e343-117">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="8e343-117">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8e343-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e343-118">Az.KeyVault</span></span>
* <span data-ttu-id="8e343-119">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-119">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="8e343-120">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="8e343-120">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="8e343-121">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-121">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8e343-122">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8e343-122">Az.Monitor</span></span>
* <span data-ttu-id="8e343-123">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-123">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="8e343-124">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="8e343-124">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="8e343-125">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="8e343-125">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-126">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-126">Az.Network</span></span>
* <span data-ttu-id="8e343-127">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-127">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-128">Az.Resources</span></span>
* <span data-ttu-id="8e343-129">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-129">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="8e343-130">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-130">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-131">Az.Sql</span></span>
* <span data-ttu-id="8e343-132">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-132">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-133">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-133">Az.Storage</span></span>
* <span data-ttu-id="8e343-134">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="8e343-134">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="8e343-135">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="8e343-135">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="8e343-136">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8e343-136">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="8e343-137">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="8e343-137">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="8e343-138">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="8e343-138">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="8e343-139">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-139">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="8e343-140">Yönetim düzlemi Dosya paylaşımı cmdlet’lerinde 5120’den yüksek Paylaşım QuotaGiB değeri desteği ve 'QuotaGiB' parametresine 'Quota' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-140">Support Share QuotaGiB more than 5120 in Management plane File Share cmdlets, and add parameter alias 'Quota' to parameter 'QuotaGiB'</span></span> 
    - <span data-ttu-id="8e343-141">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8e343-141">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="8e343-142">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8e343-142">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="8e343-143">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-143">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="8e343-144">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="8e343-144">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="8e343-145">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-145">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="8e343-146">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="8e343-146">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="8e343-147">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-147">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8e343-148">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="8e343-148">Highlights since the last major release</span></span>
* <span data-ttu-id="8e343-149">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="8e343-149">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="8e343-150">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="8e343-150">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-151">Az.Compute</span></span>
* <span data-ttu-id="8e343-152">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="8e343-152">VM Reapply feature</span></span>
    - <span data-ttu-id="8e343-153">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="8e343-153">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="8e343-154">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="8e343-154">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="8e343-155">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8e343-155">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="8e343-156">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="8e343-156">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="8e343-157">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-157">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8e343-158">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-158">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="8e343-159">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-159">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="8e343-160">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-160">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="8e343-161">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-161">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="8e343-162">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-162">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="8e343-163">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8e343-163">Az.DataBoxEdge</span></span>
* <span data-ttu-id="8e343-164">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-164">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8e343-165">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="8e343-165">Get the Order</span></span>
* <span data-ttu-id="8e343-166">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-166">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8e343-167">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="8e343-167">Create new Order</span></span>
* <span data-ttu-id="8e343-168">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-168">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8e343-169">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="8e343-169">Remove the Order</span></span>
* <span data-ttu-id="8e343-170">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="8e343-170">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="8e343-171">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="8e343-171">Now creates Local Share</span></span>
* <span data-ttu-id="8e343-172">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-172">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="8e343-173">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="8e343-173">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="8e343-174">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-174">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="8e343-175">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="8e343-175">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="8e343-176">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-176">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8e343-177">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="8e343-177">Gets the information about Triggers</span></span>
* <span data-ttu-id="8e343-178">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-178">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8e343-179">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="8e343-179">Create new Triggers</span></span>
* <span data-ttu-id="8e343-180">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-180">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8e343-181">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="8e343-181">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8e343-182">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e343-182">Az.DataFactory</span></span>
* <span data-ttu-id="8e343-183">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-183">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="8e343-184">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-184">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8e343-185">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-185">Az.DataLakeStore</span></span>
* <span data-ttu-id="8e343-186">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-186">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8e343-187">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8e343-187">Az.EventHub</span></span>
* <span data-ttu-id="8e343-188">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-188">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8e343-189">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8e343-189">Az.FrontDoor</span></span>
* <span data-ttu-id="8e343-190">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-190">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="8e343-191">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-191">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="8e343-192">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-192">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="8e343-193">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="8e343-193">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-194">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-194">Az.Network</span></span>
* <span data-ttu-id="8e343-195">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-195">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="8e343-196">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="8e343-196">Az.PrivateDns</span></span>
* <span data-ttu-id="8e343-197">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-197">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-198">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-198">Az.RecoveryServices</span></span>
* <span data-ttu-id="8e343-199">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-199">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="8e343-200">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="8e343-200">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="8e343-201">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-201">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8e343-202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8e343-202">Az.RedisCache</span></span>
* <span data-ttu-id="8e343-203">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-203">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="8e343-204">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-204">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="8e343-205">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-205">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-206">Az.Resources</span></span>
- <span data-ttu-id="8e343-207">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-207">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="8e343-208">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-208">Updated create policy definition help example</span></span>
- <span data-ttu-id="8e343-209">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-209">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="8e343-210">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-210">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="8e343-211">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-211">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-212">Az.Sql</span></span>
* <span data-ttu-id="8e343-213">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-213">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="8e343-214">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-214">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="8e343-215">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-215">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="8e343-216">Genel</span><span class="sxs-lookup"><span data-stu-id="8e343-216">General</span></span>
* <span data-ttu-id="8e343-217">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="8e343-217">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8e343-218">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-218">Az.Accounts</span></span>
* <span data-ttu-id="8e343-219">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8e343-219">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8e343-220">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8e343-220">Az.Advisor</span></span>
* <span data-ttu-id="8e343-221">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-221">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8e343-222">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8e343-222">Az.Batch</span></span>
* <span data-ttu-id="8e343-223">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-223">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="8e343-224">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="8e343-224">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="8e343-225">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-225">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="8e343-226">**New-AzBatchTask** `-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet'i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-226">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="8e343-227">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="8e343-227">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="8e343-228">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="8e343-228">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="8e343-229">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="8e343-229">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="8e343-230">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-230">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="8e343-231">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-231">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="8e343-232">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-232">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="8e343-233">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="8e343-233">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="8e343-234">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="8e343-234">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="8e343-235">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-235">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="8e343-236">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="8e343-236">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="8e343-237">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-237">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="8e343-238">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-238">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="8e343-239">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-239">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="8e343-240">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-240">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="8e343-241">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-241">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="8e343-242">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-242">This operation is no longer supported.</span></span>
* <span data-ttu-id="8e343-243">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-243">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="8e343-244">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-244">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="8e343-245">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-245">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="8e343-246">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-246">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="8e343-247">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-247">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="8e343-248">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-248">New non-verified images are also now returned.</span></span> <span data-ttu-id="8e343-249">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-249">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="8e343-250">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-250">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="8e343-251">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-251">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="8e343-252">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-252">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="8e343-253">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-253">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="8e343-254">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-254">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="8e343-255">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-255">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="8e343-256">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-256">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="8e343-257">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="8e343-257">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="8e343-258">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="8e343-258">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8e343-259">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8e343-259">Az.Cdn</span></span>
* <span data-ttu-id="8e343-260">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-260">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="8e343-261">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-261">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-262">Az.Compute</span></span>
* <span data-ttu-id="8e343-263">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="8e343-263">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="8e343-264">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="8e343-264">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="8e343-265">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="8e343-265">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="8e343-266">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8e343-266">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="8e343-267">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-267">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8e343-268">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-268">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="8e343-269">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="8e343-269">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="8e343-270">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-270">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="8e343-271">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="8e343-271">Breaking changes</span></span>
    - <span data-ttu-id="8e343-272">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="8e343-272">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="8e343-273">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="8e343-273">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8e343-274">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e343-274">Az.DataFactory</span></span>
* <span data-ttu-id="8e343-275">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-275">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8e343-276">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-276">Az.DataLakeStore</span></span>
* <span data-ttu-id="8e343-277">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="8e343-277">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="8e343-278">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="8e343-278">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="8e343-279">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="8e343-279">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="8e343-280">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="8e343-280">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="8e343-281">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="8e343-281">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="8e343-282">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="8e343-282">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8e343-283">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8e343-283">Az.FrontDoor</span></span>
* <span data-ttu-id="8e343-284">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-284">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8e343-285">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8e343-285">Az.HDInsight</span></span>
* <span data-ttu-id="8e343-286">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-286">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="8e343-287">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-287">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="8e343-288">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-288">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="8e343-289">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="8e343-289">Removed five cmdlets:</span></span>
    - <span data-ttu-id="8e343-290">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8e343-290">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8e343-291">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8e343-291">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8e343-292">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8e343-292">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8e343-293">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8e343-293">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="8e343-294">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8e343-294">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="8e343-295">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="8e343-295">Added three cmdlets:</span></span>
    - <span data-ttu-id="8e343-296">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="8e343-296">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="8e343-297">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="8e343-297">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="8e343-298">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="8e343-298">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="8e343-299">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-299">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="8e343-300">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-300">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="8e343-301">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-301">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="8e343-302">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-302">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="8e343-303">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-303">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="8e343-304">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-304">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="8e343-305">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-305">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="8e343-306">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-306">Added some scenario test cases.</span></span>
* <span data-ttu-id="8e343-307">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="8e343-307">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8e343-308">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8e343-308">Az.IotHub</span></span>
* <span data-ttu-id="8e343-309">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="8e343-309">Breaking changes:</span></span>
    - <span data-ttu-id="8e343-310">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="8e343-310">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8e343-311">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-311">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8e343-312">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="8e343-312">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8e343-313">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-313">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8e343-314">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-314">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="8e343-315">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-315">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="8e343-316">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-316">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="8e343-317">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-317">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="8e343-318">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="8e343-318">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8e343-319">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-319">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8e343-320">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="8e343-320">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8e343-321">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-321">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-322">Az.RecoveryServices</span></span>
* <span data-ttu-id="8e343-323">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-323">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="8e343-324">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-324">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="8e343-325">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-325">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="8e343-326">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-326">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="8e343-327">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-327">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="8e343-328">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-328">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="8e343-329">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-329">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="8e343-330">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-330">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="8e343-331">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-331">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-332">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-332">Az.Resources</span></span>
* <span data-ttu-id="8e343-333">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-333">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-334">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-334">Az.Network</span></span>
* <span data-ttu-id="8e343-335">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-335">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="8e343-336">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-336">Updated cmdlet:</span></span>
        - <span data-ttu-id="8e343-337">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-337">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8e343-338">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-338">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8e343-339">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-339">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8e343-340">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-340">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8e343-341">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-341">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8e343-342">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-342">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="8e343-343">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8e343-343">New cmdlet:</span></span>
        - <span data-ttu-id="8e343-344">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="8e343-344">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="8e343-345">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-345">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="8e343-346">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-346">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="8e343-347">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-347">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="8e343-348">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-348">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="8e343-349">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-349">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="8e343-350">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-350">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="8e343-351">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-351">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="8e343-352">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8e343-352">New cmdlets added:</span></span>
        - <span data-ttu-id="8e343-353">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8e343-353">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="8e343-354">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e343-354">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8e343-355">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e343-355">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8e343-356">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e343-356">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8e343-357">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8e343-357">Set-AzVirtualHub</span></span>
* <span data-ttu-id="8e343-358">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-358">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="8e343-359">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-359">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8e343-360">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-360">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="8e343-361">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-361">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="8e343-362">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-362">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="8e343-363">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-363">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="8e343-364">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-364">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="8e343-365">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8e343-365">New cmdlets added:</span></span>
        - <span data-ttu-id="8e343-366">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-366">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="8e343-367">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-367">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8e343-368">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-368">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8e343-369">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-369">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8e343-370">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-370">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8e343-371">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-371">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8e343-372">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-372">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="8e343-373">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-373">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="8e343-374">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8e343-374">New cmdlets added:</span></span>
        - <span data-ttu-id="8e343-375">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="8e343-375">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="8e343-376">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="8e343-376">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="8e343-377">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="8e343-377">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="8e343-378">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="8e343-378">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="8e343-379">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="8e343-379">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="8e343-380">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e343-380">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="8e343-381">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8e343-382">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-382">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="8e343-383">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-383">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="8e343-384">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-384">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="8e343-385">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-385">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="8e343-386">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8e343-387">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-387">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="8e343-388">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-388">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="8e343-389">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-389">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="8e343-390">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="8e343-390">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="8e343-391">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-391">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="8e343-392">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8e343-392">New cmdlets added:</span></span>
        - <span data-ttu-id="8e343-393">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8e343-393">New-AzIpGroup</span></span>
        - <span data-ttu-id="8e343-394">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8e343-394">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="8e343-395">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8e343-395">Get-AzIpGroup</span></span>
        - <span data-ttu-id="8e343-396">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8e343-396">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8e343-397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e343-397">Az.ServiceFabric</span></span>
* <span data-ttu-id="8e343-398">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-398">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-399">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-399">Az.Sql</span></span>
* <span data-ttu-id="8e343-400">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-400">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="8e343-401">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-401">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="8e343-402">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="8e343-402">Removed deprecated aliases:</span></span>
* <span data-ttu-id="8e343-403">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="8e343-403">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="8e343-404">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="8e343-404">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="8e343-405">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-405">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8e343-406">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-406">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="8e343-407">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-407">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="8e343-408">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-408">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-409">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-409">Az.Storage</span></span>
* <span data-ttu-id="8e343-410">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="8e343-410">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="8e343-411">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-411">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8e343-412">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-412">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8e343-413">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="8e343-413">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="8e343-414">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8e343-414">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="8e343-415">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8e343-415">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="8e343-416">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-416">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="8e343-417">Genel</span><span class="sxs-lookup"><span data-stu-id="8e343-417">General</span></span>
* <span data-ttu-id="8e343-418">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="8e343-418">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8e343-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-419">Az.Accounts</span></span>
* <span data-ttu-id="8e343-420">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-420">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8e343-421">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e343-421">Az.ApiManagement</span></span>
* <span data-ttu-id="8e343-422">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-422">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="8e343-423">https://github.com/Azure/azure-powershell/issues/10068 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-423">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8e343-424">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8e343-424">Az.Automation</span></span>
* <span data-ttu-id="8e343-425">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-425">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="8e343-426">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8e343-426">Az.Batch</span></span>
* <span data-ttu-id="8e343-427">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="8e343-427">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-428">Az.Compute</span></span>
* <span data-ttu-id="8e343-429">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-429">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8e343-430">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-430">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="8e343-431">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-431">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="8e343-432">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-432">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8e343-433">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e343-433">Az.DataFactory</span></span>
* <span data-ttu-id="8e343-434">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="8e343-434">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="8e343-435">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="8e343-435">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="8e343-436">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-436">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8e343-437">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-437">Az.DataLakeStore</span></span>
* <span data-ttu-id="8e343-438">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-438">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8e343-439">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8e343-439">Az.HealthcareApis</span></span>
* <span data-ttu-id="8e343-440">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-440">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="8e343-441">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-441">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="8e343-442">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-442">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="8e343-443">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-443">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8e343-444">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8e343-444">Az.IotHub</span></span>
* <span data-ttu-id="8e343-445">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="8e343-445">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="8e343-446">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="8e343-446">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="8e343-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8e343-447">Az.Monitor</span></span>
* <span data-ttu-id="8e343-448">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-448">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="8e343-449">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="8e343-449">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="8e343-450">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="8e343-450">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="8e343-451">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-451">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-452">Az.Network</span></span>
* <span data-ttu-id="8e343-453">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-453">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="8e343-454">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-454">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="8e343-455">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8e343-455">New cmdlets added:</span></span>
        - <span data-ttu-id="8e343-456">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="8e343-456">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="8e343-457">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-457">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8e343-458">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-458">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="8e343-459">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-459">Updated cmdlets:</span></span>
        - <span data-ttu-id="8e343-460">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-460">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8e343-461">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-461">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8e343-462">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-462">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8e343-463">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-463">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="8e343-464">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="8e343-464">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="8e343-465">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="8e343-465">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="8e343-466">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="8e343-466">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8e343-467">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8e343-467">Az.RedisCache</span></span>
* <span data-ttu-id="8e343-468">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-468">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-469">Az.Sql</span></span>
* <span data-ttu-id="8e343-470">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-470">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-471">Az.Storage</span></span>
* <span data-ttu-id="8e343-472">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-472">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="8e343-473">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="8e343-473">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8e343-474">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8e343-474">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="8e343-475">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="8e343-475">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8e343-476">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-476">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8e343-477">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8e343-477">Az.StorageSync</span></span>
* <span data-ttu-id="8e343-478">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-478">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-479">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-479">Az.Websites</span></span>
* <span data-ttu-id="8e343-480">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="8e343-480">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="8e343-481">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-481">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8e343-482">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e343-482">Az.ApiManagement</span></span>
* <span data-ttu-id="8e343-483">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-483">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="8e343-484">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-484">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="8e343-485">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="8e343-485">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8e343-486">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8e343-486">Az.Automation</span></span>
* <span data-ttu-id="8e343-487">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-487">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="8e343-488">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-488">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="8e343-489">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-489">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-490">Az.Compute</span></span>
* <span data-ttu-id="8e343-491">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-491">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="8e343-492">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-492">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8e343-493">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="8e343-493">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="8e343-494">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-494">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="8e343-495">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-495">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="8e343-496">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-496">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="8e343-497">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-497">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="8e343-498">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-498">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="8e343-499">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-499">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8e343-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e343-500">Az.DataFactory</span></span>
* <span data-ttu-id="8e343-501">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="8e343-501">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="8e343-502">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-502">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8e343-503">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8e343-503">Az.HDInsight</span></span>
* <span data-ttu-id="8e343-504">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="8e343-504">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8e343-505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8e343-505">Az.IotHub</span></span>
* <span data-ttu-id="8e343-506">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-506">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="8e343-507">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-507">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="8e343-508">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8e343-508">New cmdlets are:</span></span>
    - <span data-ttu-id="8e343-509">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8e343-509">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8e343-510">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8e343-510">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8e343-511">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8e343-511">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8e343-512">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8e343-512">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8e343-513">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8e343-513">Az.Monitor</span></span>
* <span data-ttu-id="8e343-514">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="8e343-514">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="8e343-515">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="8e343-515">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="8e343-516">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="8e343-516">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="8e343-517">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="8e343-517">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="8e343-518">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-518">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="8e343-519">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-519">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="8e343-520">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="8e343-520">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="8e343-521">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="8e343-521">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="8e343-522">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-522">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8e343-523">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="8e343-523">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="8e343-524">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-524">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8e343-525">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="8e343-525">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="8e343-526">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-526">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="8e343-527">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="8e343-527">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="8e343-528">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="8e343-528">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="8e343-529">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="8e343-529">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="8e343-530">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="8e343-530">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="8e343-531">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="8e343-531">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="8e343-532">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-532">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="8e343-533">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-533">Overall improved help files</span></span>
* <span data-ttu-id="8e343-534">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-534">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-535">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-535">Az.Network</span></span>
* <span data-ttu-id="8e343-536">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-536">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="8e343-537">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-537">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="8e343-538">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-538">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="8e343-539">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-539">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="8e343-540">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-540">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="8e343-541">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-541">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="8e343-542">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-542">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="8e343-543">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-543">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="8e343-544">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-544">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="8e343-545">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-545">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="8e343-546">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-546">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="8e343-547">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="8e343-547">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="8e343-548">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-548">New cmdlets</span></span>
        - <span data-ttu-id="8e343-549">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="8e343-549">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="8e343-550">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-550">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="8e343-551">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-551">Updated cmdlet:</span></span>
        - <span data-ttu-id="8e343-552">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8e343-552">New-VpnSite</span></span>
        - <span data-ttu-id="8e343-553">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8e343-553">Update-VpnSite</span></span>
        - <span data-ttu-id="8e343-554">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-554">New-VpnConnection</span></span>
        - <span data-ttu-id="8e343-555">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-555">Update-VpnConnection</span></span>
* <span data-ttu-id="8e343-556">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-556">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-557">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-557">Az.RecoveryServices</span></span>
* <span data-ttu-id="8e343-558">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-558">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="8e343-559">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-559">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-560">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-560">Az.Resources</span></span>
* <span data-ttu-id="8e343-561">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-561">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8e343-562">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e343-562">Az.ServiceFabric</span></span>
* <span data-ttu-id="8e343-563">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-563">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="8e343-564">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="8e343-564">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="8e343-565">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8e343-565">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8e343-566">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8e343-566">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8e343-567">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8e343-567">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8e343-568">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8e343-568">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="8e343-569">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8e343-569">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8e343-570">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8e343-570">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8e343-571">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8e343-571">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8e343-572">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8e343-572">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8e343-573">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8e343-573">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="8e343-574">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8e343-574">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8e343-575">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8e343-575">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8e343-576">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8e343-576">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8e343-577">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="8e343-577">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="8e343-578">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-578">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8e343-579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8e343-579">Az.SignalR</span></span>
* <span data-ttu-id="8e343-580">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-580">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-581">Az.Sql</span></span>
* <span data-ttu-id="8e343-582">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-582">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="8e343-583">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-583">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="8e343-584">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-584">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="8e343-585">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-585">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="8e343-586">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-586">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-587">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-587">Az.Storage</span></span>
* <span data-ttu-id="8e343-588">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-588">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="8e343-589">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-589">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="8e343-590">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8e343-590">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="8e343-591">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8e343-591">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="8e343-592">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-592">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="8e343-593">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8e343-593">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="8e343-594">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-594">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="8e343-595">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8e343-595">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8e343-596">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8e343-596">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8e343-597">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8e343-597">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8e343-598">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8e343-598">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-599">Az.Websites</span></span>
* <span data-ttu-id="8e343-600">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="8e343-600">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="8e343-601">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="8e343-601">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="8e343-602">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-602">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="8e343-603">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-603">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="8e343-604">Genel</span><span class="sxs-lookup"><span data-stu-id="8e343-604">General</span></span>
* <span data-ttu-id="8e343-605">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-605">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8e343-606">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-606">Az.Accounts</span></span>
* <span data-ttu-id="8e343-607">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="8e343-607">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="8e343-608">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8e343-608">Az.Aks</span></span>
* <span data-ttu-id="8e343-609">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-609">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="8e343-610">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="8e343-610">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8e343-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e343-611">Az.ApiManagement</span></span>
* <span data-ttu-id="8e343-612">https://github.com/Azure/azure-powershell/issues/9351 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-612">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="8e343-613">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-613">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="8e343-614">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-614">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="8e343-615">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="8e343-615">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="8e343-616">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-616">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8e343-617">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8e343-617">Az.Batch</span></span>
* <span data-ttu-id="8e343-618">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-618">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8e343-619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8e343-619">Az.Cdn</span></span>
* <span data-ttu-id="8e343-620">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-620">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-621">Az.Compute</span></span>
* <span data-ttu-id="8e343-622">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-622">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="8e343-623">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-623">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="8e343-624">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-624">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="8e343-625">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-625">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="8e343-626">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="8e343-626">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="8e343-627">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-627">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="8e343-628">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-628">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="8e343-629">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-629">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8e343-630">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e343-630">Az.DataFactory</span></span>
* <span data-ttu-id="8e343-631">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-631">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="8e343-632">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-632">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="8e343-633">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-633">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="8e343-634">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-634">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8e343-635">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-635">Az.DataLakeStore</span></span>
* <span data-ttu-id="8e343-636">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-636">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8e343-637">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8e343-637">Az.EventHub</span></span>
* <span data-ttu-id="8e343-638">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="8e343-638">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="8e343-639">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="8e343-639">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="8e343-640">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-640">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="8e343-641">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="8e343-641">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="8e343-642">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8e343-642">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8e343-643">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-643">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8e343-644">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8e343-644">Az.Monitor</span></span>
* <span data-ttu-id="8e343-645">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-645">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-646">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-646">Az.Network</span></span>
* <span data-ttu-id="8e343-647">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-647">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="8e343-648">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-648">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="8e343-649">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-649">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="8e343-650">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="8e343-650">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="8e343-651">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="8e343-651">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="8e343-652">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-652">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="8e343-653">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-653">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8e343-654">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8e343-654">Az.OperationalInsights</span></span>
* <span data-ttu-id="8e343-655">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-655">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="8e343-656">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-656">Added example</span></span>
    - <span data-ttu-id="8e343-657">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-657">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="8e343-658">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-658">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="8e343-659">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-659">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-660">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-660">Az.RecoveryServices</span></span>
* <span data-ttu-id="8e343-661">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-661">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-662">Az.Resources</span></span>
* <span data-ttu-id="8e343-663">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-663">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="8e343-664">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-664">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="8e343-665">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="8e343-665">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="8e343-666">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-666">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8e343-667">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8e343-667">Az.ServiceBus</span></span>
* <span data-ttu-id="8e343-668">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="8e343-668">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="8e343-669">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="8e343-669">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="8e343-670">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-670">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="8e343-671">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e343-671">Az.ServiceFabric</span></span>
* <span data-ttu-id="8e343-672">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-672">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="8e343-673">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="8e343-673">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="8e343-674">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="8e343-674">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="8e343-675">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-675">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="8e343-676">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="8e343-676">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="8e343-677">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-677">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-678">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-678">Az.Sql</span></span>
* <span data-ttu-id="8e343-679">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-679">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-680">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-680">Az.Storage</span></span>
* <span data-ttu-id="8e343-681">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-681">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="8e343-682">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="8e343-682">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="8e343-683">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8e343-683">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="8e343-684">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8e343-684">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="8e343-685">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="8e343-685">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="8e343-686">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8e343-686">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-687">Az.Websites</span></span>
* <span data-ttu-id="8e343-688">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-688">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="8e343-689">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-689">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8e343-690">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-690">Az.Accounts</span></span>
* <span data-ttu-id="8e343-691">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="8e343-692">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8e343-692">Az.ApplicationInsights</span></span>
* <span data-ttu-id="8e343-693">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-693">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="8e343-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8e343-694">Az.Automation</span></span>
* <span data-ttu-id="8e343-695">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-695">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="8e343-696">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8e343-696">Az.CognitiveServices</span></span>
* <span data-ttu-id="8e343-697">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-697">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-698">Az.Compute</span></span>
* <span data-ttu-id="8e343-699">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-699">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8e343-700">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8e343-700">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8e343-701">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-701">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="8e343-702">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="8e343-702">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8e343-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e343-703">Az.DataFactory</span></span>
* <span data-ttu-id="8e343-704">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-704">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="8e343-705">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-705">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8e343-706">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8e343-706">Az.EventHub</span></span>
* <span data-ttu-id="8e343-707">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8e343-707">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8e343-708">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-708">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8e343-709">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e343-709">Az.KeyVault</span></span>
* <span data-ttu-id="8e343-710">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-710">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8e343-711">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8e343-711">Az.LogicApp</span></span>
* <span data-ttu-id="8e343-712">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="8e343-712">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="8e343-713">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-713">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8e343-714">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8e343-714">Az.ManagedServices</span></span>
* <span data-ttu-id="8e343-715">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="8e343-715">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-716">Az.Network</span></span>
* <span data-ttu-id="8e343-717">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-717">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="8e343-718">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-718">New cmdlets</span></span>
        - <span data-ttu-id="8e343-719">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e343-719">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8e343-720">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8e343-720">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8e343-721">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-721">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8e343-722">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-722">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8e343-723">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-723">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8e343-724">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-724">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8e343-725">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="8e343-725">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="8e343-726">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8e343-726">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="8e343-727">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="8e343-727">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="8e343-728">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-728">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="8e343-729">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-729">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="8e343-730">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-730">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="8e343-731">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-731">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="8e343-732">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-732">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="8e343-733">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-733">Updated cmdlets</span></span>
        - <span data-ttu-id="8e343-734">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-734">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8e343-735">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-735">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8e343-736">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-736">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8e343-737">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-737">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8e343-738">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-738">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="8e343-739">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-739">Updated cmdlet:</span></span>
        - <span data-ttu-id="8e343-740">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-740">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8e343-741">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-741">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8e343-742">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-742">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="8e343-743">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-743">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="8e343-744">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-744">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="8e343-745">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="8e343-745">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8e343-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8e343-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="8e343-747">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-747">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="8e343-748">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-748">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-749">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-749">Az.RecoveryServices</span></span>
* <span data-ttu-id="8e343-750">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-750">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8e343-751">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-751">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="8e343-752">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-752">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="8e343-753">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-753">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8e343-754">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-754">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="8e343-755">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-755">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8e343-756">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-756">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="8e343-757">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-757">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8e343-758">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-758">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="8e343-759">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-759">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-760">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-760">Az.Resources</span></span>
- <span data-ttu-id="8e343-761">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-761">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="8e343-762">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-762">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8e343-763">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8e343-763">Az.ServiceBus</span></span>
* <span data-ttu-id="8e343-764">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8e343-764">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8e343-765">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-765">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-766">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-766">Az.Sql</span></span>
* <span data-ttu-id="8e343-767">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-767">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="8e343-768">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-768">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="8e343-769">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-769">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-770">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-770">Az.Storage</span></span>
* <span data-ttu-id="8e343-771">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-771">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8e343-772">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8e343-772">Az.StorageSync</span></span>
* <span data-ttu-id="8e343-773">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-773">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="8e343-774">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-774">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-775">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-775">Az.Websites</span></span>
* <span data-ttu-id="8e343-776">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-776">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="8e343-777">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-777">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="8e343-778">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-778">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="8e343-779">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-779">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8e343-780">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-780">Az.Accounts</span></span>
* <span data-ttu-id="8e343-781">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-781">Add support for profile cmdlets</span></span>
* <span data-ttu-id="8e343-782">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-782">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="8e343-783">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-783">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8e343-784">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8e343-784">Az.Advisor</span></span>
* <span data-ttu-id="8e343-785">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="8e343-785">GA release of Az.Advisor</span></span>
* <span data-ttu-id="8e343-786">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="8e343-786">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8e343-787">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e343-787">Az.ApiManagement</span></span>
* <span data-ttu-id="8e343-788">https://github.com/Azure/azure-powershell/issues/8671 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-788">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="8e343-789">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8e343-789">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="8e343-790">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-790">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="8e343-791">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="8e343-791">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="8e343-792">https://github.com/Azure/azure-powershell/issues/9307 ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="8e343-792">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="8e343-793">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8e343-793">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="8e343-794">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-794">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8e343-795">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8e343-795">Az.Automation</span></span>
* <span data-ttu-id="8e343-796">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-796">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-797">Az.Compute</span></span>
* <span data-ttu-id="8e343-798">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-798">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8e343-799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e343-799">Az.DataFactory</span></span>
* <span data-ttu-id="8e343-800">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-800">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8e343-801">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8e343-801">Az.EventGrid</span></span>
* <span data-ttu-id="8e343-802">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-802">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8e343-803">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8e343-803">Az.IotHub</span></span>
* <span data-ttu-id="8e343-804">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-804">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-805">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-805">Az.Network</span></span>
* <span data-ttu-id="8e343-806">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-806">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="8e343-807">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-807">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8e343-808">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8e343-808">Az.PolicyInsights</span></span>
* <span data-ttu-id="8e343-809">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-809">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="8e343-810">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="8e343-810">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8e343-811">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8e343-811">Az.OperationalInsights</span></span>
* <span data-ttu-id="8e343-812">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-812">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-813">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-813">Az.RecoveryServices</span></span>
* <span data-ttu-id="8e343-814">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="8e343-814">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-815">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-815">Az.Resources</span></span>
    - <span data-ttu-id="8e343-816">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="8e343-816">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="8e343-817">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-817">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="8e343-818">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-818">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="8e343-819">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-819">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8e343-820">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8e343-820">Az.ServiceBus</span></span>
* <span data-ttu-id="8e343-821">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-821">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-822">Az.Sql</span></span>
* <span data-ttu-id="8e343-823">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-823">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="8e343-824">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-824">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="8e343-825">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8e343-825">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8e343-826">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8e343-826">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8e343-827">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8e343-827">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8e343-828">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8e343-828">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8e343-829">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8e343-829">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8e343-830">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8e343-830">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="8e343-831">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-831">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-832">Az.Storage</span></span>
* <span data-ttu-id="8e343-833">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-833">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="8e343-834">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8e343-834">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="8e343-835">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-835">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="8e343-836">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="8e343-836">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="8e343-837">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-837">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="8e343-838">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-838">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8e343-839">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-839">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8e343-840">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-840">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="8e343-841">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8e343-841">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="8e343-842">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8e343-842">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8e343-843">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8e343-843">Az.StorageSync</span></span>
* <span data-ttu-id="8e343-844">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="8e343-844">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="8e343-845">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-845">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8e343-846">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-846">Az.Accounts</span></span>
* <span data-ttu-id="8e343-847">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-847">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="8e343-848">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="8e343-848">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="8e343-849">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-849">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="8e343-850">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8e343-850">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="8e343-851">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="8e343-851">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-852">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-852">Az.Compute</span></span>
* <span data-ttu-id="8e343-853">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-853">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="8e343-854">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-854">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="8e343-855">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8e343-855">Az.Dns</span></span>
* <span data-ttu-id="8e343-856">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-856">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8e343-857">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8e343-857">Az.EventGrid</span></span>
* <span data-ttu-id="8e343-858">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-858">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="8e343-859">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="8e343-859">New cmdlets:</span></span>
    - <span data-ttu-id="8e343-860">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8e343-860">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8e343-861">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e343-861">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8e343-862">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8e343-862">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8e343-863">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="8e343-863">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="8e343-864">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8e343-864">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8e343-865">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e343-865">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8e343-866">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8e343-866">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8e343-867">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="8e343-867">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8e343-868">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8e343-868">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8e343-869">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="8e343-869">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="8e343-870">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8e343-870">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8e343-871">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e343-871">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="8e343-872">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8e343-872">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="8e343-873">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="8e343-873">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="8e343-874">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8e343-874">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8e343-875">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e343-875">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="8e343-876">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-876">Updated cmdlets:</span></span>
    - <span data-ttu-id="8e343-877">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="8e343-877">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="8e343-878">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="8e343-878">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8e343-879">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="8e343-879">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8e343-880">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="8e343-880">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="8e343-881">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8e343-881">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="8e343-882">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="8e343-882">Event subscription expiration date,</span></span>
            - <span data-ttu-id="8e343-883">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="8e343-883">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="8e343-884">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="8e343-884">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="8e343-885">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="8e343-885">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="8e343-886">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="8e343-886">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="8e343-887">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="8e343-887">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="8e343-888">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8e343-888">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="8e343-889">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="8e343-889">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="8e343-890">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="8e343-890">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8e343-891">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8e343-891">Az.FrontDoor</span></span>
* <span data-ttu-id="8e343-892">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="8e343-892">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="8e343-893">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="8e343-893">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="8e343-894">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="8e343-894">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="8e343-895">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="8e343-895">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-896">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-896">Az.Network</span></span>
* <span data-ttu-id="8e343-897">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="8e343-897">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="8e343-898">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-898">New cmdlets</span></span>
        - <span data-ttu-id="8e343-899">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="8e343-899">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="8e343-900">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="8e343-900">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="8e343-901">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-901">New cmdlets</span></span> 
        - <span data-ttu-id="8e343-902">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8e343-902">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="8e343-903">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="8e343-903">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="8e343-904">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-904">New cmdlets</span></span> 
        - <span data-ttu-id="8e343-905">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8e343-905">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="8e343-906">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8e343-906">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8e343-907">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8e343-907">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8e343-908">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-908">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="8e343-909">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-909">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8e343-910">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="8e343-910">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="8e343-911">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-911">New cmdlets</span></span>
        - <span data-ttu-id="8e343-912">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e343-912">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8e343-913">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e343-913">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8e343-914">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e343-914">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8e343-915">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="8e343-915">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="8e343-916">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="8e343-916">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="8e343-917">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-917">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="8e343-918">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-918">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="8e343-919">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-919">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="8e343-920">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-920">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="8e343-921">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-921">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="8e343-922">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-922">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="8e343-923">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-923">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="8e343-924">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-924">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="8e343-925">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-925">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="8e343-926">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-926">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="8e343-927">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-927">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="8e343-928">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-928">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="8e343-929">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-929">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="8e343-930">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-930">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8e343-931">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-931">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="8e343-932">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-932">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="8e343-933">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8e343-933">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="8e343-934">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8e343-934">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="8e343-935">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="8e343-935">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="8e343-936">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-936">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8e343-937">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-937">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8e343-938">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-938">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8e343-939">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8e343-939">Az.OperationalInsights</span></span>
* <span data-ttu-id="8e343-940">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-940">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-941">Az.Resources</span></span>
* <span data-ttu-id="8e343-942">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="8e343-942">Support for additional Template Export options</span></span>
    - <span data-ttu-id="8e343-943">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-943">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8e343-944">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-944">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8e343-945">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-945">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8e343-946">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e343-946">Az.ServiceFabric</span></span>
* <span data-ttu-id="8e343-947">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-947">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-948">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-948">Az.Sql</span></span>
* <span data-ttu-id="8e343-949">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-949">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="8e343-950">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-950">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="8e343-951">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-951">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="8e343-952">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8e343-952">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8e343-953">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8e343-953">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8e343-954">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8e343-954">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8e343-955">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8e343-955">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="8e343-956">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8e343-956">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-957">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-957">Az.Storage</span></span>
* <span data-ttu-id="8e343-958">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="8e343-958">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="8e343-959">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-959">New-AzStorageAccount</span></span>
* <span data-ttu-id="8e343-960">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-960">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="8e343-961">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8e343-961">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-962">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-962">Az.Websites</span></span>
* <span data-ttu-id="8e343-963">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="8e343-963">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="8e343-964">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="8e343-964">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="8e343-965">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-965">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="8e343-966">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8e343-966">Az.Cdn</span></span>
* <span data-ttu-id="8e343-967">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-967">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-968">Az.Compute</span></span>
* <span data-ttu-id="8e343-969">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-969">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="8e343-970">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8e343-970">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8e343-971">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8e343-971">Az.EventHub</span></span>
* <span data-ttu-id="8e343-972">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="8e343-972">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="8e343-973">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="8e343-973">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-974">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-974">Az.Network</span></span>
* <span data-ttu-id="8e343-975">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-975">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="8e343-976">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-976">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8e343-977">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8e343-977">Az.PolicyInsights</span></span>
* <span data-ttu-id="8e343-978">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-978">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="8e343-980">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-980">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8e343-981">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8e343-981">Az.ServiceBus</span></span>
* <span data-ttu-id="8e343-982">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="8e343-982">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8e343-983">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e343-983">Az.ServiceFabric</span></span>
* <span data-ttu-id="8e343-984">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-984">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="8e343-985">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-985">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-986">Az.Sql</span></span>
* <span data-ttu-id="8e343-987">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-987">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="8e343-988">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-988">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8e343-989">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-989">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="8e343-990">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="8e343-990">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-991">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-991">Az.Websites</span></span>
* <span data-ttu-id="8e343-992">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="8e343-992">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="8e343-993">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-993">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8e343-994">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e343-994">Az.ApiManagement</span></span>
* <span data-ttu-id="8e343-995">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="8e343-995">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="8e343-996">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="8e343-996">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="8e343-997">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="8e343-997">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="8e343-998">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="8e343-998">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="8e343-999">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e343-999">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="8e343-1000">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="8e343-1000">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="8e343-1001">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="8e343-1001">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="8e343-1002">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="8e343-1002">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="8e343-1003">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="8e343-1003">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="8e343-1004">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="8e343-1004">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="8e343-1005">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="8e343-1005">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="8e343-1006">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="8e343-1006">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="8e343-1007">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="8e343-1007">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="8e343-1008">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="8e343-1008">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="8e343-1009">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="8e343-1009">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="8e343-1010">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="8e343-1010">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="8e343-1011">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="8e343-1011">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="8e343-1012">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="8e343-1012">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="8e343-1013">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="8e343-1013">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="8e343-1014">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="8e343-1014">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="8e343-1015">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="8e343-1015">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="8e343-1016">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8e343-1016">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="8e343-1017">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="8e343-1017">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="8e343-1018">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1018">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="8e343-1019">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1019">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="8e343-1020">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1020">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="8e343-1021">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="8e343-1021">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="8e343-1022">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8e343-1022">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="8e343-1023">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1023">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="8e343-1024">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1024">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="8e343-1025">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1025">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="8e343-1026">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="8e343-1026">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="8e343-1027">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1027">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="8e343-1028">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1028">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8e343-1029">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="8e343-1029">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="8e343-1030">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="8e343-1030">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="8e343-1031">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="8e343-1031">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="8e343-1032">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1032">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="8e343-1033">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1033">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="8e343-1034">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1034">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="8e343-1035">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="8e343-1035">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8e343-1036">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="8e343-1036">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8e343-1037">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="8e343-1037">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="8e343-1038">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="8e343-1038">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="8e343-1039">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1039">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8e343-1040">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="8e343-1040">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8e343-1041">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="8e343-1041">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="8e343-1042">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="8e343-1042">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="8e343-1043">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1043">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="8e343-1044">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="8e343-1044">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="8e343-1045">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="8e343-1045">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="8e343-1046">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="8e343-1046">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="8e343-1047">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="8e343-1047">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="8e343-1048">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1048">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="8e343-1049">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="8e343-1049">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="8e343-1050">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="8e343-1050">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="8e343-1051">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1051">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8e343-1052">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="8e343-1052">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8e343-1053">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="8e343-1053">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8e343-1054">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1054">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8e343-1055">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1055">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8e343-1056">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="8e343-1056">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8e343-1057">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="8e343-1057">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8e343-1058">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1058">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8e343-1059">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1059">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="8e343-1060">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="8e343-1060">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="8e343-1061">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="8e343-1061">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="8e343-1062">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="8e343-1062">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="8e343-1063">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="8e343-1063">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="8e343-1064">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="8e343-1064">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="8e343-1065">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="8e343-1065">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="8e343-1066">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="8e343-1066">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="8e343-1067">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="8e343-1067">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="8e343-1068">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="8e343-1068">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="8e343-1069">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="8e343-1069">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="8e343-1070">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="8e343-1070">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="8e343-1071">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="8e343-1071">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8e343-1072">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8e343-1072">Az.Automation</span></span>
* <span data-ttu-id="8e343-1073">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1073">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="8e343-1074">https://github.com/Azure/azure-powershell/issues/7977 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1074">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="8e343-1075">https://github.com/Azure/azure-powershell/issues/8600 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1075">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="8e343-1076">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1076">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="8e343-1077">https://github.com/Azure/azure-powershell/issues/8347 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1077">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="8e343-1078">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1078">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="8e343-1079">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-1079">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1080">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1080">Az.Compute</span></span>
* <span data-ttu-id="8e343-1081">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1081">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="8e343-1082">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="8e343-1082">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8e343-1083">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-1083">Az.DataLakeStore</span></span>
* <span data-ttu-id="8e343-1084">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1084">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8e343-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8e343-1085">Az.Monitor</span></span>
* <span data-ttu-id="8e343-1086">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1086">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-1087">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-1087">Az.Network</span></span>
* <span data-ttu-id="8e343-1088">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1088">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="8e343-1089">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="8e343-1089">Updated cmdlet:</span></span>
        - <span data-ttu-id="8e343-1090">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e343-1090">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="8e343-1091">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1091">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-1092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1092">Az.Resources</span></span>
* <span data-ttu-id="8e343-1093">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1093">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-1094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1094">Az.Sql</span></span>
* <span data-ttu-id="8e343-1095">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="8e343-1095">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="8e343-1096">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-1096">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8e343-1097">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-1097">Az.Accounts</span></span>
* <span data-ttu-id="8e343-1098">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="8e343-1098">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8e343-1099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1099">Az.CognitiveServices</span></span>
* <span data-ttu-id="8e343-1100">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="8e343-1100">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="8e343-1101">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="8e343-1101">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1102">Az.Compute</span></span>
* <span data-ttu-id="8e343-1103">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="8e343-1103">Proximity placement group feature.</span></span>
    - <span data-ttu-id="8e343-1104">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8e343-1104">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="8e343-1105">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-1105">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="8e343-1106">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1106">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="8e343-1107">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="8e343-1107">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="8e343-1108">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1108">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="8e343-1109">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="8e343-1109">Breaking changes</span></span>
    - <span data-ttu-id="8e343-1110">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1110">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="8e343-1111">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1111">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8e343-1112">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8e343-1112">Az.DeploymentManager</span></span>
* <span data-ttu-id="8e343-1113">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="8e343-1113">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="8e343-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8e343-1114">Az.Dns</span></span>
* <span data-ttu-id="8e343-1115">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="8e343-1115">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="8e343-1116">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="8e343-1116">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="8e343-1117">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="8e343-1117">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8e343-1118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8e343-1118">Az.FrontDoor</span></span>
* <span data-ttu-id="8e343-1119">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="8e343-1119">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="8e343-1120">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="8e343-1120">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="8e343-1121">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8e343-1121">Az.HDInsight</span></span>
* <span data-ttu-id="8e343-1122">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="8e343-1122">Removed two cmdlets:</span></span>
    - <span data-ttu-id="8e343-1123">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8e343-1123">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="8e343-1124">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8e343-1124">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8e343-1125">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1125">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8e343-1126">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="8e343-1126">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="8e343-1127">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="8e343-1127">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="8e343-1128">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="8e343-1128">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8e343-1129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8e343-1129">Az.Monitor</span></span>
* <span data-ttu-id="8e343-1130">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="8e343-1130">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="8e343-1131">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="8e343-1131">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="8e343-1132">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="8e343-1132">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="8e343-1133">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="8e343-1133">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="8e343-1134">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="8e343-1134">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="8e343-1135">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="8e343-1135">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="8e343-1136">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8e343-1136">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="8e343-1137">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8e343-1137">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8e343-1138">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8e343-1138">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8e343-1139">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8e343-1139">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8e343-1140">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8e343-1140">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8e343-1141">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8e343-1141">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8e343-1142">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="8e343-1142">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="8e343-1143">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1143">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-1144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-1144">Az.Network</span></span>
* <span data-ttu-id="8e343-1145">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="8e343-1145">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="8e343-1146">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-1146">New cmdlets</span></span>
        - <span data-ttu-id="8e343-1147">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8e343-1147">New-AzNatGateway</span></span>
        - <span data-ttu-id="8e343-1148">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8e343-1148">Get-AzNatGateway</span></span>
        - <span data-ttu-id="8e343-1149">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8e343-1149">Set-AzNatGateway</span></span>
        - <span data-ttu-id="8e343-1150">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8e343-1150">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="8e343-1151">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1151">Updated cmdlets</span></span>
        - <span data-ttu-id="8e343-1152">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8e343-1152">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="8e343-1153">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8e343-1153">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="8e343-1154">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="8e343-1154">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="8e343-1155">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1155">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="8e343-1156">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1156">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8e343-1157">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8e343-1157">Az.PolicyInsights</span></span>
* <span data-ttu-id="8e343-1158">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-1158">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="8e343-1159">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8e343-1159">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="8e343-1160">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="8e343-1160">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="8e343-1162">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-1162">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="8e343-1163">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="8e343-1163">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="8e343-1164">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="8e343-1164">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="8e343-1165">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="8e343-1165">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="8e343-1166">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="8e343-1166">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="8e343-1167">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="8e343-1167">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="8e343-1168">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8e343-1168">Az.Relay</span></span>
* <span data-ttu-id="8e343-1169">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="8e343-1169">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8e343-1170">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8e343-1170">Az.ServiceBus</span></span>
* <span data-ttu-id="8e343-1171">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1171">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-1172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-1172">Az.Storage</span></span>
* <span data-ttu-id="8e343-1173">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="8e343-1173">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="8e343-1174">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="8e343-1174">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="8e343-1175">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="8e343-1175">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="8e343-1176">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-1176">New-AzStorageAccount</span></span>
* <span data-ttu-id="8e343-1177">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="8e343-1177">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="8e343-1178">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-1178">New-AzStorageAccount</span></span>
    - <span data-ttu-id="8e343-1179">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-1179">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="8e343-1180">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-1180">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-1181">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-1181">Az.Websites</span></span>
* <span data-ttu-id="8e343-1182">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="8e343-1182">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="8e343-1183">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1183">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="8e343-1184">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-1184">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8e343-1185">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="8e343-1185">Highlights since the last major release</span></span>
* <span data-ttu-id="8e343-1186">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="8e343-1186">General availability of `Az` module</span></span>
* <span data-ttu-id="8e343-1187">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8e343-1187">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8e343-1188">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8e343-1188">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8e343-1189">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1189">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8e343-1190">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1190">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8e343-1191">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1191">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8e343-1192">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-1192">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8e343-1193">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-1193">Az.Accounts</span></span>
* <span data-ttu-id="8e343-1194">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1194">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8e343-1195">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8e343-1195">Az.Batch</span></span>
* <span data-ttu-id="8e343-1196">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8e343-1197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8e343-1197">Az.Cdn</span></span>
* <span data-ttu-id="8e343-1198">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8e343-1199">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1199">Az.CognitiveServices</span></span>
* <span data-ttu-id="8e343-1200">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1200">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1201">Az.Compute</span></span>
* <span data-ttu-id="8e343-1202">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1202">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="8e343-1203">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8e343-1204">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1204">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8e343-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e343-1205">Az.DataFactory</span></span>
* <span data-ttu-id="8e343-1206">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1206">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8e343-1207">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-1207">Az.DataLakeStore</span></span>
* <span data-ttu-id="8e343-1208">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8e343-1209">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8e343-1209">Az.EventGrid</span></span>
* <span data-ttu-id="8e343-1210">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1210">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8e343-1211">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8e343-1211">Az.EventHub</span></span>
* <span data-ttu-id="8e343-1212">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1212">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="8e343-1213">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8e343-1213">Az.HDInsight</span></span>
* <span data-ttu-id="8e343-1214">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1214">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8e343-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8e343-1215">Az.IotHub</span></span>
* <span data-ttu-id="8e343-1216">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8e343-1217">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e343-1217">Az.KeyVault</span></span>
* <span data-ttu-id="8e343-1218">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8e343-1219">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1219">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8e343-1220">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8e343-1220">Az.MachineLearning</span></span>
* <span data-ttu-id="8e343-1221">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="8e343-1222">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8e343-1222">Az.Media</span></span>
* <span data-ttu-id="8e343-1223">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8e343-1224">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8e343-1224">Az.Monitor</span></span>
  * <span data-ttu-id="8e343-1225">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="8e343-1225">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="8e343-1226">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8e343-1226">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="8e343-1227">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8e343-1227">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="8e343-1228">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8e343-1228">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8e343-1229">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8e343-1229">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8e343-1230">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8e343-1230">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="8e343-1231">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1231">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-1232">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-1232">Az.Network</span></span>
* <span data-ttu-id="8e343-1233">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8e343-1234">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1234">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="8e343-1235">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8e343-1235">Az.NotificationHubs</span></span>
* <span data-ttu-id="8e343-1236">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8e343-1237">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8e343-1237">Az.OperationalInsights</span></span>
* <span data-ttu-id="8e343-1238">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8e343-1239">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8e343-1239">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8e343-1240">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-1241">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1241">Az.RecoveryServices</span></span>
* <span data-ttu-id="8e343-1242">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8e343-1243">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="8e343-1243">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="8e343-1244">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1244">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="8e343-1245">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1245">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8e343-1246">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8e343-1246">Az.RedisCache</span></span>
* <span data-ttu-id="8e343-1247">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-1248">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1248">Az.Resources</span></span>
* <span data-ttu-id="8e343-1249">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1249">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-1250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1250">Az.Sql</span></span>
* <span data-ttu-id="8e343-1251">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1251">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="8e343-1252">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8e343-1253">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1253">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="8e343-1254">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1254">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="8e343-1255">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1255">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="8e343-1256">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-1256">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="8e343-1257">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1257">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-1258">Az.Websites</span></span>
* <span data-ttu-id="8e343-1259">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1259">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="8e343-1260">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8e343-1261">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1261">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="8e343-1262">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1262">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="8e343-1263">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-1263">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8e343-1264">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="8e343-1264">Highlights since the last major release</span></span>
* <span data-ttu-id="8e343-1265">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="8e343-1265">General availability of `Az` module</span></span>
* <span data-ttu-id="8e343-1266">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8e343-1266">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8e343-1267">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8e343-1267">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8e343-1268">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1268">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8e343-1269">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1269">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8e343-1270">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1270">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8e343-1271">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-1271">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8e343-1272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-1272">Az.Accounts</span></span>
* <span data-ttu-id="8e343-1273">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1273">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8e343-1274">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1274">Az.AnalysisServices</span></span>
* <span data-ttu-id="8e343-1275">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e343-1275">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="8e343-1276">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="8e343-1276">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8e343-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8e343-1277">Az.Automation</span></span>
* <span data-ttu-id="8e343-1278">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1278">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="8e343-1279">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-1279">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="8e343-1280">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="8e343-1280">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1281">Az.Compute</span></span>
* <span data-ttu-id="8e343-1282">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1282">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8e343-1283">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1283">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="8e343-1284">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8e343-1284">Az.ContainerInstance</span></span>
* <span data-ttu-id="8e343-1285">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1285">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8e343-1286">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e343-1286">Az.DataFactory</span></span>
* <span data-ttu-id="8e343-1287">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1287">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="8e343-1288">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1288">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-1289">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1289">Az.Resources</span></span>
* <span data-ttu-id="8e343-1290">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1290">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="8e343-1291">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1291">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8e343-1292">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1292">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="8e343-1293">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8e343-1293">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="8e343-1294">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1294">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="8e343-1295">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8e343-1295">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-1296">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1296">Az.Sql</span></span>
* <span data-ttu-id="8e343-1297">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-1297">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-1298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-1298">Az.Storage</span></span>
* <span data-ttu-id="8e343-1299">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="8e343-1299">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="8e343-1300">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8e343-1300">New-AzStorageContext</span></span>
* <span data-ttu-id="8e343-1301">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="8e343-1301">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="8e343-1302">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8e343-1302">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8e343-1303">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8e343-1303">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8e343-1304">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8e343-1304">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="8e343-1305">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8e343-1305">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="8e343-1306">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="8e343-1306">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="8e343-1307">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8e343-1307">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8e343-1308">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8e343-1308">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8e343-1309">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8e343-1309">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="8e343-1310">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8e343-1310">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="8e343-1311">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-1311">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8e343-1312">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="8e343-1312">Highlights since the last major release</span></span>
* <span data-ttu-id="8e343-1313">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="8e343-1313">General availability of `Az` module</span></span>
* <span data-ttu-id="8e343-1314">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8e343-1314">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8e343-1315">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8e343-1315">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8e343-1316">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1316">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8e343-1317">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1317">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8e343-1318">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1318">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8e343-1319">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-1319">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8e343-1320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8e343-1320">Az.Automation</span></span>
* <span data-ttu-id="8e343-1321">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="8e343-1321">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="8e343-1322">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="8e343-1322">Dynamic grouping</span></span>
    * <span data-ttu-id="8e343-1323">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="8e343-1323">Pre-Post script</span></span>
    * <span data-ttu-id="8e343-1324">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="8e343-1324">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1325">Az.Compute</span></span>
* <span data-ttu-id="8e343-1326">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="8e343-1326">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="8e343-1327">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1327">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8e343-1328">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e343-1328">Az.KeyVault</span></span>
* <span data-ttu-id="8e343-1329">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1329">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-1330">Az.Network</span></span>
* <span data-ttu-id="8e343-1331">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1331">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="8e343-1332">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1332">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-1333">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1333">Az.RecoveryServices</span></span>
* <span data-ttu-id="8e343-1334">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1334">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="8e343-1335">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1335">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-1336">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1336">Az.Resources</span></span>
* <span data-ttu-id="8e343-1337">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1337">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="8e343-1338">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1338">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1339">Az.Sql</span></span>
* <span data-ttu-id="8e343-1340">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1340">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-1341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-1341">Az.Storage</span></span>
* <span data-ttu-id="8e343-1342">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="8e343-1342">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="8e343-1343">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8e343-1343">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8e343-1344">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8e343-1344">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8e343-1345">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8e343-1345">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8e343-1346">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8e343-1346">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="8e343-1347">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8e343-1347">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="8e343-1348">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8e343-1348">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-1349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-1349">Az.Websites</span></span>
* <span data-ttu-id="8e343-1350">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1350">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="8e343-1351">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-1351">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8e343-1352">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-1352">Az.Accounts</span></span>
* <span data-ttu-id="8e343-1353">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1353">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="8e343-1354">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1354">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8e343-1355">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8e343-1355">Az.Automation</span></span>
* <span data-ttu-id="8e343-1356">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1356">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="8e343-1357">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1357">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="8e343-1358">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="8e343-1358">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8e343-1359">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8e343-1359">Az.Cdn</span></span>
* <span data-ttu-id="8e343-1360">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-1360">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1361">Az.Compute</span></span>
* <span data-ttu-id="8e343-1362">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1362">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8e343-1363">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e343-1363">Az.DataFactory</span></span>
* <span data-ttu-id="8e343-1364">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1364">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8e343-1365">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8e343-1365">Az.LogicApp</span></span>
* <span data-ttu-id="8e343-1366">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="8e343-1366">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-1367">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-1367">Az.Network</span></span>
* <span data-ttu-id="8e343-1368">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1368">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-1369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1369">Az.RecoveryServices</span></span>
* <span data-ttu-id="8e343-1370">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1370">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="8e343-1371">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="8e343-1371">SDK Update</span></span>
* <span data-ttu-id="8e343-1372">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-1372">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="8e343-1373">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1373">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-1374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1374">Az.Resources</span></span>
* <span data-ttu-id="8e343-1375">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1375">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="8e343-1376">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="8e343-1376">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="8e343-1377">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1377">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="8e343-1378">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="8e343-1378">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="8e343-1379">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1379">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="8e343-1380">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="8e343-1380">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-1381">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1381">Az.Sql</span></span>
* <span data-ttu-id="8e343-1382">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-1382">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="8e343-1383">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-1383">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-1384">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-1384">Az.Storage</span></span>
* <span data-ttu-id="8e343-1385">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-1385">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="8e343-1386">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-1386">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8e343-1387">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1387">Az.AnalysisServices</span></span>
* <span data-ttu-id="8e343-1388">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-1388">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8e343-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8e343-1389">Az.Automation</span></span>
* <span data-ttu-id="8e343-1390">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1390">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8e343-1391">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1391">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8e343-1392">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1392">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8e343-1393">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1393">Az.CognitiveServices</span></span>
* <span data-ttu-id="8e343-1394">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1394">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1395">Az.Compute</span></span>
* <span data-ttu-id="8e343-1396">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1396">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8e343-1397">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1397">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8e343-1398">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1398">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8e343-1399">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="8e343-1399">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8e343-1400">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-1400">Az.DataLakeStore</span></span>
* <span data-ttu-id="8e343-1401">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1401">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8e343-1402">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8e343-1402">Az.EventHub</span></span>
* <span data-ttu-id="8e343-1403">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1403">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="8e343-1404">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e343-1404">Az.KeyVault</span></span>
* <span data-ttu-id="8e343-1405">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1405">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8e343-1406">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8e343-1406">Az.LogicApp</span></span>
* <span data-ttu-id="8e343-1407">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1407">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8e343-1408">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1408">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8e343-1409">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-1409">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8e343-1410">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8e343-1410">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8e343-1411">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8e343-1411">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8e343-1412">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8e343-1412">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8e343-1413">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8e343-1413">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8e343-1414">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8e343-1414">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8e343-1415">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e343-1415">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8e343-1416">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e343-1416">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8e343-1417">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e343-1417">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8e343-1418">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e343-1418">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8e343-1419">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1419">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8e343-1420">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8e343-1420">Az.Monitor</span></span>
* <span data-ttu-id="8e343-1421">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1421">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-1422">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-1422">Az.Network</span></span>
* <span data-ttu-id="8e343-1423">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1423">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8e343-1424">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8e343-1424">Az.OperationalInsights</span></span>
* <span data-ttu-id="8e343-1425">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="8e343-1425">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8e343-1426">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1426">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="8e343-1427">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1427">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="8e343-1428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1428">Az.Resources</span></span>
* <span data-ttu-id="8e343-1429">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1429">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8e343-1430">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1430">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8e343-1431">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1431">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8e343-1432">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1432">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-1433">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1433">Az.Sql</span></span>
* <span data-ttu-id="8e343-1434">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1434">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8e343-1435">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1435">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-1436">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-1436">Az.Websites</span></span>
* <span data-ttu-id="8e343-1437">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1437">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8e343-1438">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-1438">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8e343-1439">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-1439">Az.Accounts</span></span>
* <span data-ttu-id="8e343-1440">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8e343-1440">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8e343-1441">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1441">Az.AnalysisServices</span></span>
<span data-ttu-id="8e343-1442">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="8e343-1442">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1443">Az.Compute</span></span>
* <span data-ttu-id="8e343-1444">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1444">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8e343-1445">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1445">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8e343-1446">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1446">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-1447">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1447">Az.RecoveryServices</span></span>
<span data-ttu-id="8e343-1448">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="8e343-1448">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-1449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1449">Az.Resources</span></span>
* <span data-ttu-id="8e343-1450">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1450">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="8e343-1451">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8e343-1451">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8e343-1452">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1452">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="8e343-1453">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8e343-1453">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-1454">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1454">Az.Sql</span></span>
* <span data-ttu-id="8e343-1455">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8e343-1455">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8e343-1456">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1456">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8e343-1457">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1457">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8e343-1458">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-1458">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8e343-1459">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-1459">Az.Accounts</span></span>
* <span data-ttu-id="8e343-1460">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="8e343-1460">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8e343-1461">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1461">Az.AnalysisServices</span></span>
* <span data-ttu-id="8e343-1462">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="8e343-1462">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-1463">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1463">Az.RecoveryServices</span></span>
* <span data-ttu-id="8e343-1464">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="8e343-1464">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8e343-1465">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-1465">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8e343-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-1466">Az.Accounts</span></span>
* <span data-ttu-id="8e343-1467">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1467">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8e343-1468">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1468">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8e343-1469">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1469">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8e343-1470">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8e343-1470">Az.Aks</span></span>
* <span data-ttu-id="8e343-1471">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1471">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8e343-1472">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8e343-1472">Az.Automation</span></span>
* <span data-ttu-id="8e343-1473">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1473">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8e343-1474">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1474">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8e343-1475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8e343-1475">Az.Cdn</span></span>
* <span data-ttu-id="8e343-1476">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1476">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1477">Az.Compute</span></span>
* <span data-ttu-id="8e343-1478">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1478">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8e343-1479">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1479">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8e343-1480">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1480">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8e343-1481">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8e343-1481">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8e343-1482">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1482">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8e343-1483">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e343-1483">Az.DataFactory</span></span>
* <span data-ttu-id="8e343-1484">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1484">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8e343-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-1485">Az.DataLakeStore</span></span>
* <span data-ttu-id="8e343-1486">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1486">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8e343-1487">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="8e343-1487">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8e343-1488">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1488">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8e343-1489">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8e343-1489">Az.IotHub</span></span>
* <span data-ttu-id="8e343-1490">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1490">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8e343-1491">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e343-1491">Az.KeyVault</span></span>
* <span data-ttu-id="8e343-1492">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1492">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-1493">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-1493">Az.Network</span></span>
* <span data-ttu-id="8e343-1494">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1494">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1495">Az.Resources</span></span>
* <span data-ttu-id="8e343-1496">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1496">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8e343-1497">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1497">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8e343-1498">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1498">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8e343-1499">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1499">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8e343-1500">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1500">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8e343-1501">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1501">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8e343-1502">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="8e343-1502">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8e343-1503">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e343-1503">Az.ServiceFabric</span></span>
* <span data-ttu-id="8e343-1504">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="8e343-1504">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8e343-1505">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1505">Fix some error messages.</span></span>
* <span data-ttu-id="8e343-1506">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1506">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8e343-1507">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1507">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8e343-1508">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8e343-1508">Az.SignalR</span></span>
* <span data-ttu-id="8e343-1509">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1509">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1510">Az.Sql</span></span>
* <span data-ttu-id="8e343-1511">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1511">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8e343-1512">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1512">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8e343-1513">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1513">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8e343-1514">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="8e343-1514">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-1515">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-1515">Az.Storage</span></span>
* <span data-ttu-id="8e343-1516">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8e343-1517">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-1517">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8e343-1518">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8e343-1518">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8e343-1519">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8e343-1519">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8e343-1520">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8e343-1520">Az.TrafficManager</span></span>
* <span data-ttu-id="8e343-1521">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1521">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-1522">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-1522">Az.Websites</span></span>
* <span data-ttu-id="8e343-1523">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1523">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8e343-1524">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1524">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8e343-1525">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1525">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8e343-1526">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="8e343-1526">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8e343-1527">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-1527">Az.Accounts</span></span>
* <span data-ttu-id="8e343-1528">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1528">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1529">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1529">Az.Compute</span></span>
* <span data-ttu-id="8e343-1530">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="8e343-1530">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8e343-1531">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1531">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8e343-1532">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="8e343-1532">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8e343-1533">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-1533">Az.DataLakeStore</span></span>
* <span data-ttu-id="8e343-1534">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1534">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8e343-1535">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1535">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8e343-1536">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8e343-1536">Az.EventGrid</span></span>
* <span data-ttu-id="8e343-1537">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1537">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8e343-1538">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1538">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8e343-1539">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8e343-1539">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8e343-1540">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="8e343-1540">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8e343-1541">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="8e343-1541">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8e343-1542">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="8e343-1542">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8e343-1543">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8e343-1543">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8e343-1544">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="8e343-1544">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8e343-1545">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="8e343-1545">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8e343-1546">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="8e343-1546">Dead letter endpoint.</span></span>
* <span data-ttu-id="8e343-1547">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1547">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8e343-1548">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-1548">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8e343-1549">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8e343-1549">Az.IotHub</span></span>
* <span data-ttu-id="8e343-1550">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1550">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8e343-1551">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8e343-1551">Az.LogicApp</span></span>
* <span data-ttu-id="8e343-1552">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="8e343-1552">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-1553">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1553">Az.Resources</span></span>
* <span data-ttu-id="8e343-1554">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1554">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8e343-1555">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="8e343-1555">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8e343-1556">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1556">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8e343-1557">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1557">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8e343-1558">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1558">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8e343-1559">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="8e343-1559">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8e343-1560">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8e343-1560">Az.SignalR</span></span>
* <span data-ttu-id="8e343-1561">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="8e343-1561">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1562">Az.Sql</span></span>
* <span data-ttu-id="8e343-1563">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="8e343-1563">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8e343-1564">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-1564">Az.Storage</span></span>
* <span data-ttu-id="8e343-1565">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="8e343-1565">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8e343-1566">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8e343-1566">New-AzStorageContext</span></span>
* <span data-ttu-id="8e343-1567">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1567">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8e343-1568">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8e343-1568">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-1569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-1569">Az.Websites</span></span>
* <span data-ttu-id="8e343-1570">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1570">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8e343-1571">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="8e343-1571">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8e343-1572">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="8e343-1572">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8e343-1573">Genel</span><span class="sxs-lookup"><span data-stu-id="8e343-1573">General</span></span>

- <span data-ttu-id="8e343-1574">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="8e343-1574">General Availability of Az Module</span></span>
- <span data-ttu-id="8e343-1575">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="8e343-1575">Online help for each module</span></span>
- <span data-ttu-id="8e343-1576">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="8e343-1576">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8e343-1577">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1577">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8e343-1578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8e343-1578">Az.Accounts</span></span>
- <span data-ttu-id="8e343-1579">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8e343-1579">Changed from Az.Profile</span></span>
- <span data-ttu-id="8e343-1580">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1580">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8e343-1581">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e343-1581">Az.ApiManagement</span></span>
- <span data-ttu-id="8e343-1582">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="8e343-1582">Fixes for #7002</span></span>
- <span data-ttu-id="8e343-1583">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1583">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8e343-1584">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8e343-1584">Az.Batch</span></span>
- <span data-ttu-id="8e343-1585">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1585">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8e343-1586">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="8e343-1586">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8e343-1587">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1587">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8e343-1588">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8e343-1588">Az.Billing</span></span>
- <span data-ttu-id="8e343-1589">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1589">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8e343-1590">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1590">Az.CognitivServices</span></span>
- <span data-ttu-id="8e343-1591">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1591">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8e343-1592">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-1592">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8e343-1593">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8e343-1593">Az.ContainerInstance</span></span>
- <span data-ttu-id="8e343-1594">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1594">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8e343-1595">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8e343-1595">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8e343-1596">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1596">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8e343-1597">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-1597">Az.DataLakeStore</span></span>
- <span data-ttu-id="8e343-1598">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1598">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8e343-1599">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8e343-1599">Az.Monitor</span></span>
- <span data-ttu-id="8e343-1600">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1600">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8e343-1601">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e343-1601">Az.KeyVault</span></span>
- <span data-ttu-id="8e343-1602">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-1602">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8e343-1603">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8e343-1603">Az.MachineLearning</span></span>
- <span data-ttu-id="8e343-1604">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1604">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8e343-1605">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8e343-1605">Az.Media</span></span>
- <span data-ttu-id="8e343-1606">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8e343-1606">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8e343-1607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-1607">Az.Network</span></span>
<span data-ttu-id="8e343-1608">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1608">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8e343-1609">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8e343-1609">New cmdlets added:</span></span>
        - <span data-ttu-id="8e343-1610">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e343-1610">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8e343-1611">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e343-1611">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8e343-1612">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e343-1612">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8e343-1613">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e343-1613">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8e343-1614">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e343-1614">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8e343-1615">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8e343-1615">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8e343-1616">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8e343-1616">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8e343-1617">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e343-1617">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8e343-1618">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1618">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8e343-1619">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e343-1619">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8e343-1620">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8e343-1620">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8e343-1621">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8e343-1621">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8e343-1622">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-1622">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8e343-1623">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-1623">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8e343-1624">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1624">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8e343-1625">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1625">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8e343-1626">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8e343-1626">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8e343-1627">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8e343-1627">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8e343-1628">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8e343-1628">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8e343-1629">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1629">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8e343-1630">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1630">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8e343-1631">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8e343-1631">Az.OperationalInsights</span></span>
- <span data-ttu-id="8e343-1632">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1632">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8e343-1633">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8e343-1633">Az.Profile</span></span>
- <span data-ttu-id="8e343-1634">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1634">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-1635">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1635">Az.RecoveryServices</span></span>
- <span data-ttu-id="8e343-1636">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1636">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8e343-1637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1637">Az.Resources</span></span>
- <span data-ttu-id="8e343-1638">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1638">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8e343-1639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e343-1639">Az.ServiceFabric</span></span>
- <span data-ttu-id="8e343-1640">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="8e343-1640">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8e343-1641">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1641">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8e343-1642">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8e343-1642">Az.SIgnalR</span></span>
- <span data-ttu-id="8e343-1643">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="8e343-1643">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8e343-1644">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1644">Az.Sql</span></span>
- <span data-ttu-id="8e343-1645">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1645">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8e343-1646">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1646">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8e343-1647">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1647">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8e343-1648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-1648">Az.Storage</span></span>
- <span data-ttu-id="8e343-1649">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8e343-1650">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-1650">Az.Websites</span></span>
- <span data-ttu-id="8e343-1651">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8e343-1651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8e343-1652">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="8e343-1652">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8e343-1653">Genel</span><span class="sxs-lookup"><span data-stu-id="8e343-1653">General</span></span>

* <span data-ttu-id="8e343-1654">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="8e343-1654">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8e343-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1655">Az.Compute</span></span>

* <span data-ttu-id="8e343-1656">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1656">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8e343-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-1657">Az.DataLakeStore</span></span>

* <span data-ttu-id="8e343-1658">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1658">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8e343-1659">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8e343-1659">Az.FrontDoor</span></span>

* <span data-ttu-id="8e343-1660">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1660">Fixed some broken links</span></span>
    - <span data-ttu-id="8e343-1661">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1661">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8e343-1662">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1662">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8e343-1663">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1663">Az.RecoveryServices</span></span>

* <span data-ttu-id="8e343-1664">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1664">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8e343-1665">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1665">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8e343-1666">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1666">Az.Resources</span></span>

* <span data-ttu-id="8e343-1667">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="8e343-1667">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8e343-1668">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1668">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8e343-1669">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1669">Az.Sql</span></span>

* <span data-ttu-id="8e343-1670">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="8e343-1670">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8e343-1671">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1671">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8e343-1672">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1672">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8e343-1673">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8e343-1673">Az.Storage</span></span>

* <span data-ttu-id="8e343-1674">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1674">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8e343-1675">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1675">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8e343-1676">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8e343-1676">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8e343-1677">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1677">Support Static Website configuration</span></span>
    - <span data-ttu-id="8e343-1678">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8e343-1678">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8e343-1679">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8e343-1679">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8e343-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-1680">Az.Websites</span></span>

* <span data-ttu-id="8e343-1681">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8e343-1681">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="8e343-1682">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1682">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8e343-1683">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="8e343-1683">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8e343-1684">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="8e343-1684">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8e343-1685">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e343-1685">Az.ApiManagement</span></span>
* <span data-ttu-id="8e343-1686">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="8e343-1686">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8e343-1687">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8e343-1687">Az.Automation</span></span>
* <span data-ttu-id="8e343-1688">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="8e343-1688">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8e343-1689">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1689">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8e343-1690">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1690">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8e343-1691">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1691">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8e343-1692">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1692">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8e343-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1693">Az.Compute</span></span>
* <span data-ttu-id="8e343-1694">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1694">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8e343-1695">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="8e343-1695">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8e343-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8e343-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="8e343-1697">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="8e343-1697">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8e343-1698">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8e343-1698">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8e343-1699">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1699">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8e343-1700">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-1700">Az.Network</span></span>
* <span data-ttu-id="8e343-1701">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1701">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8e343-1702">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1702">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8e343-1703">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1703">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="8e343-1704">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1704">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8e343-1705">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8e343-1705">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8e343-1706">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1706">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8e343-1707">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="8e343-1707">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8e343-1708">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8e343-1708">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8e343-1709">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1709">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8e343-1710">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="8e343-1710">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8e343-1711">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8e343-1711">Az.Relay</span></span>
* <span data-ttu-id="8e343-1712">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1712">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8e343-1713">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1713">Az.Resources</span></span>
* <span data-ttu-id="8e343-1714">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1714">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8e343-1715">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1715">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8e343-1716">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="8e343-1716">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8e343-1717">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e343-1717">Az.ServiceFabric</span></span>
* <span data-ttu-id="8e343-1718">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1718">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8e343-1719">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1719">Az.Sql</span></span>
* <span data-ttu-id="8e343-1720">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1720">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8e343-1721">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8e343-1721">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8e343-1722">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8e343-1722">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8e343-1723">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8e343-1723">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8e343-1724">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8e343-1724">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8e343-1725">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8e343-1725">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8e343-1726">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8e343-1726">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8e343-1727">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8e343-1727">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8e343-1728">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8e343-1728">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8e343-1729">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1729">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8e343-1730">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1730">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8e343-1731">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1731">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8e343-1732">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8e343-1732">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8e343-1733">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8e343-1733">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8e343-1734">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8e343-1734">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8e343-1735">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8e343-1735">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8e343-1736">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1736">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8e343-1737">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="8e343-1737">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8e343-1738">Genel</span><span class="sxs-lookup"><span data-stu-id="8e343-1738">General</span></span>
* <span data-ttu-id="8e343-1739">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="8e343-1739">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8e343-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8e343-1740">Az.Profile</span></span>
* <span data-ttu-id="8e343-1741">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1741">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8e343-1742">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1742">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8e343-1743">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1743">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8e343-1744">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1744">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8e343-1745">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1745">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8e343-1746">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1746">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8e343-1747">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1747">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8e343-1748">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1748">Az.CognitiveServices</span></span>
* <span data-ttu-id="8e343-1749">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1749">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1750">Az.Compute</span></span>
* <span data-ttu-id="8e343-1751">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1751">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8e343-1752">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="8e343-1752">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8e343-1753">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1753">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8e343-1754">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-1754">Az.DataLakeStore</span></span>
* <span data-ttu-id="8e343-1755">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1755">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8e343-1756">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1756">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8e343-1757">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8e343-1757">Az.Insights</span></span>
* <span data-ttu-id="8e343-1758">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1758">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8e343-1759">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="8e343-1759">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8e343-1760">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1760">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8e343-1761">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="8e343-1761">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-1762">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-1762">Az.Network</span></span>
* <span data-ttu-id="8e343-1763">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="8e343-1763">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8e343-1764">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e343-1764">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8e343-1765">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8e343-1765">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8e343-1766">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8e343-1766">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8e343-1767">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8e343-1767">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8e343-1768">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e343-1768">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8e343-1769">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8e343-1769">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8e343-1770">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8e343-1770">Az.PolicyInsights</span></span>
* <span data-ttu-id="8e343-1771">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1771">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-1772">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1772">Az.Resources</span></span>
* <span data-ttu-id="8e343-1773">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="8e343-1773">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8e343-1774">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="8e343-1774">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8e343-1775">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8e343-1775">Az.ServiceBus</span></span>
* <span data-ttu-id="8e343-1776">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1776">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8e343-1777">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e343-1777">Az.ServiceFabric</span></span>
* <span data-ttu-id="8e343-1778">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1778">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8e343-1779">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1779">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8e343-1780">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="8e343-1780">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8e343-1781">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="8e343-1781">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8e343-1782">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1782">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8e343-1783">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="8e343-1783">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8e343-1784">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8e343-1784">Az.Profile</span></span>
* <span data-ttu-id="8e343-1785">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="8e343-1785">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8e343-1786">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1786">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1787">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1787">Az.Compute</span></span>
* <span data-ttu-id="8e343-1788">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1788">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8e343-1789">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1789">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8e343-1790">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-1790">Az.DataLakeStore</span></span>
* <span data-ttu-id="8e343-1791">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="8e343-1791">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8e343-1792">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="8e343-1792">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8e343-1793">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="8e343-1793">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8e343-1794">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8e343-1794">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8e343-1795">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="8e343-1795">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-1796">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-1796">Az.Network</span></span>
* <span data-ttu-id="8e343-1797">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-1797">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8e343-1798">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1798">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-1799">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1799">Az.Resources</span></span>
* <span data-ttu-id="8e343-1800">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1800">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8e343-1801">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1801">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8e343-1802">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="8e343-1802">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8e343-1803">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="8e343-1803">Azure.Storage</span></span>
* <span data-ttu-id="8e343-1804">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="8e343-1804">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8e343-1805">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8e343-1805">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8e343-1806">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8e343-1806">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8e343-1807">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="8e343-1807">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8e343-1808">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8e343-1808">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="8e343-1809">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8e343-1809">Az.CognitiveServices</span></span>
* <span data-ttu-id="8e343-1810">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="8e343-1810">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8e343-1811">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8e343-1811">Az.Compute</span></span>
* <span data-ttu-id="8e343-1812">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1812">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8e343-1813">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1813">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8e343-1814">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1814">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8e343-1815">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8e343-1815">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8e343-1816">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1816">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8e343-1817">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8e343-1817">Az.Network</span></span>
* <span data-ttu-id="8e343-1818">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8e343-1818">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8e343-1819">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1819">new cmdlets added</span></span>
    - <span data-ttu-id="8e343-1820">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8e343-1820">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8e343-1821">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8e343-1821">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8e343-1822">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8e343-1822">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8e343-1823">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8e343-1823">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8e343-1824">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-1824">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8e343-1825">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8e343-1825">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8e343-1826">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1826">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8e343-1827">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1827">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8e343-1828">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1828">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8e343-1829">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8e343-1829">Az.RedisCache</span></span>
* <span data-ttu-id="8e343-1830">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="8e343-1830">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8e343-1831">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1831">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8e343-1832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8e343-1832">Az.Resources</span></span>
* <span data-ttu-id="8e343-1833">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8e343-1833">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8e343-1834">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1834">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8e343-1835">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8e343-1835">Az.Sql</span></span>
* <span data-ttu-id="8e343-1836">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8e343-1836">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8e343-1837">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8e343-1837">Az.Websites</span></span>
* <span data-ttu-id="8e343-1838">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="8e343-1838">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8e343-1839">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="8e343-1839">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8e343-1840">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="8e343-1840">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8e343-1841">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="8e343-1841">Initial Release</span></span>
