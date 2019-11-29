---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 2280b594ee9f525b2fa3175c917f6365cea354ba
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537116"
---
## <a name="310---november-2019"></a><span data-ttu-id="c117a-103">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-103">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c117a-104">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="c117a-104">Highlights since the last major release</span></span>
* <span data-ttu-id="c117a-105">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="c117a-105">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="c117a-106">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="c117a-106">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-107">Az.Compute</span></span>
* <span data-ttu-id="c117a-108">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="c117a-108">VM Reapply feature</span></span>
    - <span data-ttu-id="c117a-109">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="c117a-109">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="c117a-110">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="c117a-110">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="c117a-111">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c117a-111">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="c117a-112">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="c117a-112">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="c117a-113">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-113">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="c117a-114">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-114">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="c117a-115">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-115">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="c117a-116">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-116">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="c117a-117">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-117">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="c117a-118">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-118">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="c117a-119">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="c117a-119">Az.DataBoxEdge</span></span>
* <span data-ttu-id="c117a-120">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-120">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="c117a-121">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="c117a-121">Get the Order</span></span>
* <span data-ttu-id="c117a-122">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-122">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="c117a-123">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="c117a-123">Create new Order</span></span>
* <span data-ttu-id="c117a-124">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-124">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="c117a-125">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="c117a-125">Remove the Order</span></span>
* <span data-ttu-id="c117a-126">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="c117a-126">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="c117a-127">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="c117a-127">Now creates Local Share</span></span>
* <span data-ttu-id="c117a-128">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-128">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="c117a-129">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="c117a-129">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="c117a-130">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-130">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="c117a-131">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="c117a-131">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="c117a-132">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-132">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="c117a-133">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="c117a-133">Gets the information about Triggers</span></span>
* <span data-ttu-id="c117a-134">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-134">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="c117a-135">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="c117a-135">Create new Triggers</span></span>
* <span data-ttu-id="c117a-136">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-136">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="c117a-137">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="c117a-137">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c117a-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c117a-138">Az.DataFactory</span></span>
* <span data-ttu-id="c117a-139">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-139">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="c117a-140">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-140">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c117a-141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-141">Az.DataLakeStore</span></span>
* <span data-ttu-id="c117a-142">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-142">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c117a-143">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c117a-143">Az.EventHub</span></span>
* <span data-ttu-id="c117a-144">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-144">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c117a-145">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c117a-145">Az.FrontDoor</span></span>
* <span data-ttu-id="c117a-146">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-146">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="c117a-147">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-147">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="c117a-148">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-148">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="c117a-149">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="c117a-149">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-150">Az.Network</span></span>
* <span data-ttu-id="c117a-151">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-151">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="c117a-152">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="c117a-152">Az.PrivateDns</span></span>
* <span data-ttu-id="c117a-153">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-153">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-154">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-154">Az.RecoveryServices</span></span>
* <span data-ttu-id="c117a-155">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-155">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="c117a-156">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="c117a-156">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="c117a-157">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-157">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c117a-158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c117a-158">Az.RedisCache</span></span>
* <span data-ttu-id="c117a-159">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-159">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="c117a-160">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-160">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="c117a-161">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-161">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-162">Az.Resources</span></span>
- <span data-ttu-id="c117a-163">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-163">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="c117a-164">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-164">Updated create policy definition help example</span></span>
- <span data-ttu-id="c117a-165">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-165">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="c117a-166">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-166">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="c117a-167">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-167">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-168">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-168">Az.Sql</span></span>
* <span data-ttu-id="c117a-169">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-169">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="c117a-170">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-170">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="c117a-171">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-171">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="c117a-172">Genel</span><span class="sxs-lookup"><span data-stu-id="c117a-172">General</span></span>
* <span data-ttu-id="c117a-173">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="c117a-173">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c117a-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-174">Az.Accounts</span></span>
* <span data-ttu-id="c117a-175">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c117a-175">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="c117a-176">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="c117a-176">Az.Advisor</span></span>
* <span data-ttu-id="c117a-177">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-177">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c117a-178">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c117a-178">Az.Batch</span></span>
* <span data-ttu-id="c117a-179">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-179">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="c117a-180">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="c117a-180">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="c117a-181">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-181">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="c117a-182">**New-AzBatchTask** `-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet'i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-182">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="c117a-183">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="c117a-183">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="c117a-184">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c117a-184">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="c117a-185">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="c117a-185">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="c117a-186">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-186">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="c117a-187">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-187">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="c117a-188">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-188">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="c117a-189">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="c117a-189">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="c117a-190">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="c117a-190">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="c117a-191">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-191">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="c117a-192">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="c117a-192">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="c117a-193">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-193">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="c117a-194">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-194">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="c117a-195">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-195">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="c117a-196">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-196">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="c117a-197">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-197">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="c117a-198">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-198">This operation is no longer supported.</span></span>
* <span data-ttu-id="c117a-199">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-199">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="c117a-200">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-200">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="c117a-201">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-201">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="c117a-202">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-202">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="c117a-203">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-203">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="c117a-204">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-204">New non-verified images are also now returned.</span></span> <span data-ttu-id="c117a-205">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-205">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="c117a-206">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-206">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="c117a-207">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-207">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="c117a-208">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-208">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="c117a-209">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-209">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="c117a-210">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-210">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="c117a-211">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-211">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="c117a-212">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-212">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="c117a-213">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="c117a-213">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="c117a-214">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="c117a-214">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c117a-215">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c117a-215">Az.Cdn</span></span>
* <span data-ttu-id="c117a-216">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-216">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="c117a-217">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-217">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-218">Az.Compute</span></span>
* <span data-ttu-id="c117a-219">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="c117a-219">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="c117a-220">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c117a-220">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="c117a-221">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="c117a-221">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="c117a-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c117a-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="c117a-223">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-223">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="c117a-224">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-224">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="c117a-225">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="c117a-225">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="c117a-226">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-226">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="c117a-227">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c117a-227">Breaking changes</span></span>
    - <span data-ttu-id="c117a-228">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="c117a-228">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="c117a-229">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="c117a-229">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c117a-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c117a-230">Az.DataFactory</span></span>
* <span data-ttu-id="c117a-231">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-231">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c117a-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-232">Az.DataLakeStore</span></span>
* <span data-ttu-id="c117a-233">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="c117a-233">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="c117a-234">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="c117a-234">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="c117a-235">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="c117a-235">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="c117a-236">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="c117a-236">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="c117a-237">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="c117a-237">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="c117a-238">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="c117a-238">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c117a-239">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c117a-239">Az.FrontDoor</span></span>
* <span data-ttu-id="c117a-240">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-240">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c117a-241">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c117a-241">Az.HDInsight</span></span>
* <span data-ttu-id="c117a-242">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-242">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="c117a-243">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-243">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="c117a-244">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-244">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="c117a-245">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="c117a-245">Removed five cmdlets:</span></span>
    - <span data-ttu-id="c117a-246">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="c117a-246">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="c117a-247">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="c117a-247">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="c117a-248">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="c117a-248">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="c117a-249">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c117a-249">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="c117a-250">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c117a-250">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="c117a-251">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="c117a-251">Added three cmdlets:</span></span>
    - <span data-ttu-id="c117a-252">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="c117a-252">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="c117a-253">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="c117a-253">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="c117a-254">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="c117a-254">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="c117a-255">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-255">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="c117a-256">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-256">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="c117a-257">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-257">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="c117a-258">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-258">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="c117a-259">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-259">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="c117a-260">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-260">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="c117a-261">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-261">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="c117a-262">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-262">Added some scenario test cases.</span></span>
* <span data-ttu-id="c117a-263">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="c117a-263">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c117a-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c117a-264">Az.IotHub</span></span>
* <span data-ttu-id="c117a-265">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="c117a-265">Breaking changes:</span></span>
    - <span data-ttu-id="c117a-266">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="c117a-266">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="c117a-267">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-267">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="c117a-268">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="c117a-268">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="c117a-269">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-269">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="c117a-270">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-270">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="c117a-271">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-271">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="c117a-272">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-272">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="c117a-273">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-273">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="c117a-274">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="c117a-274">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="c117a-275">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-275">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="c117a-276">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="c117a-276">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="c117a-277">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-277">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="c117a-279">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-279">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="c117a-280">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-280">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="c117a-281">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-281">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="c117a-282">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-282">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="c117a-283">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-283">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="c117a-284">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-284">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="c117a-285">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-285">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="c117a-286">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-286">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="c117a-287">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-287">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-288">Az.Resources</span></span>
* <span data-ttu-id="c117a-289">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-289">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-290">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-290">Az.Network</span></span>
* <span data-ttu-id="c117a-291">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-291">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="c117a-292">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-292">Updated cmdlet:</span></span>
        - <span data-ttu-id="c117a-293">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-293">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c117a-294">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-294">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c117a-295">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-295">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c117a-296">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-296">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c117a-297">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-297">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="c117a-298">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-298">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="c117a-299">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c117a-299">New cmdlet:</span></span>
        - <span data-ttu-id="c117a-300">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="c117a-300">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="c117a-301">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-301">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="c117a-302">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-302">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="c117a-303">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-303">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="c117a-304">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-304">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="c117a-305">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-305">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="c117a-306">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-306">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="c117a-307">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-307">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="c117a-308">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c117a-308">New cmdlets added:</span></span>
        - <span data-ttu-id="c117a-309">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="c117a-309">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="c117a-310">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c117a-310">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="c117a-311">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c117a-311">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="c117a-312">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c117a-312">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="c117a-313">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c117a-313">Set-AzVirtualHub</span></span>
* <span data-ttu-id="c117a-314">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-314">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="c117a-315">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-315">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="c117a-316">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-316">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="c117a-317">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-317">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="c117a-318">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-318">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="c117a-319">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-319">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="c117a-320">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-320">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="c117a-321">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c117a-321">New cmdlets added:</span></span>
        - <span data-ttu-id="c117a-322">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-322">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="c117a-323">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-323">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="c117a-324">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-324">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="c117a-325">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-325">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="c117a-326">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-326">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="c117a-327">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-327">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="c117a-328">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-328">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="c117a-329">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-329">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="c117a-330">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c117a-330">New cmdlets added:</span></span>
        - <span data-ttu-id="c117a-331">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="c117a-331">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="c117a-332">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="c117a-332">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="c117a-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="c117a-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="c117a-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="c117a-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="c117a-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="c117a-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="c117a-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="c117a-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="c117a-337">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-337">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="c117a-338">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-338">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="c117a-339">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-339">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="c117a-340">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-340">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="c117a-341">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-341">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="c117a-342">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-342">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="c117a-343">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-343">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="c117a-344">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-344">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="c117a-345">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-345">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="c117a-346">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="c117a-346">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="c117a-347">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-347">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="c117a-348">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c117a-348">New cmdlets added:</span></span>
        - <span data-ttu-id="c117a-349">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c117a-349">New-AzIpGroup</span></span>
        - <span data-ttu-id="c117a-350">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c117a-350">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="c117a-351">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c117a-351">Get-AzIpGroup</span></span>
        - <span data-ttu-id="c117a-352">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c117a-352">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c117a-353">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c117a-353">Az.ServiceFabric</span></span>
* <span data-ttu-id="c117a-354">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-354">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-355">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-355">Az.Sql</span></span>
* <span data-ttu-id="c117a-356">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-356">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="c117a-357">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-357">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="c117a-358">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="c117a-358">Removed deprecated aliases:</span></span>
* <span data-ttu-id="c117a-359">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="c117a-359">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="c117a-360">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="c117a-360">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="c117a-361">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-361">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="c117a-362">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-362">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="c117a-363">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-363">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="c117a-364">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-364">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-365">Az.Storage</span></span>
* <span data-ttu-id="c117a-366">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="c117a-366">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="c117a-367">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c117a-367">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="c117a-368">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c117a-368">Set-AzStorageAccount</span></span>
* <span data-ttu-id="c117a-369">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="c117a-369">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="c117a-370">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c117a-370">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="c117a-371">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c117a-371">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="c117a-372">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-372">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="c117a-373">Genel</span><span class="sxs-lookup"><span data-stu-id="c117a-373">General</span></span>
* <span data-ttu-id="c117a-374">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="c117a-374">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c117a-375">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-375">Az.Accounts</span></span>
* <span data-ttu-id="c117a-376">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-376">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c117a-377">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c117a-377">Az.ApiManagement</span></span>
* <span data-ttu-id="c117a-378">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-378">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="c117a-379">https://github.com/Azure/azure-powershell/issues/10068 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-379">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c117a-380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c117a-380">Az.Automation</span></span>
* <span data-ttu-id="c117a-381">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-381">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="c117a-382">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c117a-382">Az.Batch</span></span>
* <span data-ttu-id="c117a-383">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="c117a-383">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-384">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-384">Az.Compute</span></span>
* <span data-ttu-id="c117a-385">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-385">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="c117a-386">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-386">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="c117a-387">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-387">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="c117a-388">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-388">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c117a-389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c117a-389">Az.DataFactory</span></span>
* <span data-ttu-id="c117a-390">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="c117a-390">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="c117a-391">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="c117a-391">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="c117a-392">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-392">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c117a-393">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-393">Az.DataLakeStore</span></span>
* <span data-ttu-id="c117a-394">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-394">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="c117a-395">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="c117a-395">Az.HealthcareApis</span></span>
* <span data-ttu-id="c117a-396">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-396">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="c117a-397">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-397">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="c117a-398">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-398">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="c117a-399">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-399">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c117a-400">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c117a-400">Az.IotHub</span></span>
* <span data-ttu-id="c117a-401">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="c117a-401">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="c117a-402">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="c117a-402">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="c117a-403">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c117a-403">Az.Monitor</span></span>
* <span data-ttu-id="c117a-404">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-404">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="c117a-405">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="c117a-405">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="c117a-406">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="c117a-406">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="c117a-407">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-407">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-408">Az.Network</span></span>
* <span data-ttu-id="c117a-409">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-409">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="c117a-410">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-410">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="c117a-411">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c117a-411">New cmdlets added:</span></span>
        - <span data-ttu-id="c117a-412">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="c117a-412">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="c117a-413">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-413">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c117a-414">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-414">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="c117a-415">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-415">Updated cmdlets:</span></span>
        - <span data-ttu-id="c117a-416">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-416">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c117a-417">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-417">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c117a-418">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-418">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="c117a-419">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-419">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="c117a-420">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="c117a-420">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="c117a-421">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="c117a-421">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="c117a-422">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="c117a-422">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c117a-423">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c117a-423">Az.RedisCache</span></span>
* <span data-ttu-id="c117a-424">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-424">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-425">Az.Sql</span></span>
* <span data-ttu-id="c117a-426">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-426">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-427">Az.Storage</span></span>
* <span data-ttu-id="c117a-428">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-428">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="c117a-429">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="c117a-429">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="c117a-430">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c117a-430">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="c117a-431">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="c117a-431">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="c117a-432">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c117a-432">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c117a-433">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c117a-433">Az.StorageSync</span></span>
* <span data-ttu-id="c117a-434">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-434">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-435">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-435">Az.Websites</span></span>
* <span data-ttu-id="c117a-436">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="c117a-436">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="c117a-437">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-437">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="c117a-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c117a-438">Az.ApiManagement</span></span>
* <span data-ttu-id="c117a-439">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-439">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="c117a-440">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-440">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="c117a-441">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="c117a-441">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c117a-442">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c117a-442">Az.Automation</span></span>
* <span data-ttu-id="c117a-443">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-443">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="c117a-444">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-444">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="c117a-445">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-445">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-446">Az.Compute</span></span>
* <span data-ttu-id="c117a-447">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-447">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="c117a-448">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-448">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="c117a-449">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="c117a-449">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="c117a-450">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-450">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="c117a-451">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-451">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="c117a-452">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-452">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="c117a-453">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-453">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="c117a-454">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-454">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="c117a-455">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-455">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c117a-456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c117a-456">Az.DataFactory</span></span>
* <span data-ttu-id="c117a-457">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="c117a-457">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="c117a-458">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-458">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c117a-459">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c117a-459">Az.HDInsight</span></span>
* <span data-ttu-id="c117a-460">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="c117a-460">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c117a-461">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c117a-461">Az.IotHub</span></span>
* <span data-ttu-id="c117a-462">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-462">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="c117a-463">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-463">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="c117a-464">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c117a-464">New cmdlets are:</span></span>
    - <span data-ttu-id="c117a-465">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c117a-465">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="c117a-466">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c117a-466">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="c117a-467">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c117a-467">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="c117a-468">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c117a-468">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c117a-469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c117a-469">Az.Monitor</span></span>
* <span data-ttu-id="c117a-470">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="c117a-470">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="c117a-471">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="c117a-471">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="c117a-472">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="c117a-472">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="c117a-473">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="c117a-473">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="c117a-474">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-474">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="c117a-475">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-475">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="c117a-476">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="c117a-476">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="c117a-477">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="c117a-477">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="c117a-478">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-478">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="c117a-479">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="c117a-479">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="c117a-480">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-480">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="c117a-481">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="c117a-481">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="c117a-482">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-482">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="c117a-483">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="c117a-483">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="c117a-484">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="c117a-484">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="c117a-485">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="c117a-485">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="c117a-486">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="c117a-486">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="c117a-487">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="c117a-487">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="c117a-488">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-488">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="c117a-489">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-489">Overall improved help files</span></span>
* <span data-ttu-id="c117a-490">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-490">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-491">Az.Network</span></span>
* <span data-ttu-id="c117a-492">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-492">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="c117a-493">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-493">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="c117a-494">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-494">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="c117a-495">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-495">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="c117a-496">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-496">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="c117a-497">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-497">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="c117a-498">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-498">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="c117a-499">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-499">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="c117a-500">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-500">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="c117a-501">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-501">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="c117a-502">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-502">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="c117a-503">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="c117a-503">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="c117a-504">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-504">New cmdlets</span></span>
        - <span data-ttu-id="c117a-505">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c117a-505">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="c117a-506">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-506">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="c117a-507">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-507">Updated cmdlet:</span></span>
        - <span data-ttu-id="c117a-508">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="c117a-508">New-VpnSite</span></span>
        - <span data-ttu-id="c117a-509">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="c117a-509">Update-VpnSite</span></span>
        - <span data-ttu-id="c117a-510">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-510">New-VpnConnection</span></span>
        - <span data-ttu-id="c117a-511">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-511">Update-VpnConnection</span></span>
* <span data-ttu-id="c117a-512">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-512">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-513">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-513">Az.RecoveryServices</span></span>
* <span data-ttu-id="c117a-514">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-514">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="c117a-515">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-515">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-516">Az.Resources</span></span>
* <span data-ttu-id="c117a-517">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-517">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c117a-518">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c117a-518">Az.ServiceFabric</span></span>
* <span data-ttu-id="c117a-519">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-519">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="c117a-520">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="c117a-520">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="c117a-521">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c117a-521">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c117a-522">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c117a-522">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="c117a-523">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c117a-523">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="c117a-524">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c117a-524">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="c117a-525">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c117a-525">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c117a-526">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c117a-526">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c117a-527">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c117a-527">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="c117a-528">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c117a-528">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="c117a-529">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c117a-529">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="c117a-530">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c117a-530">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c117a-531">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c117a-531">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="c117a-532">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c117a-532">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="c117a-533">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="c117a-533">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="c117a-534">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-534">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c117a-535">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c117a-535">Az.SignalR</span></span>
* <span data-ttu-id="c117a-536">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-536">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-537">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-537">Az.Sql</span></span>
* <span data-ttu-id="c117a-538">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-538">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="c117a-539">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-539">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="c117a-540">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-540">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="c117a-541">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-541">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="c117a-542">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-542">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-543">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-543">Az.Storage</span></span>
* <span data-ttu-id="c117a-544">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-544">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="c117a-545">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-545">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="c117a-546">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c117a-546">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="c117a-547">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c117a-547">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="c117a-548">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-548">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="c117a-549">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c117a-549">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="c117a-550">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-550">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="c117a-551">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c117a-551">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="c117a-552">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c117a-552">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="c117a-553">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c117a-553">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="c117a-554">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c117a-554">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-555">Az.Websites</span></span>
* <span data-ttu-id="c117a-556">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="c117a-556">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="c117a-557">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="c117a-557">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="c117a-558">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-558">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="c117a-559">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-559">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="c117a-560">Genel</span><span class="sxs-lookup"><span data-stu-id="c117a-560">General</span></span>
* <span data-ttu-id="c117a-561">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-561">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c117a-562">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-562">Az.Accounts</span></span>
* <span data-ttu-id="c117a-563">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="c117a-563">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="c117a-564">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c117a-564">Az.Aks</span></span>
* <span data-ttu-id="c117a-565">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-565">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="c117a-566">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="c117a-566">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c117a-567">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c117a-567">Az.ApiManagement</span></span>
* <span data-ttu-id="c117a-568">https://github.com/Azure/azure-powershell/issues/9351 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-568">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="c117a-569">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-569">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="c117a-570">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-570">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="c117a-571">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="c117a-571">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="c117a-572">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-572">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c117a-573">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c117a-573">Az.Batch</span></span>
* <span data-ttu-id="c117a-574">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-574">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c117a-575">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c117a-575">Az.Cdn</span></span>
* <span data-ttu-id="c117a-576">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-576">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-577">Az.Compute</span></span>
* <span data-ttu-id="c117a-578">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-578">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="c117a-579">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-579">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="c117a-580">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-580">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="c117a-581">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-581">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="c117a-582">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="c117a-582">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="c117a-583">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-583">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="c117a-584">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-584">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="c117a-585">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-585">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c117a-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c117a-586">Az.DataFactory</span></span>
* <span data-ttu-id="c117a-587">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-587">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="c117a-588">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-588">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="c117a-589">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-589">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="c117a-590">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-590">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c117a-591">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-591">Az.DataLakeStore</span></span>
* <span data-ttu-id="c117a-592">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-592">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c117a-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c117a-593">Az.EventHub</span></span>
* <span data-ttu-id="c117a-594">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="c117a-594">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="c117a-595">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="c117a-595">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="c117a-596">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-596">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="c117a-597">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="c117a-597">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="c117a-598">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c117a-598">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c117a-599">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-599">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c117a-600">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c117a-600">Az.Monitor</span></span>
* <span data-ttu-id="c117a-601">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-601">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-602">Az.Network</span></span>
* <span data-ttu-id="c117a-603">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-603">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="c117a-604">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-604">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="c117a-605">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-605">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="c117a-606">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="c117a-606">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="c117a-607">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="c117a-607">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="c117a-608">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-608">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="c117a-609">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-609">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c117a-610">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c117a-610">Az.OperationalInsights</span></span>
* <span data-ttu-id="c117a-611">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-611">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="c117a-612">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-612">Added example</span></span>
    - <span data-ttu-id="c117a-613">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-613">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="c117a-614">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-614">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="c117a-615">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-615">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-616">Az.RecoveryServices</span></span>
* <span data-ttu-id="c117a-617">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-617">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-618">Az.Resources</span></span>
* <span data-ttu-id="c117a-619">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-619">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="c117a-620">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-620">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="c117a-621">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="c117a-621">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="c117a-622">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-622">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c117a-623">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c117a-623">Az.ServiceBus</span></span>
* <span data-ttu-id="c117a-624">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="c117a-624">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="c117a-625">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="c117a-625">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="c117a-626">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-626">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="c117a-627">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c117a-627">Az.ServiceFabric</span></span>
* <span data-ttu-id="c117a-628">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-628">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="c117a-629">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="c117a-629">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="c117a-630">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="c117a-630">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="c117a-631">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-631">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="c117a-632">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="c117a-632">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="c117a-633">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-633">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-634">Az.Sql</span></span>
* <span data-ttu-id="c117a-635">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-635">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-636">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-636">Az.Storage</span></span>
* <span data-ttu-id="c117a-637">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-637">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="c117a-638">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="c117a-638">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="c117a-639">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c117a-639">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="c117a-640">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c117a-640">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="c117a-641">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="c117a-641">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="c117a-642">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c117a-642">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-643">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-643">Az.Websites</span></span>
* <span data-ttu-id="c117a-644">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-644">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="c117a-645">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-645">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c117a-646">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-646">Az.Accounts</span></span>
* <span data-ttu-id="c117a-647">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-647">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="c117a-648">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c117a-648">Az.ApplicationInsights</span></span>
* <span data-ttu-id="c117a-649">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-649">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="c117a-650">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c117a-650">Az.Automation</span></span>
* <span data-ttu-id="c117a-651">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-651">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="c117a-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c117a-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="c117a-653">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-653">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-654">Az.Compute</span></span>
* <span data-ttu-id="c117a-655">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-655">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="c117a-656">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c117a-656">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c117a-657">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-657">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="c117a-658">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="c117a-658">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c117a-659">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c117a-659">Az.DataFactory</span></span>
* <span data-ttu-id="c117a-660">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-660">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="c117a-661">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-661">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c117a-662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c117a-662">Az.EventHub</span></span>
* <span data-ttu-id="c117a-663">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="c117a-663">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="c117a-664">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-664">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c117a-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c117a-665">Az.KeyVault</span></span>
* <span data-ttu-id="c117a-666">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-666">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c117a-667">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c117a-667">Az.LogicApp</span></span>
* <span data-ttu-id="c117a-668">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="c117a-668">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="c117a-669">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-669">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="c117a-670">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="c117a-670">Az.ManagedServices</span></span>
* <span data-ttu-id="c117a-671">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="c117a-671">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-672">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-672">Az.Network</span></span>
* <span data-ttu-id="c117a-673">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-673">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="c117a-674">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-674">New cmdlets</span></span>
        - <span data-ttu-id="c117a-675">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c117a-675">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c117a-676">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c117a-676">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c117a-677">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-677">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c117a-678">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-678">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c117a-679">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-679">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c117a-680">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-680">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c117a-681">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="c117a-681">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="c117a-682">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c117a-682">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="c117a-683">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="c117a-683">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="c117a-684">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-684">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="c117a-685">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-685">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="c117a-686">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-686">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="c117a-687">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-687">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="c117a-688">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-688">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="c117a-689">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-689">Updated cmdlets</span></span>
        - <span data-ttu-id="c117a-690">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-690">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c117a-691">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-691">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c117a-692">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-692">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="c117a-693">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-693">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c117a-694">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-694">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="c117a-695">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-695">Updated cmdlet:</span></span>
        - <span data-ttu-id="c117a-696">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-696">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="c117a-697">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-697">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="c117a-698">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-698">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="c117a-699">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-699">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="c117a-700">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-700">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="c117a-701">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="c117a-701">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c117a-702">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c117a-702">Az.OperationalInsights</span></span>
* <span data-ttu-id="c117a-703">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-703">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="c117a-704">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-704">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-705">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-705">Az.RecoveryServices</span></span>
* <span data-ttu-id="c117a-706">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-706">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="c117a-707">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-707">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="c117a-708">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-708">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="c117a-709">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-709">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="c117a-710">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-710">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="c117a-711">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-711">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="c117a-712">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-712">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="c117a-713">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-713">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="c117a-714">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-714">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="c117a-715">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-715">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-716">Az.Resources</span></span>
- <span data-ttu-id="c117a-717">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-717">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="c117a-718">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-718">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c117a-719">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c117a-719">Az.ServiceBus</span></span>
* <span data-ttu-id="c117a-720">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="c117a-720">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="c117a-721">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-721">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-722">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-722">Az.Sql</span></span>
* <span data-ttu-id="c117a-723">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-723">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="c117a-724">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-724">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="c117a-725">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-725">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-726">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-726">Az.Storage</span></span>
* <span data-ttu-id="c117a-727">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-727">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c117a-728">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c117a-728">Az.StorageSync</span></span>
* <span data-ttu-id="c117a-729">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-729">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="c117a-730">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-730">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-731">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-731">Az.Websites</span></span>
* <span data-ttu-id="c117a-732">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-732">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="c117a-733">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-733">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="c117a-734">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-734">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="c117a-735">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-735">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c117a-736">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-736">Az.Accounts</span></span>
* <span data-ttu-id="c117a-737">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-737">Add support for profile cmdlets</span></span>
* <span data-ttu-id="c117a-738">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-738">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="c117a-739">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-739">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="c117a-740">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="c117a-740">Az.Advisor</span></span>
* <span data-ttu-id="c117a-741">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c117a-741">GA release of Az.Advisor</span></span>
* <span data-ttu-id="c117a-742">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="c117a-742">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c117a-743">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c117a-743">Az.ApiManagement</span></span>
* <span data-ttu-id="c117a-744">https://github.com/Azure/azure-powershell/issues/8671 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-744">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="c117a-745">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="c117a-745">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="c117a-746">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-746">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="c117a-747">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="c117a-747">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="c117a-748">https://github.com/Azure/azure-powershell/issues/9307 ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="c117a-748">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="c117a-749">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="c117a-749">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="c117a-750">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-750">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c117a-751">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c117a-751">Az.Automation</span></span>
* <span data-ttu-id="c117a-752">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-752">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-753">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-753">Az.Compute</span></span>
* <span data-ttu-id="c117a-754">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-754">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c117a-755">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c117a-755">Az.DataFactory</span></span>
* <span data-ttu-id="c117a-756">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-756">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c117a-757">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c117a-757">Az.EventGrid</span></span>
* <span data-ttu-id="c117a-758">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-758">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c117a-759">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c117a-759">Az.IotHub</span></span>
* <span data-ttu-id="c117a-760">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-760">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-761">Az.Network</span></span>
* <span data-ttu-id="c117a-762">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-762">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="c117a-763">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-763">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c117a-764">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c117a-764">Az.PolicyInsights</span></span>
* <span data-ttu-id="c117a-765">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-765">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="c117a-766">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="c117a-766">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c117a-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c117a-767">Az.OperationalInsights</span></span>
* <span data-ttu-id="c117a-768">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-768">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-769">Az.RecoveryServices</span></span>
* <span data-ttu-id="c117a-770">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c117a-770">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-771">Az.Resources</span></span>
    - <span data-ttu-id="c117a-772">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c117a-772">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="c117a-773">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-773">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="c117a-774">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-774">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="c117a-775">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-775">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c117a-776">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c117a-776">Az.ServiceBus</span></span>
* <span data-ttu-id="c117a-777">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-777">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-778">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-778">Az.Sql</span></span>
* <span data-ttu-id="c117a-779">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-779">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="c117a-780">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-780">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="c117a-781">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c117a-781">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="c117a-782">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c117a-782">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="c117a-783">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c117a-783">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="c117a-784">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c117a-784">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="c117a-785">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c117a-785">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="c117a-786">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c117a-786">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="c117a-787">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-787">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-788">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-788">Az.Storage</span></span>
* <span data-ttu-id="c117a-789">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-789">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="c117a-790">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c117a-790">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="c117a-791">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-791">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="c117a-792">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="c117a-792">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="c117a-793">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-793">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="c117a-794">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c117a-794">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="c117a-795">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c117a-795">Set-AzStorageAccount</span></span>
* <span data-ttu-id="c117a-796">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-796">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="c117a-797">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c117a-797">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="c117a-798">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c117a-798">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c117a-799">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c117a-799">Az.StorageSync</span></span>
* <span data-ttu-id="c117a-800">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="c117a-800">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="c117a-801">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-801">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c117a-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-802">Az.Accounts</span></span>
* <span data-ttu-id="c117a-803">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-803">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="c117a-804">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="c117a-804">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="c117a-805">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-805">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="c117a-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c117a-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="c117a-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="c117a-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-808">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-808">Az.Compute</span></span>
* <span data-ttu-id="c117a-809">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-809">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="c117a-810">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-810">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="c117a-811">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="c117a-811">Az.Dns</span></span>
* <span data-ttu-id="c117a-812">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-812">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c117a-813">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c117a-813">Az.EventGrid</span></span>
* <span data-ttu-id="c117a-814">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-814">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="c117a-815">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="c117a-815">New cmdlets:</span></span>
    - <span data-ttu-id="c117a-816">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c117a-816">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="c117a-817">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c117a-817">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="c117a-818">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c117a-818">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="c117a-819">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="c117a-819">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="c117a-820">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c117a-820">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="c117a-821">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c117a-821">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="c117a-822">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="c117a-822">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="c117a-823">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="c117a-823">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="c117a-824">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="c117a-824">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="c117a-825">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="c117a-825">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="c117a-826">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="c117a-826">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="c117a-827">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c117a-827">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="c117a-828">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="c117a-828">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="c117a-829">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="c117a-829">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="c117a-830">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="c117a-830">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="c117a-831">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c117a-831">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="c117a-832">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-832">Updated cmdlets:</span></span>
    - <span data-ttu-id="c117a-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="c117a-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="c117a-834">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="c117a-834">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="c117a-835">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="c117a-835">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="c117a-836">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="c117a-836">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="c117a-837">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c117a-837">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="c117a-838">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="c117a-838">Event subscription expiration date,</span></span>
            - <span data-ttu-id="c117a-839">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="c117a-839">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="c117a-840">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="c117a-840">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="c117a-841">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="c117a-841">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="c117a-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="c117a-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="c117a-843">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="c117a-843">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="c117a-844">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c117a-844">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="c117a-845">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="c117a-845">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="c117a-846">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="c117a-846">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c117a-847">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c117a-847">Az.FrontDoor</span></span>
* <span data-ttu-id="c117a-848">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="c117a-848">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="c117a-849">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="c117a-849">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="c117a-850">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="c117a-850">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="c117a-851">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="c117a-851">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-852">Az.Network</span></span>
* <span data-ttu-id="c117a-853">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="c117a-853">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="c117a-854">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-854">New cmdlets</span></span>
        - <span data-ttu-id="c117a-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="c117a-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="c117a-856">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="c117a-856">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="c117a-857">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-857">New cmdlets</span></span> 
        - <span data-ttu-id="c117a-858">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="c117a-858">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="c117a-859">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="c117a-859">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="c117a-860">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-860">New cmdlets</span></span> 
        - <span data-ttu-id="c117a-861">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c117a-861">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="c117a-862">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c117a-862">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c117a-863">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c117a-863">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c117a-864">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-864">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="c117a-865">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-865">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="c117a-866">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="c117a-866">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="c117a-867">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-867">New cmdlets</span></span>
        - <span data-ttu-id="c117a-868">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c117a-868">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c117a-869">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c117a-869">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c117a-870">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c117a-870">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c117a-871">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="c117a-871">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="c117a-872">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="c117a-872">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="c117a-873">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-873">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="c117a-874">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-874">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="c117a-875">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-875">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="c117a-876">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-876">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="c117a-877">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-877">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="c117a-878">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-878">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="c117a-879">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-879">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="c117a-880">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-880">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="c117a-881">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-881">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="c117a-882">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-882">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="c117a-883">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-883">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="c117a-884">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-884">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="c117a-885">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-885">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="c117a-886">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-886">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="c117a-887">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-887">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="c117a-888">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-888">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="c117a-889">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c117a-889">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="c117a-890">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c117a-890">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="c117a-891">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="c117a-891">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="c117a-892">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-892">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="c117a-893">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-893">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="c117a-894">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-894">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c117a-895">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c117a-895">Az.OperationalInsights</span></span>
* <span data-ttu-id="c117a-896">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-896">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-897">Az.Resources</span></span>
* <span data-ttu-id="c117a-898">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="c117a-898">Support for additional Template Export options</span></span>
    - <span data-ttu-id="c117a-899">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-899">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="c117a-900">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-900">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="c117a-901">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-901">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c117a-902">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c117a-902">Az.ServiceFabric</span></span>
* <span data-ttu-id="c117a-903">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-903">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-904">Az.Sql</span></span>
* <span data-ttu-id="c117a-905">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-905">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="c117a-906">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-906">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="c117a-907">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-907">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="c117a-908">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c117a-908">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="c117a-909">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c117a-909">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="c117a-910">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c117a-910">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="c117a-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c117a-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="c117a-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c117a-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-913">Az.Storage</span></span>
* <span data-ttu-id="c117a-914">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="c117a-914">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="c117a-915">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c117a-915">New-AzStorageAccount</span></span>
* <span data-ttu-id="c117a-916">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-916">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="c117a-917">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c117a-917">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-918">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-918">Az.Websites</span></span>
* <span data-ttu-id="c117a-919">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="c117a-919">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="c117a-920">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="c117a-920">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="c117a-921">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-921">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="c117a-922">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c117a-922">Az.Cdn</span></span>
* <span data-ttu-id="c117a-923">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-923">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-924">Az.Compute</span></span>
* <span data-ttu-id="c117a-925">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-925">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="c117a-926">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="c117a-926">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c117a-927">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c117a-927">Az.EventHub</span></span>
* <span data-ttu-id="c117a-928">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c117a-928">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="c117a-929">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c117a-929">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-930">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-930">Az.Network</span></span>
* <span data-ttu-id="c117a-931">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-931">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="c117a-932">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-932">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c117a-933">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c117a-933">Az.PolicyInsights</span></span>
* <span data-ttu-id="c117a-934">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-934">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-935">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-935">Az.RecoveryServices</span></span>
* <span data-ttu-id="c117a-936">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-936">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c117a-937">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c117a-937">Az.ServiceBus</span></span>
* <span data-ttu-id="c117a-938">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="c117a-938">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c117a-939">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c117a-939">Az.ServiceFabric</span></span>
* <span data-ttu-id="c117a-940">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-940">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="c117a-941">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-941">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-942">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-942">Az.Sql</span></span>
* <span data-ttu-id="c117a-943">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-943">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="c117a-944">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-944">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="c117a-945">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-945">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="c117a-946">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="c117a-946">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-947">Az.Websites</span></span>
* <span data-ttu-id="c117a-948">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="c117a-948">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="c117a-949">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-949">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="c117a-950">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c117a-950">Az.ApiManagement</span></span>
* <span data-ttu-id="c117a-951">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c117a-951">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="c117a-952">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="c117a-952">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="c117a-953">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="c117a-953">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="c117a-954">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="c117a-954">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="c117a-955">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c117a-955">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="c117a-956">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="c117a-956">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="c117a-957">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="c117a-957">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="c117a-958">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c117a-958">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="c117a-959">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c117a-959">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="c117a-960">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="c117a-960">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="c117a-961">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="c117a-961">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="c117a-962">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="c117a-962">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="c117a-963">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c117a-963">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="c117a-964">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c117a-964">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="c117a-965">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="c117a-965">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="c117a-966">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="c117a-966">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="c117a-967">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="c117a-967">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="c117a-968">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c117a-968">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="c117a-969">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="c117a-969">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="c117a-970">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="c117a-970">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="c117a-971">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c117a-971">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="c117a-972">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c117a-972">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="c117a-973">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="c117a-973">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="c117a-974">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-974">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="c117a-975">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-975">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="c117a-976">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-976">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="c117a-977">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="c117a-977">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="c117a-978">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c117a-978">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="c117a-979">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-979">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="c117a-980">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-980">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="c117a-981">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-981">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="c117a-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="c117a-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="c117a-983">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-983">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="c117a-984">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-984">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="c117a-985">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="c117a-985">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="c117a-986">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="c117a-986">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="c117a-987">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="c117a-987">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="c117a-988">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-988">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="c117a-989">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-989">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="c117a-990">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-990">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="c117a-991">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="c117a-991">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="c117a-992">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="c117a-992">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="c117a-993">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="c117a-993">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="c117a-994">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="c117a-994">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="c117a-995">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-995">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="c117a-996">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="c117a-996">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="c117a-997">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="c117a-997">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="c117a-998">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="c117a-998">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="c117a-999">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-999">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="c117a-1000">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="c117a-1000">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="c117a-1001">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="c117a-1001">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="c117a-1002">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="c117a-1002">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="c117a-1003">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="c117a-1003">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="c117a-1004">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1004">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="c117a-1005">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="c117a-1005">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="c117a-1006">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="c117a-1006">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="c117a-1007">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1007">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="c117a-1008">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="c117a-1008">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="c117a-1009">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="c117a-1009">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="c117a-1010">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1010">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="c117a-1011">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1011">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="c117a-1012">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="c117a-1012">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="c117a-1013">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="c117a-1013">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="c117a-1014">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1014">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="c117a-1015">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1015">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="c117a-1016">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="c117a-1016">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="c117a-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="c117a-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="c117a-1018">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="c117a-1018">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="c117a-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="c117a-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="c117a-1020">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="c117a-1020">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="c117a-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="c117a-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="c117a-1022">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="c117a-1022">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="c117a-1023">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="c117a-1023">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="c117a-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="c117a-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="c117a-1025">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="c117a-1025">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="c117a-1026">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="c117a-1026">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="c117a-1027">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="c117a-1027">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c117a-1028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c117a-1028">Az.Automation</span></span>
* <span data-ttu-id="c117a-1029">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1029">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="c117a-1030">https://github.com/Azure/azure-powershell/issues/7977 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1030">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="c117a-1031">https://github.com/Azure/azure-powershell/issues/8600 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1031">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="c117a-1032">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1032">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="c117a-1033">https://github.com/Azure/azure-powershell/issues/8347 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1033">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="c117a-1034">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1034">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="c117a-1035">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-1035">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1036">Az.Compute</span></span>
* <span data-ttu-id="c117a-1037">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1037">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="c117a-1038">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="c117a-1038">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c117a-1039">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-1039">Az.DataLakeStore</span></span>
* <span data-ttu-id="c117a-1040">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1040">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c117a-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c117a-1041">Az.Monitor</span></span>
* <span data-ttu-id="c117a-1042">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1042">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-1043">Az.Network</span></span>
* <span data-ttu-id="c117a-1044">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1044">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="c117a-1045">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c117a-1045">Updated cmdlet:</span></span>
        - <span data-ttu-id="c117a-1046">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="c117a-1046">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="c117a-1047">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1047">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1048">Az.Resources</span></span>
* <span data-ttu-id="c117a-1049">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1049">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1050">Az.Sql</span></span>
* <span data-ttu-id="c117a-1051">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="c117a-1051">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="c117a-1052">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-1052">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c117a-1053">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-1053">Az.Accounts</span></span>
* <span data-ttu-id="c117a-1054">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="c117a-1054">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c117a-1055">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1055">Az.CognitiveServices</span></span>
* <span data-ttu-id="c117a-1056">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="c117a-1056">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="c117a-1057">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="c117a-1057">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1058">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1058">Az.Compute</span></span>
* <span data-ttu-id="c117a-1059">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="c117a-1059">Proximity placement group feature.</span></span>
    - <span data-ttu-id="c117a-1060">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c117a-1060">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="c117a-1061">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-1061">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="c117a-1062">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1062">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="c117a-1063">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="c117a-1063">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="c117a-1064">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1064">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="c117a-1065">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c117a-1065">Breaking changes</span></span>
    - <span data-ttu-id="c117a-1066">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1066">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="c117a-1067">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1067">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="c117a-1068">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="c117a-1068">Az.DeploymentManager</span></span>
* <span data-ttu-id="c117a-1069">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="c117a-1069">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="c117a-1070">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="c117a-1070">Az.Dns</span></span>
* <span data-ttu-id="c117a-1071">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="c117a-1071">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="c117a-1072">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="c117a-1072">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="c117a-1073">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="c117a-1073">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c117a-1074">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c117a-1074">Az.FrontDoor</span></span>
* <span data-ttu-id="c117a-1075">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="c117a-1075">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="c117a-1076">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="c117a-1076">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="c117a-1077">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c117a-1077">Az.HDInsight</span></span>
* <span data-ttu-id="c117a-1078">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="c117a-1078">Removed two cmdlets:</span></span>
    - <span data-ttu-id="c117a-1079">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c117a-1079">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="c117a-1080">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c117a-1080">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="c117a-1081">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1081">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="c117a-1082">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="c117a-1082">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="c117a-1083">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="c117a-1083">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="c117a-1084">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="c117a-1084">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c117a-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c117a-1085">Az.Monitor</span></span>
* <span data-ttu-id="c117a-1086">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="c117a-1086">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="c117a-1087">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="c117a-1087">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="c117a-1088">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="c117a-1088">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="c117a-1089">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="c117a-1089">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="c117a-1090">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="c117a-1090">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="c117a-1091">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="c117a-1091">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="c117a-1092">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="c117a-1092">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="c117a-1093">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c117a-1093">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c117a-1094">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c117a-1094">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c117a-1095">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c117a-1095">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c117a-1096">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c117a-1096">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c117a-1097">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c117a-1097">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c117a-1098">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="c117a-1098">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="c117a-1099">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1099">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-1100">Az.Network</span></span>
* <span data-ttu-id="c117a-1101">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="c117a-1101">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="c117a-1102">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-1102">New cmdlets</span></span>
        - <span data-ttu-id="c117a-1103">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c117a-1103">New-AzNatGateway</span></span>
        - <span data-ttu-id="c117a-1104">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c117a-1104">Get-AzNatGateway</span></span>
        - <span data-ttu-id="c117a-1105">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c117a-1105">Set-AzNatGateway</span></span>
        - <span data-ttu-id="c117a-1106">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c117a-1106">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="c117a-1107">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1107">Updated cmdlets</span></span>
        - <span data-ttu-id="c117a-1108">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="c117a-1108">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="c117a-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="c117a-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="c117a-1110">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="c117a-1110">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="c117a-1111">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1111">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="c117a-1112">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1112">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c117a-1113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c117a-1113">Az.PolicyInsights</span></span>
* <span data-ttu-id="c117a-1114">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-1114">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="c117a-1115">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c117a-1115">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="c117a-1116">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="c117a-1116">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-1117">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1117">Az.RecoveryServices</span></span>
* <span data-ttu-id="c117a-1118">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-1118">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="c117a-1119">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="c117a-1119">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="c117a-1120">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="c117a-1120">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="c117a-1121">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="c117a-1121">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="c117a-1122">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="c117a-1122">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="c117a-1123">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="c117a-1123">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="c117a-1124">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c117a-1124">Az.Relay</span></span>
* <span data-ttu-id="c117a-1125">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="c117a-1125">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c117a-1126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c117a-1126">Az.ServiceBus</span></span>
* <span data-ttu-id="c117a-1127">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1127">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-1128">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-1128">Az.Storage</span></span>
* <span data-ttu-id="c117a-1129">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="c117a-1129">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="c117a-1130">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="c117a-1130">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="c117a-1131">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="c117a-1131">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="c117a-1132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c117a-1132">New-AzStorageAccount</span></span>
* <span data-ttu-id="c117a-1133">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="c117a-1133">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="c117a-1134">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c117a-1134">New-AzStorageAccount</span></span>
    - <span data-ttu-id="c117a-1135">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c117a-1135">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="c117a-1136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c117a-1136">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-1137">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-1137">Az.Websites</span></span>
* <span data-ttu-id="c117a-1138">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="c117a-1138">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="c117a-1139">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1139">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="c117a-1140">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-1140">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c117a-1141">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="c117a-1141">Highlights since the last major release</span></span>
* <span data-ttu-id="c117a-1142">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c117a-1142">General availability of `Az` module</span></span>
* <span data-ttu-id="c117a-1143">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c117a-1143">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c117a-1144">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c117a-1144">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c117a-1145">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1145">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c117a-1146">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1146">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c117a-1147">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1147">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c117a-1148">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-1148">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c117a-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-1149">Az.Accounts</span></span>
* <span data-ttu-id="c117a-1150">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1150">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c117a-1151">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c117a-1151">Az.Batch</span></span>
* <span data-ttu-id="c117a-1152">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c117a-1153">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c117a-1153">Az.Cdn</span></span>
* <span data-ttu-id="c117a-1154">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1154">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c117a-1155">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1155">Az.CognitiveServices</span></span>
* <span data-ttu-id="c117a-1156">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1157">Az.Compute</span></span>
* <span data-ttu-id="c117a-1158">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1158">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="c117a-1159">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c117a-1160">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1160">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c117a-1161">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c117a-1161">Az.DataFactory</span></span>
* <span data-ttu-id="c117a-1162">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1162">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c117a-1163">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-1163">Az.DataLakeStore</span></span>
* <span data-ttu-id="c117a-1164">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c117a-1165">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c117a-1165">Az.EventGrid</span></span>
* <span data-ttu-id="c117a-1166">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1166">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c117a-1167">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c117a-1167">Az.EventHub</span></span>
* <span data-ttu-id="c117a-1168">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1168">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="c117a-1169">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c117a-1169">Az.HDInsight</span></span>
* <span data-ttu-id="c117a-1170">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1170">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c117a-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c117a-1171">Az.IotHub</span></span>
* <span data-ttu-id="c117a-1172">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c117a-1173">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c117a-1173">Az.KeyVault</span></span>
* <span data-ttu-id="c117a-1174">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1174">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c117a-1175">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1175">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="c117a-1176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c117a-1176">Az.MachineLearning</span></span>
* <span data-ttu-id="c117a-1177">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="c117a-1178">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c117a-1178">Az.Media</span></span>
* <span data-ttu-id="c117a-1179">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c117a-1180">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c117a-1180">Az.Monitor</span></span>
  * <span data-ttu-id="c117a-1181">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="c117a-1181">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="c117a-1182">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="c117a-1182">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="c117a-1183">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="c117a-1183">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="c117a-1184">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c117a-1184">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="c117a-1185">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c117a-1185">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="c117a-1186">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c117a-1186">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="c117a-1187">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1187">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-1188">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-1188">Az.Network</span></span>
* <span data-ttu-id="c117a-1189">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1189">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c117a-1190">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1190">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="c117a-1191">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="c117a-1191">Az.NotificationHubs</span></span>
* <span data-ttu-id="c117a-1192">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1192">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c117a-1193">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c117a-1193">Az.OperationalInsights</span></span>
* <span data-ttu-id="c117a-1194">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1194">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="c117a-1195">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c117a-1195">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="c117a-1196">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-1197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1197">Az.RecoveryServices</span></span>
* <span data-ttu-id="c117a-1198">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c117a-1199">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="c117a-1199">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="c117a-1200">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1200">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="c117a-1201">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1201">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c117a-1202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c117a-1202">Az.RedisCache</span></span>
* <span data-ttu-id="c117a-1203">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-1204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1204">Az.Resources</span></span>
* <span data-ttu-id="c117a-1205">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1205">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-1206">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1206">Az.Sql</span></span>
* <span data-ttu-id="c117a-1207">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1207">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="c117a-1208">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c117a-1209">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1209">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="c117a-1210">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1210">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="c117a-1211">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1211">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="c117a-1212">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-1212">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="c117a-1213">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1213">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-1214">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-1214">Az.Websites</span></span>
* <span data-ttu-id="c117a-1215">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1215">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="c117a-1216">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c117a-1217">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1217">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="c117a-1218">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1218">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="c117a-1219">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-1219">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c117a-1220">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="c117a-1220">Highlights since the last major release</span></span>
* <span data-ttu-id="c117a-1221">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c117a-1221">General availability of `Az` module</span></span>
* <span data-ttu-id="c117a-1222">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c117a-1222">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c117a-1223">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c117a-1223">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c117a-1224">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1224">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c117a-1225">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1225">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c117a-1226">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1226">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c117a-1227">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-1227">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c117a-1228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-1228">Az.Accounts</span></span>
* <span data-ttu-id="c117a-1229">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1229">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c117a-1230">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1230">Az.AnalysisServices</span></span>
* <span data-ttu-id="c117a-1231">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c117a-1231">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="c117a-1232">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="c117a-1232">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c117a-1233">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c117a-1233">Az.Automation</span></span>
* <span data-ttu-id="c117a-1234">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1234">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="c117a-1235">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-1235">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="c117a-1236">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c117a-1236">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1237">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1237">Az.Compute</span></span>
* <span data-ttu-id="c117a-1238">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1238">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="c117a-1239">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1239">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="c117a-1240">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c117a-1240">Az.ContainerInstance</span></span>
* <span data-ttu-id="c117a-1241">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1241">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c117a-1242">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c117a-1242">Az.DataFactory</span></span>
* <span data-ttu-id="c117a-1243">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1243">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="c117a-1244">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1244">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-1245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1245">Az.Resources</span></span>
* <span data-ttu-id="c117a-1246">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1246">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="c117a-1247">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1247">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="c117a-1248">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1248">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="c117a-1249">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="c117a-1249">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="c117a-1250">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1250">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="c117a-1251">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="c117a-1251">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1252">Az.Sql</span></span>
* <span data-ttu-id="c117a-1253">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-1253">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-1254">Az.Storage</span></span>
* <span data-ttu-id="c117a-1255">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="c117a-1255">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="c117a-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c117a-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="c117a-1257">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="c117a-1257">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="c117a-1258">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c117a-1258">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="c117a-1259">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c117a-1259">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="c117a-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c117a-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="c117a-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c117a-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="c117a-1262">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="c117a-1262">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="c117a-1263">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c117a-1263">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="c117a-1264">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c117a-1264">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="c117a-1265">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c117a-1265">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="c117a-1266">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c117a-1266">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="c117a-1267">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-1267">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c117a-1268">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="c117a-1268">Highlights since the last major release</span></span>
* <span data-ttu-id="c117a-1269">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c117a-1269">General availability of `Az` module</span></span>
* <span data-ttu-id="c117a-1270">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c117a-1270">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c117a-1271">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c117a-1271">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c117a-1272">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1272">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c117a-1273">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1273">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c117a-1274">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1274">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c117a-1275">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-1275">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c117a-1276">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c117a-1276">Az.Automation</span></span>
* <span data-ttu-id="c117a-1277">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="c117a-1277">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="c117a-1278">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="c117a-1278">Dynamic grouping</span></span>
    * <span data-ttu-id="c117a-1279">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="c117a-1279">Pre-Post script</span></span>
    * <span data-ttu-id="c117a-1280">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="c117a-1280">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1281">Az.Compute</span></span>
* <span data-ttu-id="c117a-1282">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="c117a-1282">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="c117a-1283">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1283">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c117a-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c117a-1284">Az.KeyVault</span></span>
* <span data-ttu-id="c117a-1285">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1285">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-1286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-1286">Az.Network</span></span>
* <span data-ttu-id="c117a-1287">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1287">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="c117a-1288">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1288">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-1289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1289">Az.RecoveryServices</span></span>
* <span data-ttu-id="c117a-1290">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1290">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="c117a-1291">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1291">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1292">Az.Resources</span></span>
* <span data-ttu-id="c117a-1293">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1293">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="c117a-1294">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1294">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-1295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1295">Az.Sql</span></span>
* <span data-ttu-id="c117a-1296">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1296">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-1297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-1297">Az.Storage</span></span>
* <span data-ttu-id="c117a-1298">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="c117a-1298">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="c117a-1299">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c117a-1299">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c117a-1300">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c117a-1300">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c117a-1301">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c117a-1301">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c117a-1302">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="c117a-1302">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="c117a-1303">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="c117a-1303">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="c117a-1304">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="c117a-1304">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-1305">Az.Websites</span></span>
* <span data-ttu-id="c117a-1306">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1306">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="c117a-1307">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-1307">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c117a-1308">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-1308">Az.Accounts</span></span>
* <span data-ttu-id="c117a-1309">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1309">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="c117a-1310">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1310">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c117a-1311">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c117a-1311">Az.Automation</span></span>
* <span data-ttu-id="c117a-1312">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1312">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="c117a-1313">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1313">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="c117a-1314">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="c117a-1314">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c117a-1315">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c117a-1315">Az.Cdn</span></span>
* <span data-ttu-id="c117a-1316">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-1316">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1317">Az.Compute</span></span>
* <span data-ttu-id="c117a-1318">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1318">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c117a-1319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c117a-1319">Az.DataFactory</span></span>
* <span data-ttu-id="c117a-1320">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1320">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c117a-1321">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c117a-1321">Az.LogicApp</span></span>
* <span data-ttu-id="c117a-1322">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="c117a-1322">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-1323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-1323">Az.Network</span></span>
* <span data-ttu-id="c117a-1324">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1324">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1325">Az.RecoveryServices</span></span>
* <span data-ttu-id="c117a-1326">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1326">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="c117a-1327">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="c117a-1327">SDK Update</span></span>
* <span data-ttu-id="c117a-1328">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-1328">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="c117a-1329">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1329">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1330">Az.Resources</span></span>
* <span data-ttu-id="c117a-1331">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1331">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="c117a-1332">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="c117a-1332">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="c117a-1333">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1333">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="c117a-1334">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="c117a-1334">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="c117a-1335">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1335">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="c117a-1336">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="c117a-1336">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1337">Az.Sql</span></span>
* <span data-ttu-id="c117a-1338">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-1338">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="c117a-1339">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-1339">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-1340">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-1340">Az.Storage</span></span>
* <span data-ttu-id="c117a-1341">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c117a-1341">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="c117a-1342">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-1342">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="c117a-1343">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1343">Az.AnalysisServices</span></span>
* <span data-ttu-id="c117a-1344">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-1344">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c117a-1345">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c117a-1345">Az.Automation</span></span>
* <span data-ttu-id="c117a-1346">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1346">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="c117a-1347">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1347">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="c117a-1348">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1348">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c117a-1349">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1349">Az.CognitiveServices</span></span>
* <span data-ttu-id="c117a-1350">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1350">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1351">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1351">Az.Compute</span></span>
* <span data-ttu-id="c117a-1352">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1352">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="c117a-1353">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1353">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="c117a-1354">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1354">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="c117a-1355">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="c117a-1355">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c117a-1356">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-1356">Az.DataLakeStore</span></span>
* <span data-ttu-id="c117a-1357">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1357">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c117a-1358">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c117a-1358">Az.EventHub</span></span>
* <span data-ttu-id="c117a-1359">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1359">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="c117a-1360">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c117a-1360">Az.KeyVault</span></span>
* <span data-ttu-id="c117a-1361">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1361">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c117a-1362">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c117a-1362">Az.LogicApp</span></span>
* <span data-ttu-id="c117a-1363">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1363">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="c117a-1364">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1364">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="c117a-1365">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-1365">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="c117a-1366">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c117a-1366">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c117a-1367">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c117a-1367">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c117a-1368">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c117a-1368">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c117a-1369">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c117a-1369">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="c117a-1370">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c117a-1370">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="c117a-1371">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c117a-1371">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c117a-1372">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c117a-1372">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c117a-1373">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c117a-1373">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c117a-1374">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c117a-1374">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="c117a-1375">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1375">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c117a-1376">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c117a-1376">Az.Monitor</span></span>
* <span data-ttu-id="c117a-1377">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1377">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-1378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-1378">Az.Network</span></span>
* <span data-ttu-id="c117a-1379">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1379">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c117a-1380">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c117a-1380">Az.OperationalInsights</span></span>
* <span data-ttu-id="c117a-1381">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="c117a-1381">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="c117a-1382">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1382">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="c117a-1383">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1383">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="c117a-1384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1384">Az.Resources</span></span>
* <span data-ttu-id="c117a-1385">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1385">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c117a-1386">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1386">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="c117a-1387">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1387">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="c117a-1388">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1388">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1389">Az.Sql</span></span>
* <span data-ttu-id="c117a-1390">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1390">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="c117a-1391">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1391">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-1392">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-1392">Az.Websites</span></span>
* <span data-ttu-id="c117a-1393">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1393">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="c117a-1394">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-1394">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c117a-1395">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-1395">Az.Accounts</span></span>
* <span data-ttu-id="c117a-1396">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c117a-1396">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c117a-1397">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1397">Az.AnalysisServices</span></span>
<span data-ttu-id="c117a-1398">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="c117a-1398">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1399">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1399">Az.Compute</span></span>
* <span data-ttu-id="c117a-1400">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1400">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="c117a-1401">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1401">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="c117a-1402">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1402">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-1403">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1403">Az.RecoveryServices</span></span>
<span data-ttu-id="c117a-1404">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="c117a-1404">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-1405">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1405">Az.Resources</span></span>
* <span data-ttu-id="c117a-1406">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1406">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="c117a-1407">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="c117a-1407">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c117a-1408">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1408">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="c117a-1409">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="c117a-1409">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-1410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1410">Az.Sql</span></span>
* <span data-ttu-id="c117a-1411">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c117a-1411">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="c117a-1412">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1412">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="c117a-1413">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1413">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="c117a-1414">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-1414">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c117a-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-1415">Az.Accounts</span></span>
* <span data-ttu-id="c117a-1416">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="c117a-1416">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c117a-1417">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1417">Az.AnalysisServices</span></span>
* <span data-ttu-id="c117a-1418">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="c117a-1418">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-1419">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1419">Az.RecoveryServices</span></span>
* <span data-ttu-id="c117a-1420">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="c117a-1420">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="c117a-1421">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-1421">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c117a-1422">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-1422">Az.Accounts</span></span>
* <span data-ttu-id="c117a-1423">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1423">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c117a-1424">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1424">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c117a-1425">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1425">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="c117a-1426">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c117a-1426">Az.Aks</span></span>
* <span data-ttu-id="c117a-1427">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1427">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c117a-1428">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c117a-1428">Az.Automation</span></span>
* <span data-ttu-id="c117a-1429">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1429">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="c117a-1430">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1430">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c117a-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c117a-1431">Az.Cdn</span></span>
* <span data-ttu-id="c117a-1432">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1432">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1433">Az.Compute</span></span>
* <span data-ttu-id="c117a-1434">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1434">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="c117a-1435">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1435">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="c117a-1436">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1436">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="c117a-1437">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c117a-1437">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c117a-1438">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1438">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c117a-1439">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c117a-1439">Az.DataFactory</span></span>
* <span data-ttu-id="c117a-1440">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1440">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c117a-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="c117a-1442">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1442">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="c117a-1443">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="c117a-1443">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="c117a-1444">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1444">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c117a-1445">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c117a-1445">Az.IotHub</span></span>
* <span data-ttu-id="c117a-1446">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1446">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c117a-1447">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c117a-1447">Az.KeyVault</span></span>
* <span data-ttu-id="c117a-1448">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1448">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-1449">Az.Network</span></span>
* <span data-ttu-id="c117a-1450">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1450">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-1451">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1451">Az.Resources</span></span>
* <span data-ttu-id="c117a-1452">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1452">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="c117a-1453">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1453">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="c117a-1454">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1454">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="c117a-1455">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1455">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="c117a-1456">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1456">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="c117a-1457">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1457">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="c117a-1458">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="c117a-1458">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c117a-1459">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c117a-1459">Az.ServiceFabric</span></span>
* <span data-ttu-id="c117a-1460">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="c117a-1460">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="c117a-1461">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1461">Fix some error messages.</span></span>
* <span data-ttu-id="c117a-1462">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1462">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="c117a-1463">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1463">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c117a-1464">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c117a-1464">Az.SignalR</span></span>
* <span data-ttu-id="c117a-1465">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1465">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-1466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1466">Az.Sql</span></span>
* <span data-ttu-id="c117a-1467">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1467">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c117a-1468">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1468">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="c117a-1469">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1469">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="c117a-1470">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="c117a-1470">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-1471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-1471">Az.Storage</span></span>
* <span data-ttu-id="c117a-1472">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1472">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c117a-1473">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-1473">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="c117a-1474">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c117a-1474">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="c117a-1475">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c117a-1475">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="c117a-1476">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c117a-1476">Az.TrafficManager</span></span>
* <span data-ttu-id="c117a-1477">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1477">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-1478">Az.Websites</span></span>
* <span data-ttu-id="c117a-1479">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1479">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c117a-1480">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1480">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="c117a-1481">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1481">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="c117a-1482">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="c117a-1482">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c117a-1483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-1483">Az.Accounts</span></span>
* <span data-ttu-id="c117a-1484">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1484">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1485">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1485">Az.Compute</span></span>
* <span data-ttu-id="c117a-1486">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="c117a-1486">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="c117a-1487">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1487">Updated the description of ID in help files</span></span>
* <span data-ttu-id="c117a-1488">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="c117a-1488">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c117a-1489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-1489">Az.DataLakeStore</span></span>
* <span data-ttu-id="c117a-1490">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1490">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="c117a-1491">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1491">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c117a-1492">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c117a-1492">Az.EventGrid</span></span>
* <span data-ttu-id="c117a-1493">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1493">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="c117a-1494">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1494">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="c117a-1495">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c117a-1495">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c117a-1496">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="c117a-1496">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c117a-1497">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="c117a-1497">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c117a-1498">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="c117a-1498">Dead letter endpoint.</span></span>
    - <span data-ttu-id="c117a-1499">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c117a-1499">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c117a-1500">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="c117a-1500">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c117a-1501">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="c117a-1501">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c117a-1502">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="c117a-1502">Dead letter endpoint.</span></span>
* <span data-ttu-id="c117a-1503">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1503">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="c117a-1504">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-1504">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c117a-1505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c117a-1505">Az.IotHub</span></span>
* <span data-ttu-id="c117a-1506">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1506">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c117a-1507">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c117a-1507">Az.LogicApp</span></span>
* <span data-ttu-id="c117a-1508">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="c117a-1508">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-1509">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1509">Az.Resources</span></span>
* <span data-ttu-id="c117a-1510">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1510">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="c117a-1511">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="c117a-1511">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="c117a-1512">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1512">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c117a-1513">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1513">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="c117a-1514">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1514">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="c117a-1515">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="c117a-1515">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c117a-1516">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c117a-1516">Az.SignalR</span></span>
* <span data-ttu-id="c117a-1517">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="c117a-1517">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-1518">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1518">Az.Sql</span></span>
* <span data-ttu-id="c117a-1519">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="c117a-1519">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c117a-1520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-1520">Az.Storage</span></span>
* <span data-ttu-id="c117a-1521">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="c117a-1521">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="c117a-1522">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c117a-1522">New-AzStorageContext</span></span>
* <span data-ttu-id="c117a-1523">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1523">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="c117a-1524">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c117a-1524">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-1525">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-1525">Az.Websites</span></span>
* <span data-ttu-id="c117a-1526">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1526">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="c117a-1527">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="c117a-1527">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="c117a-1528">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="c117a-1528">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="c117a-1529">Genel</span><span class="sxs-lookup"><span data-stu-id="c117a-1529">General</span></span>

- <span data-ttu-id="c117a-1530">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="c117a-1530">General Availability of Az Module</span></span>
- <span data-ttu-id="c117a-1531">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="c117a-1531">Online help for each module</span></span>
- <span data-ttu-id="c117a-1532">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="c117a-1532">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="c117a-1533">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1533">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="c117a-1534">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c117a-1534">Az.Accounts</span></span>
- <span data-ttu-id="c117a-1535">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c117a-1535">Changed from Az.Profile</span></span>
- <span data-ttu-id="c117a-1536">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1536">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c117a-1537">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c117a-1537">Az.ApiManagement</span></span>
- <span data-ttu-id="c117a-1538">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="c117a-1538">Fixes for #7002</span></span>
- <span data-ttu-id="c117a-1539">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="c117a-1540">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c117a-1540">Az.Batch</span></span>
- <span data-ttu-id="c117a-1541">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1541">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="c117a-1542">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="c117a-1542">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="c117a-1543">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="c117a-1544">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c117a-1544">Az.Billing</span></span>
- <span data-ttu-id="c117a-1545">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1545">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="c117a-1546">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1546">Az.CognitivServices</span></span>
- <span data-ttu-id="c117a-1547">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1547">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="c117a-1548">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-1548">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c117a-1549">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c117a-1549">Az.ContainerInstance</span></span>
- <span data-ttu-id="c117a-1550">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1550">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="c117a-1551">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c117a-1551">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="c117a-1552">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c117a-1553">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-1553">Az.DataLakeStore</span></span>
- <span data-ttu-id="c117a-1554">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="c117a-1555">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c117a-1555">Az.Monitor</span></span>
- <span data-ttu-id="c117a-1556">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1556">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="c117a-1557">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c117a-1557">Az.KeyVault</span></span>
- <span data-ttu-id="c117a-1558">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-1558">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="c117a-1559">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c117a-1559">Az.MachineLearning</span></span>
- <span data-ttu-id="c117a-1560">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1560">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="c117a-1561">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c117a-1561">Az.Media</span></span>
- <span data-ttu-id="c117a-1562">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c117a-1562">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c117a-1563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-1563">Az.Network</span></span>
<span data-ttu-id="c117a-1564">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1564">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="c117a-1565">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c117a-1565">New cmdlets added:</span></span>
        - <span data-ttu-id="c117a-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c117a-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c117a-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c117a-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c117a-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c117a-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c117a-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c117a-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c117a-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c117a-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c117a-1571">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c117a-1571">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="c117a-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c117a-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="c117a-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c117a-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="c117a-1574">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1574">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="c117a-1575">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c117a-1575">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="c117a-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c117a-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c117a-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c117a-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c117a-1578">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-1578">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="c117a-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="c117a-1580">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1580">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="c117a-1581">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1581">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="c117a-1582">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c117a-1582">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c117a-1583">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c117a-1583">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c117a-1584">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c117a-1584">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="c117a-1585">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1585">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="c117a-1586">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1586">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="c117a-1587">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c117a-1587">Az.OperationalInsights</span></span>
- <span data-ttu-id="c117a-1588">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="c117a-1589">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c117a-1589">Az.Profile</span></span>
- <span data-ttu-id="c117a-1590">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1590">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-1591">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1591">Az.RecoveryServices</span></span>
- <span data-ttu-id="c117a-1592">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="c117a-1593">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1593">Az.Resources</span></span>
- <span data-ttu-id="c117a-1594">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1594">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c117a-1595">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c117a-1595">Az.ServiceFabric</span></span>
- <span data-ttu-id="c117a-1596">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="c117a-1596">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="c117a-1597">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1597">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="c117a-1598">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c117a-1598">Az.SIgnalR</span></span>
- <span data-ttu-id="c117a-1599">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c117a-1599">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="c117a-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1600">Az.Sql</span></span>
- <span data-ttu-id="c117a-1601">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1601">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="c117a-1602">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1602">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="c117a-1603">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="c117a-1604">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-1604">Az.Storage</span></span>
- <span data-ttu-id="c117a-1605">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c117a-1606">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-1606">Az.Websites</span></span>
- <span data-ttu-id="c117a-1607">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c117a-1607">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="c117a-1608">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="c117a-1608">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="c117a-1609">Genel</span><span class="sxs-lookup"><span data-stu-id="c117a-1609">General</span></span>

* <span data-ttu-id="c117a-1610">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c117a-1610">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="c117a-1611">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1611">Az.Compute</span></span>

* <span data-ttu-id="c117a-1612">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1612">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c117a-1613">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-1613">Az.DataLakeStore</span></span>

* <span data-ttu-id="c117a-1614">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1614">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="c117a-1615">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c117a-1615">Az.FrontDoor</span></span>

* <span data-ttu-id="c117a-1616">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1616">Fixed some broken links</span></span>
    - <span data-ttu-id="c117a-1617">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1617">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="c117a-1618">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1618">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c117a-1619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1619">Az.RecoveryServices</span></span>

* <span data-ttu-id="c117a-1620">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1620">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="c117a-1621">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1621">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="c117a-1622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1622">Az.Resources</span></span>

* <span data-ttu-id="c117a-1623">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c117a-1623">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="c117a-1624">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1624">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="c117a-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1625">Az.Sql</span></span>

* <span data-ttu-id="c117a-1626">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c117a-1626">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="c117a-1627">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1627">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="c117a-1628">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1628">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="c117a-1629">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c117a-1629">Az.Storage</span></span>

* <span data-ttu-id="c117a-1630">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1630">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="c117a-1631">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1631">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="c117a-1632">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c117a-1632">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c117a-1633">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1633">Support Static Website configuration</span></span>
    - <span data-ttu-id="c117a-1634">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c117a-1634">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="c117a-1635">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c117a-1635">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c117a-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-1636">Az.Websites</span></span>

* <span data-ttu-id="c117a-1637">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c117a-1637">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="c117a-1638">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1638">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="c117a-1639">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="c117a-1639">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="c117a-1640">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="c117a-1640">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c117a-1641">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c117a-1641">Az.ApiManagement</span></span>
* <span data-ttu-id="c117a-1642">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="c117a-1642">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="c117a-1643">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c117a-1643">Az.Automation</span></span>
* <span data-ttu-id="c117a-1644">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="c117a-1644">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="c117a-1645">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1645">Added Update Management cmdlets</span></span>
* <span data-ttu-id="c117a-1646">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1646">Added Source Control cmdlets</span></span>
* <span data-ttu-id="c117a-1647">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1647">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="c117a-1648">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1648">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="c117a-1649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1649">Az.Compute</span></span>
* <span data-ttu-id="c117a-1650">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1650">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="c117a-1651">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="c117a-1651">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c117a-1652">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c117a-1652">Az.ContainerInstance</span></span>
* <span data-ttu-id="c117a-1653">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="c117a-1653">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="c117a-1654">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c117a-1654">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c117a-1655">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1655">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c117a-1656">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-1656">Az.Network</span></span>
* <span data-ttu-id="c117a-1657">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1657">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="c117a-1658">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1658">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="c117a-1659">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1659">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="c117a-1660">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1660">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="c117a-1661">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c117a-1661">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c117a-1662">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1662">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="c117a-1663">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="c117a-1663">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="c117a-1664">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c117a-1664">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c117a-1665">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1665">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="c117a-1666">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="c117a-1666">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="c117a-1667">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c117a-1667">Az.Relay</span></span>
* <span data-ttu-id="c117a-1668">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1668">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="c117a-1669">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1669">Az.Resources</span></span>
* <span data-ttu-id="c117a-1670">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1670">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="c117a-1671">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1671">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="c117a-1672">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="c117a-1672">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c117a-1673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c117a-1673">Az.ServiceFabric</span></span>
* <span data-ttu-id="c117a-1674">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1674">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="c117a-1675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1675">Az.Sql</span></span>
* <span data-ttu-id="c117a-1676">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1676">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="c117a-1677">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c117a-1677">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c117a-1678">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c117a-1678">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c117a-1679">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c117a-1679">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c117a-1680">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c117a-1680">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c117a-1681">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c117a-1681">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c117a-1682">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c117a-1682">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c117a-1683">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c117a-1683">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c117a-1684">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c117a-1684">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="c117a-1685">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1685">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="c117a-1686">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1686">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="c117a-1687">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1687">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="c117a-1688">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c117a-1688">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c117a-1689">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c117a-1689">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c117a-1690">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c117a-1690">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="c117a-1691">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c117a-1691">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="c117a-1692">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1692">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="c117a-1693">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="c117a-1693">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c117a-1694">Genel</span><span class="sxs-lookup"><span data-stu-id="c117a-1694">General</span></span>
* <span data-ttu-id="c117a-1695">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="c117a-1695">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="c117a-1696">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c117a-1696">Az.Profile</span></span>
* <span data-ttu-id="c117a-1697">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1697">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="c117a-1698">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1698">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="c117a-1699">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1699">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="c117a-1700">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1700">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="c117a-1701">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1701">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="c117a-1702">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1702">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="c117a-1703">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1703">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="c117a-1704">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1704">Az.CognitiveServices</span></span>
* <span data-ttu-id="c117a-1705">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1705">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1706">Az.Compute</span></span>
* <span data-ttu-id="c117a-1707">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1707">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="c117a-1708">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="c117a-1708">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="c117a-1709">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1709">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c117a-1710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-1710">Az.DataLakeStore</span></span>
* <span data-ttu-id="c117a-1711">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1711">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="c117a-1712">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1712">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="c117a-1713">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="c117a-1713">Az.Insights</span></span>
* <span data-ttu-id="c117a-1714">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1714">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="c117a-1715">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="c117a-1715">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="c117a-1716">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1716">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="c117a-1717">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="c117a-1717">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-1718">Az.Network</span></span>
* <span data-ttu-id="c117a-1719">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="c117a-1719">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="c117a-1720">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c117a-1720">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="c117a-1721">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c117a-1721">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="c117a-1722">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c117a-1722">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="c117a-1723">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c117a-1723">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c117a-1724">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c117a-1724">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c117a-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c117a-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c117a-1726">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c117a-1726">Az.PolicyInsights</span></span>
* <span data-ttu-id="c117a-1727">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1727">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1728">Az.Resources</span></span>
* <span data-ttu-id="c117a-1729">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c117a-1729">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="c117a-1730">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="c117a-1730">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c117a-1731">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c117a-1731">Az.ServiceBus</span></span>
* <span data-ttu-id="c117a-1732">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1732">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c117a-1733">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c117a-1733">Az.ServiceFabric</span></span>
* <span data-ttu-id="c117a-1734">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1734">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="c117a-1735">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1735">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="c117a-1736">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="c117a-1736">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="c117a-1737">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="c117a-1737">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="c117a-1738">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1738">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="c117a-1739">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="c117a-1739">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="c117a-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c117a-1740">Az.Profile</span></span>
* <span data-ttu-id="c117a-1741">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="c117a-1741">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="c117a-1742">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1742">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1743">Az.Compute</span></span>
* <span data-ttu-id="c117a-1744">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1744">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="c117a-1745">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1745">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c117a-1746">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c117a-1746">Az.DataLakeStore</span></span>
* <span data-ttu-id="c117a-1747">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="c117a-1747">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c117a-1748">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="c117a-1748">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c117a-1749">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="c117a-1749">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c117a-1750">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c117a-1750">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c117a-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="c117a-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-1752">Az.Network</span></span>
* <span data-ttu-id="c117a-1753">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-1753">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c117a-1754">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1755">Az.Resources</span></span>
* <span data-ttu-id="c117a-1756">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1756">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c117a-1757">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1757">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="c117a-1758">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="c117a-1758">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c117a-1759">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="c117a-1759">Azure.Storage</span></span>
* <span data-ttu-id="c117a-1760">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="c117a-1760">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c117a-1761">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c117a-1761">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c117a-1762">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c117a-1762">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c117a-1763">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="c117a-1763">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c117a-1764">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c117a-1764">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="c117a-1765">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c117a-1765">Az.CognitiveServices</span></span>
* <span data-ttu-id="c117a-1766">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="c117a-1766">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c117a-1767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c117a-1767">Az.Compute</span></span>
* <span data-ttu-id="c117a-1768">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1768">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c117a-1769">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1769">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="c117a-1770">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1770">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="c117a-1771">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c117a-1771">Az.DataFactoryV2</span></span>
* <span data-ttu-id="c117a-1772">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1772">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c117a-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c117a-1773">Az.Network</span></span>
* <span data-ttu-id="c117a-1774">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c117a-1774">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c117a-1775">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1775">new cmdlets added</span></span>
    - <span data-ttu-id="c117a-1776">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c117a-1776">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="c117a-1777">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c117a-1777">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="c117a-1778">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c117a-1778">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="c117a-1779">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c117a-1779">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="c117a-1780">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-1780">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="c117a-1781">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c117a-1781">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c117a-1782">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1782">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c117a-1783">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1783">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="c117a-1784">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1784">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c117a-1785">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c117a-1785">Az.RedisCache</span></span>
* <span data-ttu-id="c117a-1786">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="c117a-1786">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c117a-1787">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1787">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="c117a-1788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c117a-1788">Az.Resources</span></span>
* <span data-ttu-id="c117a-1789">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c117a-1789">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c117a-1790">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1790">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="c117a-1791">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c117a-1791">Az.Sql</span></span>
* <span data-ttu-id="c117a-1792">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c117a-1792">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c117a-1793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c117a-1793">Az.Websites</span></span>
* <span data-ttu-id="c117a-1794">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="c117a-1794">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c117a-1795">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="c117a-1795">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="c117a-1796">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="c117a-1796">0.2.0 - September 2018</span></span>
 <span data-ttu-id="c117a-1797">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="c117a-1797">Initial Release</span></span>
