---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: ee3f54e6bc15dbbaeb97cad7463cb1d2e5795e3e
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062148"
---
## <a name="300---november-2019"></a><span data-ttu-id="e06de-103">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-103">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="e06de-104">Genel</span><span class="sxs-lookup"><span data-stu-id="e06de-104">General</span></span>
* <span data-ttu-id="e06de-105">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="e06de-105">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e06de-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-106">Az.Accounts</span></span>
* <span data-ttu-id="e06de-107">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e06de-107">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e06de-108">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e06de-108">Az.Advisor</span></span>
* <span data-ttu-id="e06de-109">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-109">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e06de-110">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e06de-110">Az.Batch</span></span>
* <span data-ttu-id="e06de-111">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-111">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="e06de-112">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="e06de-112">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="e06de-113">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-113">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="e06de-114">**New-AzBatchTask** `-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet'i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-114">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="e06de-115">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="e06de-115">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="e06de-116">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="e06de-116">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="e06de-117">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="e06de-117">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="e06de-118">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-118">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="e06de-119">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-119">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="e06de-120">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-120">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="e06de-121">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="e06de-121">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="e06de-122">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="e06de-122">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="e06de-123">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-123">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="e06de-124">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="e06de-124">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="e06de-125">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-125">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="e06de-126">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-126">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="e06de-127">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-127">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="e06de-128">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-128">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="e06de-129">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-129">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="e06de-130">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-130">This operation is no longer supported.</span></span>
* <span data-ttu-id="e06de-131">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-131">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="e06de-132">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-132">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="e06de-133">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-133">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="e06de-134">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-134">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="e06de-135">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-135">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="e06de-136">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-136">New non-verified images are also now returned.</span></span> <span data-ttu-id="e06de-137">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-137">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="e06de-138">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-138">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="e06de-139">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-139">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="e06de-140">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-140">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="e06de-141">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-141">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="e06de-142">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-142">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="e06de-143">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-143">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="e06de-144">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-144">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="e06de-145">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="e06de-145">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="e06de-146">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="e06de-146">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e06de-147">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e06de-147">Az.Cdn</span></span>
* <span data-ttu-id="e06de-148">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-148">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="e06de-149">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-149">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-150">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-150">Az.Compute</span></span>
* <span data-ttu-id="e06de-151">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="e06de-151">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="e06de-152">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e06de-152">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="e06de-153">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="e06de-153">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="e06de-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e06de-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="e06de-155">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-155">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e06de-156">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-156">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="e06de-157">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="e06de-157">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="e06de-158">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-158">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="e06de-159">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="e06de-159">Breaking changes</span></span>
    - <span data-ttu-id="e06de-160">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="e06de-160">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="e06de-161">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="e06de-161">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e06de-162">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e06de-162">Az.DataFactory</span></span>
* <span data-ttu-id="e06de-163">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-163">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e06de-164">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e06de-164">Az.DataLakeStore</span></span>
* <span data-ttu-id="e06de-165">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="e06de-165">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="e06de-166">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="e06de-166">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="e06de-167">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="e06de-167">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="e06de-168">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="e06de-168">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="e06de-169">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="e06de-169">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="e06de-170">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="e06de-170">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e06de-171">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e06de-171">Az.FrontDoor</span></span>
* <span data-ttu-id="e06de-172">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-172">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e06de-173">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e06de-173">Az.HDInsight</span></span>
* <span data-ttu-id="e06de-174">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-174">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="e06de-175">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-175">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="e06de-176">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-176">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="e06de-177">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="e06de-177">Removed five cmdlets:</span></span>
    - <span data-ttu-id="e06de-178">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e06de-178">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e06de-179">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e06de-179">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e06de-180">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e06de-180">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e06de-181">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e06de-181">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="e06de-182">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e06de-182">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="e06de-183">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="e06de-183">Added three cmdlets:</span></span>
    - <span data-ttu-id="e06de-184">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="e06de-184">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="e06de-185">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="e06de-185">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="e06de-186">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="e06de-186">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="e06de-187">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-187">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="e06de-188">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-188">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="e06de-189">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-189">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="e06de-190">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-190">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="e06de-191">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-191">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="e06de-192">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-192">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="e06de-193">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-193">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="e06de-194">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-194">Added some scenario test cases.</span></span>
* <span data-ttu-id="e06de-195">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="e06de-195">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e06de-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e06de-196">Az.IotHub</span></span>
* <span data-ttu-id="e06de-197">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="e06de-197">Breaking changes:</span></span>
    - <span data-ttu-id="e06de-198">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="e06de-198">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e06de-199">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-199">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e06de-200">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="e06de-200">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e06de-201">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-201">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e06de-202">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-202">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="e06de-203">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-203">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="e06de-204">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-204">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="e06de-205">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-205">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="e06de-206">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="e06de-206">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e06de-207">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-207">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e06de-208">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="e06de-208">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e06de-209">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-209">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-210">Az.RecoveryServices</span></span>
* <span data-ttu-id="e06de-211">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-211">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="e06de-212">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-212">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="e06de-213">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-213">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="e06de-214">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-214">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="e06de-215">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-215">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="e06de-216">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-216">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="e06de-217">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-217">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="e06de-218">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-218">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="e06de-219">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-219">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-220">Az.Resources</span></span>
* <span data-ttu-id="e06de-221">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-221">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-222">Az.Network</span></span>
* <span data-ttu-id="e06de-223">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-223">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="e06de-224">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="e06de-225">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-225">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e06de-226">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-226">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e06de-227">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-227">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e06de-228">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-228">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e06de-229">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-229">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e06de-230">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-230">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="e06de-231">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e06de-231">New cmdlet:</span></span>
        - <span data-ttu-id="e06de-232">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="e06de-232">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="e06de-233">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-233">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="e06de-234">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-234">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="e06de-235">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-235">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="e06de-236">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-236">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="e06de-237">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-237">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="e06de-238">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-238">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="e06de-239">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-239">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="e06de-240">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="e06de-240">New cmdlets added:</span></span>
        - <span data-ttu-id="e06de-241">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e06de-241">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="e06de-242">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e06de-242">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e06de-243">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e06de-243">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e06de-244">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e06de-244">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e06de-245">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e06de-245">Set-AzVirtualHub</span></span>
* <span data-ttu-id="e06de-246">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-246">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="e06de-247">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-247">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e06de-248">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-248">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="e06de-249">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-249">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="e06de-250">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-250">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="e06de-251">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-251">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="e06de-252">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-252">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="e06de-253">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="e06de-253">New cmdlets added:</span></span>
        - <span data-ttu-id="e06de-254">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-254">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="e06de-255">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-255">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e06de-256">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-256">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e06de-257">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-257">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e06de-258">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-258">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e06de-259">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-259">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e06de-260">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-260">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="e06de-261">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-261">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="e06de-262">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="e06de-262">New cmdlets added:</span></span>
        - <span data-ttu-id="e06de-263">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="e06de-263">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="e06de-264">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="e06de-264">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="e06de-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e06de-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="e06de-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="e06de-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="e06de-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="e06de-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="e06de-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="e06de-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="e06de-269">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-269">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e06de-270">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-270">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="e06de-271">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-271">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="e06de-272">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-272">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="e06de-273">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-273">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="e06de-274">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-274">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e06de-275">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-275">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="e06de-276">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-276">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="e06de-277">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-277">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="e06de-278">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="e06de-278">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="e06de-279">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-279">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="e06de-280">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="e06de-280">New cmdlets added:</span></span>
        - <span data-ttu-id="e06de-281">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e06de-281">New-AzIpGroup</span></span>
        - <span data-ttu-id="e06de-282">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e06de-282">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="e06de-283">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e06de-283">Get-AzIpGroup</span></span>
        - <span data-ttu-id="e06de-284">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e06de-284">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e06de-285">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e06de-285">Az.ServiceFabric</span></span>
* <span data-ttu-id="e06de-286">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-286">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-287">Az.Sql</span></span>
* <span data-ttu-id="e06de-288">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-288">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="e06de-289">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-289">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="e06de-290">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="e06de-290">Removed deprecated aliases:</span></span>
* <span data-ttu-id="e06de-291">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="e06de-291">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="e06de-292">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="e06de-292">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="e06de-293">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-293">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e06de-294">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-294">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="e06de-295">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-295">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="e06de-296">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-296">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-297">Az.Storage</span></span>
* <span data-ttu-id="e06de-298">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="e06de-298">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="e06de-299">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e06de-299">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e06de-300">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e06de-300">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e06de-301">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="e06de-301">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="e06de-302">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e06de-302">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="e06de-303">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e06de-303">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="e06de-304">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-304">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="e06de-305">Genel</span><span class="sxs-lookup"><span data-stu-id="e06de-305">General</span></span>
* <span data-ttu-id="e06de-306">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="e06de-306">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e06de-307">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-307">Az.Accounts</span></span>
* <span data-ttu-id="e06de-308">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-308">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e06de-309">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e06de-309">Az.ApiManagement</span></span>
* <span data-ttu-id="e06de-310">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-310">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="e06de-311">https://github.com/Azure/azure-powershell/issues/10068 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-311">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e06de-312">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e06de-312">Az.Automation</span></span>
* <span data-ttu-id="e06de-313">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-313">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="e06de-314">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e06de-314">Az.Batch</span></span>
* <span data-ttu-id="e06de-315">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="e06de-315">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-316">Az.Compute</span></span>
* <span data-ttu-id="e06de-317">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-317">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="e06de-318">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-318">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="e06de-319">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-319">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="e06de-320">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-320">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e06de-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e06de-321">Az.DataFactory</span></span>
* <span data-ttu-id="e06de-322">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="e06de-322">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="e06de-323">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="e06de-323">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="e06de-324">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-324">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e06de-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e06de-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="e06de-326">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-326">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e06de-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e06de-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="e06de-328">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-328">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="e06de-329">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-329">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="e06de-330">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-330">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="e06de-331">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-331">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e06de-332">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e06de-332">Az.IotHub</span></span>
* <span data-ttu-id="e06de-333">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="e06de-333">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="e06de-334">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="e06de-334">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="e06de-335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e06de-335">Az.Monitor</span></span>
* <span data-ttu-id="e06de-336">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-336">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="e06de-337">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="e06de-337">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="e06de-338">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="e06de-338">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="e06de-339">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-339">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-340">Az.Network</span></span>
* <span data-ttu-id="e06de-341">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-341">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="e06de-342">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-342">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="e06de-343">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="e06de-343">New cmdlets added:</span></span>
        - <span data-ttu-id="e06de-344">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="e06de-344">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="e06de-345">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-345">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e06de-346">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-346">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="e06de-347">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-347">Updated cmdlets:</span></span>
        - <span data-ttu-id="e06de-348">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-348">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e06de-349">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-349">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e06de-350">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-350">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e06de-351">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-351">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="e06de-352">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="e06de-352">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="e06de-353">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="e06de-353">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="e06de-354">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="e06de-354">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e06de-355">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e06de-355">Az.RedisCache</span></span>
* <span data-ttu-id="e06de-356">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-356">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-357">Az.Sql</span></span>
* <span data-ttu-id="e06de-358">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-358">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-359">Az.Storage</span></span>
* <span data-ttu-id="e06de-360">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-360">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="e06de-361">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="e06de-361">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e06de-362">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e06de-362">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="e06de-363">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="e06de-363">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e06de-364">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e06de-364">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e06de-365">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e06de-365">Az.StorageSync</span></span>
* <span data-ttu-id="e06de-366">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-366">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-367">Az.Websites</span></span>
* <span data-ttu-id="e06de-368">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="e06de-368">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="e06de-369">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-369">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e06de-370">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e06de-370">Az.ApiManagement</span></span>
* <span data-ttu-id="e06de-371">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-371">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="e06de-372">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-372">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="e06de-373">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="e06de-373">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e06de-374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e06de-374">Az.Automation</span></span>
* <span data-ttu-id="e06de-375">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-375">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="e06de-376">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-376">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="e06de-377">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-377">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-378">Az.Compute</span></span>
* <span data-ttu-id="e06de-379">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-379">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="e06de-380">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-380">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e06de-381">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="e06de-381">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="e06de-382">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-382">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="e06de-383">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-383">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="e06de-384">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-384">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="e06de-385">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-385">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="e06de-386">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-386">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="e06de-387">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-387">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e06de-388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e06de-388">Az.DataFactory</span></span>
* <span data-ttu-id="e06de-389">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="e06de-389">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="e06de-390">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-390">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e06de-391">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e06de-391">Az.HDInsight</span></span>
* <span data-ttu-id="e06de-392">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="e06de-392">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e06de-393">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e06de-393">Az.IotHub</span></span>
* <span data-ttu-id="e06de-394">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-394">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="e06de-395">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-395">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="e06de-396">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e06de-396">New cmdlets are:</span></span>
    - <span data-ttu-id="e06de-397">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e06de-397">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e06de-398">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e06de-398">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e06de-399">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e06de-399">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e06de-400">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e06de-400">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e06de-401">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e06de-401">Az.Monitor</span></span>
* <span data-ttu-id="e06de-402">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="e06de-402">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="e06de-403">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="e06de-403">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="e06de-404">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="e06de-404">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="e06de-405">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="e06de-405">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="e06de-406">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-406">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="e06de-407">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-407">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="e06de-408">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="e06de-408">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="e06de-409">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="e06de-409">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="e06de-410">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-410">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e06de-411">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="e06de-411">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="e06de-412">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-412">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e06de-413">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="e06de-413">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="e06de-414">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-414">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="e06de-415">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="e06de-415">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="e06de-416">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="e06de-416">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="e06de-417">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="e06de-417">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="e06de-418">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="e06de-418">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="e06de-419">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="e06de-419">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="e06de-420">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-420">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="e06de-421">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-421">Overall improved help files</span></span>
* <span data-ttu-id="e06de-422">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-422">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-423">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-423">Az.Network</span></span>
* <span data-ttu-id="e06de-424">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-424">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="e06de-425">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-425">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="e06de-426">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-426">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="e06de-427">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-427">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="e06de-428">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-428">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="e06de-429">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-429">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="e06de-430">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-430">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="e06de-431">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-431">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="e06de-432">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-432">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="e06de-433">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-433">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="e06de-434">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-434">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="e06de-435">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="e06de-435">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="e06de-436">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-436">New cmdlets</span></span>
        - <span data-ttu-id="e06de-437">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="e06de-437">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="e06de-438">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-438">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="e06de-439">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-439">Updated cmdlet:</span></span>
        - <span data-ttu-id="e06de-440">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e06de-440">New-VpnSite</span></span>
        - <span data-ttu-id="e06de-441">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e06de-441">Update-VpnSite</span></span>
        - <span data-ttu-id="e06de-442">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-442">New-VpnConnection</span></span>
        - <span data-ttu-id="e06de-443">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-443">Update-VpnConnection</span></span>
* <span data-ttu-id="e06de-444">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-444">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-445">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-445">Az.RecoveryServices</span></span>
* <span data-ttu-id="e06de-446">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-446">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="e06de-447">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-447">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-448">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-448">Az.Resources</span></span>
* <span data-ttu-id="e06de-449">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-449">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e06de-450">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e06de-450">Az.ServiceFabric</span></span>
* <span data-ttu-id="e06de-451">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-451">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="e06de-452">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="e06de-452">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="e06de-453">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e06de-453">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e06de-454">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e06de-454">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e06de-455">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e06de-455">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e06de-456">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e06de-456">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="e06de-457">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e06de-457">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e06de-458">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e06de-458">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e06de-459">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e06de-459">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e06de-460">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e06de-460">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e06de-461">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e06de-461">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="e06de-462">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e06de-462">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e06de-463">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e06de-463">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e06de-464">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e06de-464">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e06de-465">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="e06de-465">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="e06de-466">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-466">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e06de-467">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e06de-467">Az.SignalR</span></span>
* <span data-ttu-id="e06de-468">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-468">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-469">Az.Sql</span></span>
* <span data-ttu-id="e06de-470">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-470">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="e06de-471">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-471">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="e06de-472">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-472">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="e06de-473">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-473">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="e06de-474">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-474">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-475">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-475">Az.Storage</span></span>
* <span data-ttu-id="e06de-476">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-476">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="e06de-477">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-477">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="e06de-478">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e06de-478">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="e06de-479">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e06de-479">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="e06de-480">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-480">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="e06de-481">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e06de-481">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="e06de-482">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-482">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="e06de-483">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e06de-483">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e06de-484">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e06de-484">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e06de-485">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e06de-485">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e06de-486">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e06de-486">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-487">Az.Websites</span></span>
* <span data-ttu-id="e06de-488">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="e06de-488">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="e06de-489">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="e06de-489">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="e06de-490">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-490">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="e06de-491">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-491">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="e06de-492">Genel</span><span class="sxs-lookup"><span data-stu-id="e06de-492">General</span></span>
* <span data-ttu-id="e06de-493">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-493">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e06de-494">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-494">Az.Accounts</span></span>
* <span data-ttu-id="e06de-495">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="e06de-495">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="e06de-496">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e06de-496">Az.Aks</span></span>
* <span data-ttu-id="e06de-497">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-497">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="e06de-498">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="e06de-498">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e06de-499">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e06de-499">Az.ApiManagement</span></span>
* <span data-ttu-id="e06de-500">https://github.com/Azure/azure-powershell/issues/9351 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-500">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="e06de-501">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-501">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="e06de-502">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-502">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="e06de-503">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="e06de-503">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="e06de-504">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-504">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e06de-505">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e06de-505">Az.Batch</span></span>
* <span data-ttu-id="e06de-506">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-506">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e06de-507">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e06de-507">Az.Cdn</span></span>
* <span data-ttu-id="e06de-508">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-508">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-509">Az.Compute</span></span>
* <span data-ttu-id="e06de-510">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-510">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="e06de-511">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-511">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="e06de-512">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-512">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="e06de-513">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-513">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="e06de-514">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="e06de-514">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="e06de-515">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-515">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="e06de-516">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-516">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="e06de-517">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-517">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e06de-518">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e06de-518">Az.DataFactory</span></span>
* <span data-ttu-id="e06de-519">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-519">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="e06de-520">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-520">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="e06de-521">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-521">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="e06de-522">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-522">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e06de-523">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e06de-523">Az.DataLakeStore</span></span>
* <span data-ttu-id="e06de-524">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-524">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e06de-525">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e06de-525">Az.EventHub</span></span>
* <span data-ttu-id="e06de-526">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="e06de-526">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="e06de-527">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="e06de-527">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="e06de-528">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-528">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="e06de-529">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="e06de-529">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="e06de-530">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e06de-530">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e06de-531">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-531">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e06de-532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e06de-532">Az.Monitor</span></span>
* <span data-ttu-id="e06de-533">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-533">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-534">Az.Network</span></span>
* <span data-ttu-id="e06de-535">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-535">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="e06de-536">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-536">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="e06de-537">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-537">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="e06de-538">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="e06de-538">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="e06de-539">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="e06de-539">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="e06de-540">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-540">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="e06de-541">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-541">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e06de-542">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e06de-542">Az.OperationalInsights</span></span>
* <span data-ttu-id="e06de-543">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-543">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="e06de-544">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-544">Added example</span></span>
    - <span data-ttu-id="e06de-545">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-545">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="e06de-546">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-546">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="e06de-547">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-547">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-548">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-548">Az.RecoveryServices</span></span>
* <span data-ttu-id="e06de-549">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-549">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-550">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-550">Az.Resources</span></span>
* <span data-ttu-id="e06de-551">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-551">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="e06de-552">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-552">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="e06de-553">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="e06de-553">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="e06de-554">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-554">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e06de-555">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e06de-555">Az.ServiceBus</span></span>
* <span data-ttu-id="e06de-556">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="e06de-556">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="e06de-557">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="e06de-557">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="e06de-558">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-558">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="e06de-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e06de-559">Az.ServiceFabric</span></span>
* <span data-ttu-id="e06de-560">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-560">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="e06de-561">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="e06de-561">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="e06de-562">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="e06de-562">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="e06de-563">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-563">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="e06de-564">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="e06de-564">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="e06de-565">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-565">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-566">Az.Sql</span></span>
* <span data-ttu-id="e06de-567">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-567">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-568">Az.Storage</span></span>
* <span data-ttu-id="e06de-569">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-569">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="e06de-570">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="e06de-570">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="e06de-571">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e06de-571">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="e06de-572">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e06de-572">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="e06de-573">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="e06de-573">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="e06de-574">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e06de-574">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-575">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-575">Az.Websites</span></span>
* <span data-ttu-id="e06de-576">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-576">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="e06de-577">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-577">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e06de-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-578">Az.Accounts</span></span>
* <span data-ttu-id="e06de-579">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-579">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e06de-580">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e06de-580">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e06de-581">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-581">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="e06de-582">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e06de-582">Az.Automation</span></span>
* <span data-ttu-id="e06de-583">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-583">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="e06de-584">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e06de-584">Az.CognitiveServices</span></span>
* <span data-ttu-id="e06de-585">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-585">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-586">Az.Compute</span></span>
* <span data-ttu-id="e06de-587">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-587">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e06de-588">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e06de-588">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e06de-589">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-589">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="e06de-590">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="e06de-590">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e06de-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e06de-591">Az.DataFactory</span></span>
* <span data-ttu-id="e06de-592">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-592">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="e06de-593">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-593">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e06de-594">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e06de-594">Az.EventHub</span></span>
* <span data-ttu-id="e06de-595">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e06de-595">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e06de-596">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-596">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e06de-597">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e06de-597">Az.KeyVault</span></span>
* <span data-ttu-id="e06de-598">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-598">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e06de-599">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e06de-599">Az.LogicApp</span></span>
* <span data-ttu-id="e06de-600">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="e06de-600">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="e06de-601">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-601">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e06de-602">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e06de-602">Az.ManagedServices</span></span>
* <span data-ttu-id="e06de-603">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="e06de-603">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-604">Az.Network</span></span>
* <span data-ttu-id="e06de-605">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-605">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="e06de-606">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-606">New cmdlets</span></span>
        - <span data-ttu-id="e06de-607">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e06de-607">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e06de-608">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e06de-608">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e06de-609">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-609">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e06de-610">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-610">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e06de-611">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-611">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e06de-612">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-612">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e06de-613">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="e06de-613">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="e06de-614">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e06de-614">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="e06de-615">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="e06de-615">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="e06de-616">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-616">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="e06de-617">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-617">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="e06de-618">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-618">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="e06de-619">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-619">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="e06de-620">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-620">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="e06de-621">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-621">Updated cmdlets</span></span>
        - <span data-ttu-id="e06de-622">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-622">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e06de-623">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-623">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e06de-624">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-624">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e06de-625">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-625">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e06de-626">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-626">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="e06de-627">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-627">Updated cmdlet:</span></span>
        - <span data-ttu-id="e06de-628">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-628">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e06de-629">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-629">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e06de-630">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-630">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="e06de-631">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-631">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="e06de-632">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-632">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="e06de-633">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="e06de-633">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e06de-634">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e06de-634">Az.OperationalInsights</span></span>
* <span data-ttu-id="e06de-635">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-635">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="e06de-636">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-636">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-637">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-637">Az.RecoveryServices</span></span>
* <span data-ttu-id="e06de-638">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-638">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e06de-639">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-639">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="e06de-640">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-640">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="e06de-641">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-641">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e06de-642">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-642">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="e06de-643">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-643">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e06de-644">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-644">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="e06de-645">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-645">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e06de-646">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-646">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="e06de-647">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-647">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-648">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-648">Az.Resources</span></span>
- <span data-ttu-id="e06de-649">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-649">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="e06de-650">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-650">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e06de-651">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e06de-651">Az.ServiceBus</span></span>
* <span data-ttu-id="e06de-652">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e06de-652">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e06de-653">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-653">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-654">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-654">Az.Sql</span></span>
* <span data-ttu-id="e06de-655">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-655">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="e06de-656">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-656">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="e06de-657">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-657">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-658">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-658">Az.Storage</span></span>
* <span data-ttu-id="e06de-659">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-659">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e06de-660">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e06de-660">Az.StorageSync</span></span>
* <span data-ttu-id="e06de-661">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-661">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="e06de-662">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-662">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-663">Az.Websites</span></span>
* <span data-ttu-id="e06de-664">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-664">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="e06de-665">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-665">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="e06de-666">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-666">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="e06de-667">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-667">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e06de-668">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-668">Az.Accounts</span></span>
* <span data-ttu-id="e06de-669">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-669">Add support for profile cmdlets</span></span>
* <span data-ttu-id="e06de-670">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-670">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="e06de-671">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-671">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e06de-672">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e06de-672">Az.Advisor</span></span>
* <span data-ttu-id="e06de-673">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="e06de-673">GA release of Az.Advisor</span></span>
* <span data-ttu-id="e06de-674">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="e06de-674">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e06de-675">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e06de-675">Az.ApiManagement</span></span>
* <span data-ttu-id="e06de-676">https://github.com/Azure/azure-powershell/issues/8671 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-676">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="e06de-677">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e06de-677">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="e06de-678">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-678">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="e06de-679">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="e06de-679">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="e06de-680">https://github.com/Azure/azure-powershell/issues/9307 ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="e06de-680">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="e06de-681">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e06de-681">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="e06de-682">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-682">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e06de-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e06de-683">Az.Automation</span></span>
* <span data-ttu-id="e06de-684">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-684">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-685">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-685">Az.Compute</span></span>
* <span data-ttu-id="e06de-686">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-686">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e06de-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e06de-687">Az.DataFactory</span></span>
* <span data-ttu-id="e06de-688">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-688">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e06de-689">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e06de-689">Az.EventGrid</span></span>
* <span data-ttu-id="e06de-690">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-690">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e06de-691">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e06de-691">Az.IotHub</span></span>
* <span data-ttu-id="e06de-692">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-692">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-693">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-693">Az.Network</span></span>
* <span data-ttu-id="e06de-694">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-694">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="e06de-695">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-695">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e06de-696">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e06de-696">Az.PolicyInsights</span></span>
* <span data-ttu-id="e06de-697">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-697">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="e06de-698">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="e06de-698">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e06de-699">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e06de-699">Az.OperationalInsights</span></span>
* <span data-ttu-id="e06de-700">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-700">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-701">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-701">Az.RecoveryServices</span></span>
* <span data-ttu-id="e06de-702">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="e06de-702">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-703">Az.Resources</span></span>
    - <span data-ttu-id="e06de-704">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="e06de-704">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="e06de-705">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-705">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="e06de-706">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-706">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="e06de-707">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-707">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e06de-708">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e06de-708">Az.ServiceBus</span></span>
* <span data-ttu-id="e06de-709">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-709">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-710">Az.Sql</span></span>
* <span data-ttu-id="e06de-711">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-711">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="e06de-712">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-712">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="e06de-713">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e06de-713">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e06de-714">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e06de-714">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e06de-715">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e06de-715">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e06de-716">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e06de-716">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e06de-717">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e06de-717">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e06de-718">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e06de-718">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="e06de-719">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-719">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-720">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-720">Az.Storage</span></span>
* <span data-ttu-id="e06de-721">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-721">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="e06de-722">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e06de-722">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="e06de-723">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-723">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="e06de-724">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="e06de-724">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="e06de-725">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-725">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="e06de-726">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e06de-726">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e06de-727">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e06de-727">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e06de-728">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-728">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="e06de-729">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e06de-729">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="e06de-730">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e06de-730">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e06de-731">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e06de-731">Az.StorageSync</span></span>
* <span data-ttu-id="e06de-732">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="e06de-732">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="e06de-733">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-733">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e06de-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-734">Az.Accounts</span></span>
* <span data-ttu-id="e06de-735">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-735">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="e06de-736">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="e06de-736">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="e06de-737">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-737">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="e06de-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e06de-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="e06de-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="e06de-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-740">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-740">Az.Compute</span></span>
* <span data-ttu-id="e06de-741">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-741">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="e06de-742">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-742">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="e06de-743">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e06de-743">Az.Dns</span></span>
* <span data-ttu-id="e06de-744">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-744">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e06de-745">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e06de-745">Az.EventGrid</span></span>
* <span data-ttu-id="e06de-746">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-746">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="e06de-747">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="e06de-747">New cmdlets:</span></span>
    - <span data-ttu-id="e06de-748">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e06de-748">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e06de-749">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e06de-749">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e06de-750">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e06de-750">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e06de-751">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="e06de-751">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="e06de-752">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e06de-752">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e06de-753">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e06de-753">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e06de-754">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e06de-754">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e06de-755">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="e06de-755">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e06de-756">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e06de-756">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e06de-757">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e06de-757">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="e06de-758">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e06de-758">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e06de-759">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e06de-759">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="e06de-760">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e06de-760">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="e06de-761">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="e06de-761">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="e06de-762">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e06de-762">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e06de-763">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e06de-763">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="e06de-764">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-764">Updated cmdlets:</span></span>
    - <span data-ttu-id="e06de-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e06de-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="e06de-766">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="e06de-766">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e06de-767">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="e06de-767">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e06de-768">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="e06de-768">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="e06de-769">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="e06de-769">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="e06de-770">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="e06de-770">Event subscription expiration date,</span></span>
            - <span data-ttu-id="e06de-771">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="e06de-771">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="e06de-772">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="e06de-772">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="e06de-773">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="e06de-773">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="e06de-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e06de-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="e06de-775">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="e06de-775">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="e06de-776">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e06de-776">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="e06de-777">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="e06de-777">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="e06de-778">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="e06de-778">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e06de-779">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e06de-779">Az.FrontDoor</span></span>
* <span data-ttu-id="e06de-780">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="e06de-780">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="e06de-781">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="e06de-781">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="e06de-782">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e06de-782">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="e06de-783">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="e06de-783">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-784">Az.Network</span></span>
* <span data-ttu-id="e06de-785">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="e06de-785">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="e06de-786">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-786">New cmdlets</span></span>
        - <span data-ttu-id="e06de-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e06de-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="e06de-788">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="e06de-788">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="e06de-789">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-789">New cmdlets</span></span> 
        - <span data-ttu-id="e06de-790">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e06de-790">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="e06de-791">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="e06de-791">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="e06de-792">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-792">New cmdlets</span></span> 
        - <span data-ttu-id="e06de-793">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e06de-793">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="e06de-794">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e06de-794">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e06de-795">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e06de-795">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e06de-796">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-796">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="e06de-797">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-797">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e06de-798">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="e06de-798">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="e06de-799">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-799">New cmdlets</span></span>
        - <span data-ttu-id="e06de-800">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e06de-800">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e06de-801">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e06de-801">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e06de-802">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e06de-802">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e06de-803">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="e06de-803">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="e06de-804">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="e06de-804">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="e06de-805">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-805">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="e06de-806">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-806">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="e06de-807">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-807">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="e06de-808">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-808">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="e06de-809">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-809">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="e06de-810">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-810">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="e06de-811">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-811">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="e06de-812">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-812">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="e06de-813">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-813">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="e06de-814">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-814">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="e06de-815">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-815">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="e06de-816">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-816">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="e06de-817">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-817">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="e06de-818">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-818">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e06de-819">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-819">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="e06de-820">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-820">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="e06de-821">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e06de-821">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="e06de-822">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e06de-822">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="e06de-823">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="e06de-823">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="e06de-824">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-824">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e06de-825">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-825">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e06de-826">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-826">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e06de-827">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e06de-827">Az.OperationalInsights</span></span>
* <span data-ttu-id="e06de-828">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-828">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-829">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-829">Az.Resources</span></span>
* <span data-ttu-id="e06de-830">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="e06de-830">Support for additional Template Export options</span></span>
    - <span data-ttu-id="e06de-831">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-831">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e06de-832">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-832">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e06de-833">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-833">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e06de-834">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e06de-834">Az.ServiceFabric</span></span>
* <span data-ttu-id="e06de-835">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-835">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-836">Az.Sql</span></span>
* <span data-ttu-id="e06de-837">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-837">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="e06de-838">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-838">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="e06de-839">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-839">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="e06de-840">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e06de-840">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e06de-841">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e06de-841">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e06de-842">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e06de-842">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e06de-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e06de-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="e06de-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e06de-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-845">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-845">Az.Storage</span></span>
* <span data-ttu-id="e06de-846">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="e06de-846">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="e06de-847">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e06de-847">New-AzStorageAccount</span></span>
* <span data-ttu-id="e06de-848">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-848">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="e06de-849">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e06de-849">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-850">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-850">Az.Websites</span></span>
* <span data-ttu-id="e06de-851">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="e06de-851">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="e06de-852">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="e06de-852">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="e06de-853">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-853">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="e06de-854">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e06de-854">Az.Cdn</span></span>
* <span data-ttu-id="e06de-855">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-855">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-856">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-856">Az.Compute</span></span>
* <span data-ttu-id="e06de-857">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-857">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="e06de-858">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e06de-858">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e06de-859">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e06de-859">Az.EventHub</span></span>
* <span data-ttu-id="e06de-860">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="e06de-860">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="e06de-861">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="e06de-861">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-862">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-862">Az.Network</span></span>
* <span data-ttu-id="e06de-863">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-863">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="e06de-864">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-864">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e06de-865">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e06de-865">Az.PolicyInsights</span></span>
* <span data-ttu-id="e06de-866">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-866">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="e06de-868">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-868">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e06de-869">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e06de-869">Az.ServiceBus</span></span>
* <span data-ttu-id="e06de-870">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="e06de-870">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e06de-871">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e06de-871">Az.ServiceFabric</span></span>
* <span data-ttu-id="e06de-872">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-872">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="e06de-873">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-873">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-874">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-874">Az.Sql</span></span>
* <span data-ttu-id="e06de-875">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-875">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="e06de-876">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-876">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e06de-877">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-877">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="e06de-878">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="e06de-878">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-879">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-879">Az.Websites</span></span>
* <span data-ttu-id="e06de-880">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="e06de-880">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="e06de-881">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-881">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e06de-882">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e06de-882">Az.ApiManagement</span></span>
* <span data-ttu-id="e06de-883">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="e06de-883">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="e06de-884">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="e06de-884">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="e06de-885">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="e06de-885">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="e06de-886">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="e06de-886">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="e06de-887">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e06de-887">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="e06de-888">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="e06de-888">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="e06de-889">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="e06de-889">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="e06de-890">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="e06de-890">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="e06de-891">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="e06de-891">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="e06de-892">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="e06de-892">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="e06de-893">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="e06de-893">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="e06de-894">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="e06de-894">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="e06de-895">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="e06de-895">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="e06de-896">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="e06de-896">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="e06de-897">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="e06de-897">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="e06de-898">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="e06de-898">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="e06de-899">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="e06de-899">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="e06de-900">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="e06de-900">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="e06de-901">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="e06de-901">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="e06de-902">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="e06de-902">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="e06de-903">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="e06de-903">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="e06de-904">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="e06de-904">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="e06de-905">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="e06de-905">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="e06de-906">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-906">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="e06de-907">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-907">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="e06de-908">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-908">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="e06de-909">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="e06de-909">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="e06de-910">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e06de-910">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="e06de-911">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-911">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="e06de-912">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-912">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="e06de-913">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-913">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="e06de-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="e06de-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="e06de-915">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-915">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="e06de-916">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-916">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e06de-917">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="e06de-917">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="e06de-918">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="e06de-918">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="e06de-919">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="e06de-919">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="e06de-920">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-920">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="e06de-921">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-921">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="e06de-922">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-922">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="e06de-923">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="e06de-923">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e06de-924">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="e06de-924">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e06de-925">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="e06de-925">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="e06de-926">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="e06de-926">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e06de-927">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-927">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e06de-928">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="e06de-928">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e06de-929">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="e06de-929">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="e06de-930">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="e06de-930">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e06de-931">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-931">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="e06de-932">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="e06de-932">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="e06de-933">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="e06de-933">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="e06de-934">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="e06de-934">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="e06de-935">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="e06de-935">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="e06de-936">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-936">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="e06de-937">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="e06de-937">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="e06de-938">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="e06de-938">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="e06de-939">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-939">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e06de-940">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="e06de-940">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e06de-941">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="e06de-941">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e06de-942">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-942">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e06de-943">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-943">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e06de-944">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="e06de-944">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e06de-945">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="e06de-945">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e06de-946">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-946">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e06de-947">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-947">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="e06de-948">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="e06de-948">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="e06de-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="e06de-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="e06de-950">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="e06de-950">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="e06de-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="e06de-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="e06de-952">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e06de-952">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="e06de-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="e06de-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="e06de-954">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="e06de-954">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="e06de-955">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="e06de-955">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="e06de-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="e06de-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="e06de-957">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="e06de-957">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="e06de-958">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e06de-958">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="e06de-959">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="e06de-959">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e06de-960">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e06de-960">Az.Automation</span></span>
* <span data-ttu-id="e06de-961">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-961">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="e06de-962">https://github.com/Azure/azure-powershell/issues/7977 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-962">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="e06de-963">https://github.com/Azure/azure-powershell/issues/8600 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-963">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="e06de-964">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-964">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="e06de-965">https://github.com/Azure/azure-powershell/issues/8347 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-965">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="e06de-966">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-966">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="e06de-967">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-967">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-968">Az.Compute</span></span>
* <span data-ttu-id="e06de-969">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-969">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="e06de-970">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="e06de-970">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e06de-971">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e06de-971">Az.DataLakeStore</span></span>
* <span data-ttu-id="e06de-972">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-972">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e06de-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e06de-973">Az.Monitor</span></span>
* <span data-ttu-id="e06de-974">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-974">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-975">Az.Network</span></span>
* <span data-ttu-id="e06de-976">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-976">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="e06de-977">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="e06de-977">Updated cmdlet:</span></span>
        - <span data-ttu-id="e06de-978">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e06de-978">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="e06de-979">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-979">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-980">Az.Resources</span></span>
* <span data-ttu-id="e06de-981">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-981">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-982">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-982">Az.Sql</span></span>
* <span data-ttu-id="e06de-983">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="e06de-983">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="e06de-984">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-984">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e06de-985">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-985">Az.Accounts</span></span>
* <span data-ttu-id="e06de-986">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="e06de-986">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e06de-987">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e06de-987">Az.CognitiveServices</span></span>
* <span data-ttu-id="e06de-988">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="e06de-988">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="e06de-989">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="e06de-989">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-990">Az.Compute</span></span>
* <span data-ttu-id="e06de-991">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="e06de-991">Proximity placement group feature.</span></span>
    - <span data-ttu-id="e06de-992">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e06de-992">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="e06de-993">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-993">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="e06de-994">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-994">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="e06de-995">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="e06de-995">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="e06de-996">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-996">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="e06de-997">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="e06de-997">Breaking changes</span></span>
    - <span data-ttu-id="e06de-998">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-998">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="e06de-999">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-999">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e06de-1000">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e06de-1000">Az.DeploymentManager</span></span>
* <span data-ttu-id="e06de-1001">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="e06de-1001">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="e06de-1002">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e06de-1002">Az.Dns</span></span>
* <span data-ttu-id="e06de-1003">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="e06de-1003">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="e06de-1004">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="e06de-1004">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="e06de-1005">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="e06de-1005">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e06de-1006">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e06de-1006">Az.FrontDoor</span></span>
* <span data-ttu-id="e06de-1007">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="e06de-1007">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="e06de-1008">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="e06de-1008">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="e06de-1009">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e06de-1009">Az.HDInsight</span></span>
* <span data-ttu-id="e06de-1010">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="e06de-1010">Removed two cmdlets:</span></span>
    - <span data-ttu-id="e06de-1011">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e06de-1011">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="e06de-1012">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e06de-1012">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e06de-1013">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1013">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e06de-1014">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="e06de-1014">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="e06de-1015">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="e06de-1015">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="e06de-1016">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="e06de-1016">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e06de-1017">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e06de-1017">Az.Monitor</span></span>
* <span data-ttu-id="e06de-1018">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="e06de-1018">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="e06de-1019">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e06de-1019">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="e06de-1020">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="e06de-1020">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="e06de-1021">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e06de-1021">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="e06de-1022">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e06de-1022">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="e06de-1023">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="e06de-1023">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="e06de-1024">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="e06de-1024">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="e06de-1025">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e06de-1025">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e06de-1026">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e06de-1026">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e06de-1027">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e06de-1027">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e06de-1028">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e06de-1028">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e06de-1029">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e06de-1029">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e06de-1030">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="e06de-1030">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="e06de-1031">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1031">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-1032">Az.Network</span></span>
* <span data-ttu-id="e06de-1033">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="e06de-1033">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="e06de-1034">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-1034">New cmdlets</span></span>
        - <span data-ttu-id="e06de-1035">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e06de-1035">New-AzNatGateway</span></span>
        - <span data-ttu-id="e06de-1036">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e06de-1036">Get-AzNatGateway</span></span>
        - <span data-ttu-id="e06de-1037">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e06de-1037">Set-AzNatGateway</span></span>
        - <span data-ttu-id="e06de-1038">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e06de-1038">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="e06de-1039">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1039">Updated cmdlets</span></span>
        - <span data-ttu-id="e06de-1040">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e06de-1040">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="e06de-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e06de-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="e06de-1042">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="e06de-1042">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="e06de-1043">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1043">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="e06de-1044">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1044">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e06de-1045">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e06de-1045">Az.PolicyInsights</span></span>
* <span data-ttu-id="e06de-1046">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-1046">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="e06de-1047">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e06de-1047">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="e06de-1048">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="e06de-1048">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-1049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1049">Az.RecoveryServices</span></span>
* <span data-ttu-id="e06de-1050">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-1050">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="e06de-1051">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="e06de-1051">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="e06de-1052">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="e06de-1052">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="e06de-1053">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="e06de-1053">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="e06de-1054">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="e06de-1054">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="e06de-1055">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="e06de-1055">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="e06de-1056">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e06de-1056">Az.Relay</span></span>
* <span data-ttu-id="e06de-1057">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="e06de-1057">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e06de-1058">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e06de-1058">Az.ServiceBus</span></span>
* <span data-ttu-id="e06de-1059">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1059">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-1060">Az.Storage</span></span>
* <span data-ttu-id="e06de-1061">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="e06de-1061">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="e06de-1062">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="e06de-1062">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="e06de-1063">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="e06de-1063">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="e06de-1064">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e06de-1064">New-AzStorageAccount</span></span>
* <span data-ttu-id="e06de-1065">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="e06de-1065">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="e06de-1066">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e06de-1066">New-AzStorageAccount</span></span>
    - <span data-ttu-id="e06de-1067">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e06de-1067">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="e06de-1068">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e06de-1068">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-1069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-1069">Az.Websites</span></span>
* <span data-ttu-id="e06de-1070">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="e06de-1070">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="e06de-1071">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1071">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="e06de-1072">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-1072">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e06de-1073">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="e06de-1073">Highlights since the last major release</span></span>
* <span data-ttu-id="e06de-1074">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="e06de-1074">General availability of `Az` module</span></span>
* <span data-ttu-id="e06de-1075">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e06de-1075">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e06de-1076">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e06de-1076">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e06de-1077">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1077">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e06de-1078">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1078">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e06de-1079">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1079">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e06de-1080">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-1080">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e06de-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-1081">Az.Accounts</span></span>
* <span data-ttu-id="e06de-1082">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1082">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e06de-1083">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e06de-1083">Az.Batch</span></span>
* <span data-ttu-id="e06de-1084">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1084">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e06de-1085">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e06de-1085">Az.Cdn</span></span>
* <span data-ttu-id="e06de-1086">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1086">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e06de-1087">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1087">Az.CognitiveServices</span></span>
* <span data-ttu-id="e06de-1088">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1088">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-1089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1089">Az.Compute</span></span>
* <span data-ttu-id="e06de-1090">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1090">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e06de-1091">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1091">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e06de-1092">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1092">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e06de-1093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e06de-1093">Az.DataFactory</span></span>
* <span data-ttu-id="e06de-1094">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1094">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e06de-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e06de-1095">Az.DataLakeStore</span></span>
* <span data-ttu-id="e06de-1096">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1096">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e06de-1097">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e06de-1097">Az.EventGrid</span></span>
* <span data-ttu-id="e06de-1098">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1098">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e06de-1099">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e06de-1099">Az.EventHub</span></span>
* <span data-ttu-id="e06de-1100">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1100">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="e06de-1101">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e06de-1101">Az.HDInsight</span></span>
* <span data-ttu-id="e06de-1102">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1102">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e06de-1103">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e06de-1103">Az.IotHub</span></span>
* <span data-ttu-id="e06de-1104">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1104">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e06de-1105">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e06de-1105">Az.KeyVault</span></span>
* <span data-ttu-id="e06de-1106">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1106">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e06de-1107">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1107">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e06de-1108">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e06de-1108">Az.MachineLearning</span></span>
* <span data-ttu-id="e06de-1109">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1109">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e06de-1110">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e06de-1110">Az.Media</span></span>
* <span data-ttu-id="e06de-1111">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1111">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e06de-1112">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e06de-1112">Az.Monitor</span></span>
  * <span data-ttu-id="e06de-1113">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="e06de-1113">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e06de-1114">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e06de-1114">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e06de-1115">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e06de-1115">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e06de-1116">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e06de-1116">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e06de-1117">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e06de-1117">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e06de-1118">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e06de-1118">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e06de-1119">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1119">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-1120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-1120">Az.Network</span></span>
* <span data-ttu-id="e06de-1121">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e06de-1122">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1122">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e06de-1123">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e06de-1123">Az.NotificationHubs</span></span>
* <span data-ttu-id="e06de-1124">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1124">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e06de-1125">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e06de-1125">Az.OperationalInsights</span></span>
* <span data-ttu-id="e06de-1126">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e06de-1127">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e06de-1127">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e06de-1128">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-1129">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1129">Az.RecoveryServices</span></span>
* <span data-ttu-id="e06de-1130">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1130">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e06de-1131">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="e06de-1131">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e06de-1132">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1132">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e06de-1133">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1133">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e06de-1134">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e06de-1134">Az.RedisCache</span></span>
* <span data-ttu-id="e06de-1135">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1136">Az.Resources</span></span>
* <span data-ttu-id="e06de-1137">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1137">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-1138">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-1138">Az.Sql</span></span>
* <span data-ttu-id="e06de-1139">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1139">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e06de-1140">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e06de-1141">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1141">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e06de-1142">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1142">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e06de-1143">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1143">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e06de-1144">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-1144">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e06de-1145">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1145">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-1146">Az.Websites</span></span>
* <span data-ttu-id="e06de-1147">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1147">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e06de-1148">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1148">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e06de-1149">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1149">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e06de-1150">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1150">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e06de-1151">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-1151">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e06de-1152">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="e06de-1152">Highlights since the last major release</span></span>
* <span data-ttu-id="e06de-1153">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="e06de-1153">General availability of `Az` module</span></span>
* <span data-ttu-id="e06de-1154">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e06de-1154">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e06de-1155">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e06de-1155">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e06de-1156">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1156">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e06de-1157">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1157">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e06de-1158">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1158">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e06de-1159">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-1159">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e06de-1160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-1160">Az.Accounts</span></span>
* <span data-ttu-id="e06de-1161">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1161">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e06de-1162">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1162">Az.AnalysisServices</span></span>
* <span data-ttu-id="e06de-1163">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e06de-1163">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e06de-1164">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="e06de-1164">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e06de-1165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e06de-1165">Az.Automation</span></span>
* <span data-ttu-id="e06de-1166">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1166">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e06de-1167">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-1167">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e06de-1168">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="e06de-1168">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1169">Az.Compute</span></span>
* <span data-ttu-id="e06de-1170">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1170">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e06de-1171">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1171">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="e06de-1172">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e06de-1172">Az.ContainerInstance</span></span>
* <span data-ttu-id="e06de-1173">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1173">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e06de-1174">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e06de-1174">Az.DataFactory</span></span>
* <span data-ttu-id="e06de-1175">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1175">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e06de-1176">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1176">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-1177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1177">Az.Resources</span></span>
* <span data-ttu-id="e06de-1178">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1178">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e06de-1179">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1179">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e06de-1180">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1180">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e06de-1181">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e06de-1181">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e06de-1182">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1182">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e06de-1183">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e06de-1183">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-1184">Az.Sql</span></span>
* <span data-ttu-id="e06de-1185">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-1185">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-1186">Az.Storage</span></span>
* <span data-ttu-id="e06de-1187">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="e06de-1187">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e06de-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e06de-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="e06de-1189">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="e06de-1189">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e06de-1190">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e06de-1190">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e06de-1191">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e06de-1191">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e06de-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e06de-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e06de-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e06de-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e06de-1194">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="e06de-1194">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e06de-1195">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e06de-1195">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e06de-1196">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e06de-1196">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e06de-1197">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e06de-1197">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e06de-1198">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e06de-1198">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e06de-1199">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-1199">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e06de-1200">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="e06de-1200">Highlights since the last major release</span></span>
* <span data-ttu-id="e06de-1201">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="e06de-1201">General availability of `Az` module</span></span>
* <span data-ttu-id="e06de-1202">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e06de-1202">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e06de-1203">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e06de-1203">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e06de-1204">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1204">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e06de-1205">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1205">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e06de-1206">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1206">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e06de-1207">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-1207">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e06de-1208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e06de-1208">Az.Automation</span></span>
* <span data-ttu-id="e06de-1209">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="e06de-1209">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e06de-1210">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="e06de-1210">Dynamic grouping</span></span>
    * <span data-ttu-id="e06de-1211">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="e06de-1211">Pre-Post script</span></span>
    * <span data-ttu-id="e06de-1212">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="e06de-1212">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-1213">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1213">Az.Compute</span></span>
* <span data-ttu-id="e06de-1214">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="e06de-1214">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e06de-1215">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1215">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e06de-1216">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e06de-1216">Az.KeyVault</span></span>
* <span data-ttu-id="e06de-1217">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1217">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-1218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-1218">Az.Network</span></span>
* <span data-ttu-id="e06de-1219">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1219">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e06de-1220">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1220">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="e06de-1222">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1222">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e06de-1223">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1223">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-1224">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1224">Az.Resources</span></span>
* <span data-ttu-id="e06de-1225">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1225">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e06de-1226">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1226">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-1227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-1227">Az.Sql</span></span>
* <span data-ttu-id="e06de-1228">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1228">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-1229">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-1229">Az.Storage</span></span>
* <span data-ttu-id="e06de-1230">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="e06de-1230">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e06de-1231">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e06de-1231">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e06de-1232">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e06de-1232">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e06de-1233">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e06de-1233">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e06de-1234">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e06de-1234">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e06de-1235">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e06de-1235">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e06de-1236">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e06de-1236">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-1237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-1237">Az.Websites</span></span>
* <span data-ttu-id="e06de-1238">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1238">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="e06de-1239">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-1239">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e06de-1240">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-1240">Az.Accounts</span></span>
* <span data-ttu-id="e06de-1241">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1241">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e06de-1242">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1242">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e06de-1243">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e06de-1243">Az.Automation</span></span>
* <span data-ttu-id="e06de-1244">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1244">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e06de-1245">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1245">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e06de-1246">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="e06de-1246">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e06de-1247">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e06de-1247">Az.Cdn</span></span>
* <span data-ttu-id="e06de-1248">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-1248">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-1249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1249">Az.Compute</span></span>
* <span data-ttu-id="e06de-1250">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1250">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e06de-1251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e06de-1251">Az.DataFactory</span></span>
* <span data-ttu-id="e06de-1252">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1252">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e06de-1253">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e06de-1253">Az.LogicApp</span></span>
* <span data-ttu-id="e06de-1254">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="e06de-1254">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-1255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-1255">Az.Network</span></span>
* <span data-ttu-id="e06de-1256">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1256">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1257">Az.RecoveryServices</span></span>
* <span data-ttu-id="e06de-1258">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1258">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e06de-1259">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="e06de-1259">SDK Update</span></span>
* <span data-ttu-id="e06de-1260">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-1260">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e06de-1261">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1261">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-1262">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1262">Az.Resources</span></span>
* <span data-ttu-id="e06de-1263">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1263">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e06de-1264">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="e06de-1264">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e06de-1265">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1265">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e06de-1266">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="e06de-1266">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e06de-1267">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1267">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e06de-1268">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="e06de-1268">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-1269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-1269">Az.Sql</span></span>
* <span data-ttu-id="e06de-1270">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-1270">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e06de-1271">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-1271">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-1272">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-1272">Az.Storage</span></span>
* <span data-ttu-id="e06de-1273">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e06de-1273">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e06de-1274">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-1274">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e06de-1275">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1275">Az.AnalysisServices</span></span>
* <span data-ttu-id="e06de-1276">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-1276">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e06de-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e06de-1277">Az.Automation</span></span>
* <span data-ttu-id="e06de-1278">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1278">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e06de-1279">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1279">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e06de-1280">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1280">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e06de-1281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1281">Az.CognitiveServices</span></span>
* <span data-ttu-id="e06de-1282">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1282">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-1283">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1283">Az.Compute</span></span>
* <span data-ttu-id="e06de-1284">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1284">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e06de-1285">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1285">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e06de-1286">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1286">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e06de-1287">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="e06de-1287">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e06de-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e06de-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="e06de-1289">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1289">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e06de-1290">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e06de-1290">Az.EventHub</span></span>
* <span data-ttu-id="e06de-1291">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1291">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="e06de-1292">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e06de-1292">Az.KeyVault</span></span>
* <span data-ttu-id="e06de-1293">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1293">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e06de-1294">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e06de-1294">Az.LogicApp</span></span>
* <span data-ttu-id="e06de-1295">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1295">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e06de-1296">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1296">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e06de-1297">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-1297">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e06de-1298">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e06de-1298">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e06de-1299">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e06de-1299">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e06de-1300">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e06de-1300">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e06de-1301">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e06de-1301">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e06de-1302">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="e06de-1302">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e06de-1303">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e06de-1303">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e06de-1304">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e06de-1304">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e06de-1305">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e06de-1305">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e06de-1306">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e06de-1306">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e06de-1307">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1307">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e06de-1308">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e06de-1308">Az.Monitor</span></span>
* <span data-ttu-id="e06de-1309">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1309">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-1310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-1310">Az.Network</span></span>
* <span data-ttu-id="e06de-1311">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1311">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e06de-1312">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e06de-1312">Az.OperationalInsights</span></span>
* <span data-ttu-id="e06de-1313">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="e06de-1313">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e06de-1314">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1314">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="e06de-1315">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1315">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="e06de-1316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1316">Az.Resources</span></span>
* <span data-ttu-id="e06de-1317">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1317">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e06de-1318">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1318">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e06de-1319">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1319">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e06de-1320">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1320">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-1321">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-1321">Az.Sql</span></span>
* <span data-ttu-id="e06de-1322">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1322">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e06de-1323">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1323">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-1324">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-1324">Az.Websites</span></span>
* <span data-ttu-id="e06de-1325">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1325">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e06de-1326">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-1326">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e06de-1327">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-1327">Az.Accounts</span></span>
* <span data-ttu-id="e06de-1328">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e06de-1328">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e06de-1329">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1329">Az.AnalysisServices</span></span>
<span data-ttu-id="e06de-1330">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="e06de-1330">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-1331">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1331">Az.Compute</span></span>
* <span data-ttu-id="e06de-1332">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1332">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e06de-1333">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1333">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e06de-1334">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1334">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-1335">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1335">Az.RecoveryServices</span></span>
<span data-ttu-id="e06de-1336">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="e06de-1336">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-1337">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1337">Az.Resources</span></span>
* <span data-ttu-id="e06de-1338">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1338">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="e06de-1339">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e06de-1339">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e06de-1340">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1340">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="e06de-1341">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e06de-1341">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-1342">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-1342">Az.Sql</span></span>
* <span data-ttu-id="e06de-1343">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e06de-1343">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e06de-1344">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1344">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e06de-1345">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1345">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e06de-1346">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-1346">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e06de-1347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-1347">Az.Accounts</span></span>
* <span data-ttu-id="e06de-1348">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="e06de-1348">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e06de-1349">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1349">Az.AnalysisServices</span></span>
* <span data-ttu-id="e06de-1350">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="e06de-1350">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-1351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1351">Az.RecoveryServices</span></span>
* <span data-ttu-id="e06de-1352">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="e06de-1352">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e06de-1353">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-1353">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e06de-1354">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-1354">Az.Accounts</span></span>
* <span data-ttu-id="e06de-1355">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1355">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e06de-1356">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1356">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e06de-1357">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1357">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e06de-1358">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e06de-1358">Az.Aks</span></span>
* <span data-ttu-id="e06de-1359">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1359">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e06de-1360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e06de-1360">Az.Automation</span></span>
* <span data-ttu-id="e06de-1361">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1361">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e06de-1362">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1362">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e06de-1363">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e06de-1363">Az.Cdn</span></span>
* <span data-ttu-id="e06de-1364">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1364">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-1365">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1365">Az.Compute</span></span>
* <span data-ttu-id="e06de-1366">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1366">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e06de-1367">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1367">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e06de-1368">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1368">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e06de-1369">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e06de-1369">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e06de-1370">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1370">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e06de-1371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e06de-1371">Az.DataFactory</span></span>
* <span data-ttu-id="e06de-1372">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1372">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e06de-1373">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e06de-1373">Az.DataLakeStore</span></span>
* <span data-ttu-id="e06de-1374">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1374">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e06de-1375">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="e06de-1375">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e06de-1376">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1376">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e06de-1377">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e06de-1377">Az.IotHub</span></span>
* <span data-ttu-id="e06de-1378">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1378">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e06de-1379">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e06de-1379">Az.KeyVault</span></span>
* <span data-ttu-id="e06de-1380">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1380">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-1381">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-1381">Az.Network</span></span>
* <span data-ttu-id="e06de-1382">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1382">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-1383">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1383">Az.Resources</span></span>
* <span data-ttu-id="e06de-1384">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1384">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e06de-1385">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1385">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e06de-1386">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1386">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e06de-1387">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1387">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e06de-1388">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1388">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e06de-1389">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1389">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e06de-1390">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="e06de-1390">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e06de-1391">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e06de-1391">Az.ServiceFabric</span></span>
* <span data-ttu-id="e06de-1392">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="e06de-1392">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e06de-1393">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1393">Fix some error messages.</span></span>
* <span data-ttu-id="e06de-1394">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1394">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e06de-1395">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1395">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e06de-1396">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e06de-1396">Az.SignalR</span></span>
* <span data-ttu-id="e06de-1397">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1397">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-1398">Az.Sql</span></span>
* <span data-ttu-id="e06de-1399">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1399">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e06de-1400">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1400">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e06de-1401">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1401">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e06de-1402">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="e06de-1402">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-1403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-1403">Az.Storage</span></span>
* <span data-ttu-id="e06de-1404">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1404">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e06de-1405">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-1405">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e06de-1406">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e06de-1406">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e06de-1407">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e06de-1407">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e06de-1408">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e06de-1408">Az.TrafficManager</span></span>
* <span data-ttu-id="e06de-1409">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1409">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-1410">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-1410">Az.Websites</span></span>
* <span data-ttu-id="e06de-1411">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1411">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e06de-1412">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1412">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e06de-1413">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1413">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e06de-1414">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="e06de-1414">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e06de-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-1415">Az.Accounts</span></span>
* <span data-ttu-id="e06de-1416">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1416">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-1417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1417">Az.Compute</span></span>
* <span data-ttu-id="e06de-1418">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="e06de-1418">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e06de-1419">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1419">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e06de-1420">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="e06de-1420">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e06de-1421">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e06de-1421">Az.DataLakeStore</span></span>
* <span data-ttu-id="e06de-1422">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1422">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e06de-1423">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1423">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e06de-1424">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e06de-1424">Az.EventGrid</span></span>
* <span data-ttu-id="e06de-1425">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1425">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e06de-1426">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1426">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e06de-1427">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="e06de-1427">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e06de-1428">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="e06de-1428">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e06de-1429">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="e06de-1429">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e06de-1430">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="e06de-1430">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e06de-1431">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="e06de-1431">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e06de-1432">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="e06de-1432">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e06de-1433">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="e06de-1433">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e06de-1434">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="e06de-1434">Dead letter endpoint.</span></span>
* <span data-ttu-id="e06de-1435">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1435">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e06de-1436">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-1436">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e06de-1437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e06de-1437">Az.IotHub</span></span>
* <span data-ttu-id="e06de-1438">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1438">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e06de-1439">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e06de-1439">Az.LogicApp</span></span>
* <span data-ttu-id="e06de-1440">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="e06de-1440">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1441">Az.Resources</span></span>
* <span data-ttu-id="e06de-1442">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1442">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e06de-1443">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="e06de-1443">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e06de-1444">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1444">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e06de-1445">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1445">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e06de-1446">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1446">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e06de-1447">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="e06de-1447">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e06de-1448">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e06de-1448">Az.SignalR</span></span>
* <span data-ttu-id="e06de-1449">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="e06de-1449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-1450">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-1450">Az.Sql</span></span>
* <span data-ttu-id="e06de-1451">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="e06de-1451">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e06de-1452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-1452">Az.Storage</span></span>
* <span data-ttu-id="e06de-1453">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="e06de-1453">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e06de-1454">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e06de-1454">New-AzStorageContext</span></span>
* <span data-ttu-id="e06de-1455">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1455">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e06de-1456">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e06de-1456">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-1457">Az.Websites</span></span>
* <span data-ttu-id="e06de-1458">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1458">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e06de-1459">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="e06de-1459">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e06de-1460">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="e06de-1460">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e06de-1461">Genel</span><span class="sxs-lookup"><span data-stu-id="e06de-1461">General</span></span>

- <span data-ttu-id="e06de-1462">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="e06de-1462">General Availability of Az Module</span></span>
- <span data-ttu-id="e06de-1463">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="e06de-1463">Online help for each module</span></span>
- <span data-ttu-id="e06de-1464">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="e06de-1464">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e06de-1465">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1465">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e06de-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e06de-1466">Az.Accounts</span></span>
- <span data-ttu-id="e06de-1467">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e06de-1467">Changed from Az.Profile</span></span>
- <span data-ttu-id="e06de-1468">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1468">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e06de-1469">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e06de-1469">Az.ApiManagement</span></span>
- <span data-ttu-id="e06de-1470">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="e06de-1470">Fixes for #7002</span></span>
- <span data-ttu-id="e06de-1471">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1471">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e06de-1472">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e06de-1472">Az.Batch</span></span>
- <span data-ttu-id="e06de-1473">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1473">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e06de-1474">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="e06de-1474">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e06de-1475">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1475">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e06de-1476">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e06de-1476">Az.Billing</span></span>
- <span data-ttu-id="e06de-1477">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1477">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e06de-1478">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1478">Az.CognitivServices</span></span>
- <span data-ttu-id="e06de-1479">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1479">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e06de-1480">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-1480">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e06de-1481">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e06de-1481">Az.ContainerInstance</span></span>
- <span data-ttu-id="e06de-1482">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1482">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e06de-1483">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e06de-1483">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e06de-1484">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1484">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e06de-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e06de-1485">Az.DataLakeStore</span></span>
- <span data-ttu-id="e06de-1486">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1486">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e06de-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e06de-1487">Az.Monitor</span></span>
- <span data-ttu-id="e06de-1488">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1488">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e06de-1489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e06de-1489">Az.KeyVault</span></span>
- <span data-ttu-id="e06de-1490">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-1490">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e06de-1491">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e06de-1491">Az.MachineLearning</span></span>
- <span data-ttu-id="e06de-1492">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1492">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e06de-1493">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e06de-1493">Az.Media</span></span>
- <span data-ttu-id="e06de-1494">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e06de-1494">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e06de-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-1495">Az.Network</span></span>
<span data-ttu-id="e06de-1496">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1496">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e06de-1497">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="e06de-1497">New cmdlets added:</span></span>
        - <span data-ttu-id="e06de-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e06de-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e06de-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e06de-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e06de-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e06de-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e06de-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e06de-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e06de-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e06de-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e06de-1503">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e06de-1503">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e06de-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e06de-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e06de-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e06de-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e06de-1506">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1506">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e06de-1507">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e06de-1507">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e06de-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e06de-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e06de-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e06de-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e06de-1510">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-1510">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e06de-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e06de-1512">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1512">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e06de-1513">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1513">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e06de-1514">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e06de-1514">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e06de-1515">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e06de-1515">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e06de-1516">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e06de-1516">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e06de-1517">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1517">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e06de-1518">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e06de-1519">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e06de-1519">Az.OperationalInsights</span></span>
- <span data-ttu-id="e06de-1520">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1520">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e06de-1521">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e06de-1521">Az.Profile</span></span>
- <span data-ttu-id="e06de-1522">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1522">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-1523">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1523">Az.RecoveryServices</span></span>
- <span data-ttu-id="e06de-1524">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1524">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e06de-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1525">Az.Resources</span></span>
- <span data-ttu-id="e06de-1526">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1526">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e06de-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e06de-1527">Az.ServiceFabric</span></span>
- <span data-ttu-id="e06de-1528">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="e06de-1528">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e06de-1529">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1529">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e06de-1530">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e06de-1530">Az.SIgnalR</span></span>
- <span data-ttu-id="e06de-1531">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="e06de-1531">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e06de-1532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-1532">Az.Sql</span></span>
- <span data-ttu-id="e06de-1533">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1533">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e06de-1534">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1534">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e06de-1535">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e06de-1536">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-1536">Az.Storage</span></span>
- <span data-ttu-id="e06de-1537">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e06de-1538">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-1538">Az.Websites</span></span>
- <span data-ttu-id="e06de-1539">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e06de-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e06de-1540">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="e06de-1540">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e06de-1541">Genel</span><span class="sxs-lookup"><span data-stu-id="e06de-1541">General</span></span>

* <span data-ttu-id="e06de-1542">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="e06de-1542">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e06de-1543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1543">Az.Compute</span></span>

* <span data-ttu-id="e06de-1544">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1544">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e06de-1545">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e06de-1545">Az.DataLakeStore</span></span>

* <span data-ttu-id="e06de-1546">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1546">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e06de-1547">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e06de-1547">Az.FrontDoor</span></span>

* <span data-ttu-id="e06de-1548">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1548">Fixed some broken links</span></span>
    - <span data-ttu-id="e06de-1549">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1549">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e06de-1550">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1550">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e06de-1551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1551">Az.RecoveryServices</span></span>

* <span data-ttu-id="e06de-1552">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1552">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e06de-1553">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1553">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e06de-1554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1554">Az.Resources</span></span>

* <span data-ttu-id="e06de-1555">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="e06de-1555">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e06de-1556">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1556">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e06de-1557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-1557">Az.Sql</span></span>

* <span data-ttu-id="e06de-1558">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="e06de-1558">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e06de-1559">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1559">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e06de-1560">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1560">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e06de-1561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e06de-1561">Az.Storage</span></span>

* <span data-ttu-id="e06de-1562">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1562">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e06de-1563">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1563">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e06de-1564">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e06de-1564">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e06de-1565">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1565">Support Static Website configuration</span></span>
    - <span data-ttu-id="e06de-1566">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e06de-1566">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e06de-1567">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e06de-1567">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e06de-1568">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-1568">Az.Websites</span></span>

* <span data-ttu-id="e06de-1569">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e06de-1569">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="e06de-1570">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1570">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e06de-1571">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="e06de-1571">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e06de-1572">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="e06de-1572">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e06de-1573">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e06de-1573">Az.ApiManagement</span></span>
* <span data-ttu-id="e06de-1574">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="e06de-1574">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e06de-1575">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e06de-1575">Az.Automation</span></span>
* <span data-ttu-id="e06de-1576">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="e06de-1576">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e06de-1577">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1577">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e06de-1578">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1578">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e06de-1579">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1579">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e06de-1580">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1580">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e06de-1581">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1581">Az.Compute</span></span>
* <span data-ttu-id="e06de-1582">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1582">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e06de-1583">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="e06de-1583">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e06de-1584">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e06de-1584">Az.ContainerInstance</span></span>
* <span data-ttu-id="e06de-1585">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="e06de-1585">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e06de-1586">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e06de-1586">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e06de-1587">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1587">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e06de-1588">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-1588">Az.Network</span></span>
* <span data-ttu-id="e06de-1589">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1589">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e06de-1590">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1590">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e06de-1591">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1591">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="e06de-1592">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1592">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e06de-1593">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e06de-1593">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e06de-1594">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1594">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e06de-1595">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="e06de-1595">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e06de-1596">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e06de-1596">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e06de-1597">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1597">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e06de-1598">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="e06de-1598">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e06de-1599">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e06de-1599">Az.Relay</span></span>
* <span data-ttu-id="e06de-1600">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1600">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e06de-1601">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1601">Az.Resources</span></span>
* <span data-ttu-id="e06de-1602">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1602">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e06de-1603">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1603">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e06de-1604">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="e06de-1604">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e06de-1605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e06de-1605">Az.ServiceFabric</span></span>
* <span data-ttu-id="e06de-1606">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1606">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e06de-1607">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-1607">Az.Sql</span></span>
* <span data-ttu-id="e06de-1608">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1608">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e06de-1609">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e06de-1609">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e06de-1610">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e06de-1610">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e06de-1611">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e06de-1611">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e06de-1612">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e06de-1612">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e06de-1613">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e06de-1613">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e06de-1614">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e06de-1614">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e06de-1615">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e06de-1615">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e06de-1616">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e06de-1616">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e06de-1617">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1617">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e06de-1618">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1618">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e06de-1619">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1619">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e06de-1620">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e06de-1620">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e06de-1621">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e06de-1621">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e06de-1622">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e06de-1622">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e06de-1623">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e06de-1623">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e06de-1624">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1624">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e06de-1625">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="e06de-1625">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e06de-1626">Genel</span><span class="sxs-lookup"><span data-stu-id="e06de-1626">General</span></span>
* <span data-ttu-id="e06de-1627">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="e06de-1627">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e06de-1628">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e06de-1628">Az.Profile</span></span>
* <span data-ttu-id="e06de-1629">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1629">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e06de-1630">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1630">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e06de-1631">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1631">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e06de-1632">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1632">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e06de-1633">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1633">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e06de-1634">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1634">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e06de-1635">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1635">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e06de-1636">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1636">Az.CognitiveServices</span></span>
* <span data-ttu-id="e06de-1637">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1637">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-1638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1638">Az.Compute</span></span>
* <span data-ttu-id="e06de-1639">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1639">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e06de-1640">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="e06de-1640">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e06de-1641">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1641">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e06de-1642">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e06de-1642">Az.DataLakeStore</span></span>
* <span data-ttu-id="e06de-1643">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1643">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e06de-1644">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1644">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e06de-1645">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e06de-1645">Az.Insights</span></span>
* <span data-ttu-id="e06de-1646">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1646">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e06de-1647">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="e06de-1647">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e06de-1648">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1648">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e06de-1649">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="e06de-1649">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-1650">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-1650">Az.Network</span></span>
* <span data-ttu-id="e06de-1651">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="e06de-1651">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e06de-1652">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e06de-1652">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e06de-1653">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e06de-1653">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e06de-1654">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e06de-1654">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e06de-1655">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e06de-1655">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e06de-1656">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e06de-1656">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e06de-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e06de-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e06de-1658">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e06de-1658">Az.PolicyInsights</span></span>
* <span data-ttu-id="e06de-1659">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1659">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1660">Az.Resources</span></span>
* <span data-ttu-id="e06de-1661">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="e06de-1661">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e06de-1662">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="e06de-1662">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e06de-1663">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e06de-1663">Az.ServiceBus</span></span>
* <span data-ttu-id="e06de-1664">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1664">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e06de-1665">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e06de-1665">Az.ServiceFabric</span></span>
* <span data-ttu-id="e06de-1666">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1666">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e06de-1667">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1667">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e06de-1668">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="e06de-1668">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e06de-1669">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e06de-1669">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e06de-1670">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1670">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e06de-1671">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="e06de-1671">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e06de-1672">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e06de-1672">Az.Profile</span></span>
* <span data-ttu-id="e06de-1673">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="e06de-1673">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e06de-1674">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1674">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-1675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1675">Az.Compute</span></span>
* <span data-ttu-id="e06de-1676">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1676">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e06de-1677">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1677">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e06de-1678">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e06de-1678">Az.DataLakeStore</span></span>
* <span data-ttu-id="e06de-1679">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="e06de-1679">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e06de-1680">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="e06de-1680">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e06de-1681">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="e06de-1681">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e06de-1682">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e06de-1682">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e06de-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="e06de-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-1684">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-1684">Az.Network</span></span>
* <span data-ttu-id="e06de-1685">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-1685">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e06de-1686">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1686">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1687">Az.Resources</span></span>
* <span data-ttu-id="e06de-1688">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1688">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e06de-1689">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1689">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e06de-1690">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="e06de-1690">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e06de-1691">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="e06de-1691">Azure.Storage</span></span>
* <span data-ttu-id="e06de-1692">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="e06de-1692">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e06de-1693">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e06de-1693">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e06de-1694">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e06de-1694">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e06de-1695">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="e06de-1695">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e06de-1696">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e06de-1696">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="e06de-1697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e06de-1697">Az.CognitiveServices</span></span>
* <span data-ttu-id="e06de-1698">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="e06de-1698">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e06de-1699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e06de-1699">Az.Compute</span></span>
* <span data-ttu-id="e06de-1700">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1700">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e06de-1701">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1701">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e06de-1702">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1702">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e06de-1703">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e06de-1703">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e06de-1704">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1704">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e06de-1705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e06de-1705">Az.Network</span></span>
* <span data-ttu-id="e06de-1706">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e06de-1706">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e06de-1707">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1707">new cmdlets added</span></span>
    - <span data-ttu-id="e06de-1708">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e06de-1708">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e06de-1709">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e06de-1709">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e06de-1710">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e06de-1710">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e06de-1711">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e06de-1711">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e06de-1712">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-1712">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e06de-1713">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e06de-1713">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e06de-1714">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1714">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e06de-1715">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1715">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e06de-1716">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1716">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e06de-1717">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e06de-1717">Az.RedisCache</span></span>
* <span data-ttu-id="e06de-1718">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="e06de-1718">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e06de-1719">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1719">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e06de-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e06de-1720">Az.Resources</span></span>
* <span data-ttu-id="e06de-1721">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e06de-1721">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e06de-1722">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1722">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e06de-1723">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e06de-1723">Az.Sql</span></span>
* <span data-ttu-id="e06de-1724">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e06de-1724">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e06de-1725">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e06de-1725">Az.Websites</span></span>
* <span data-ttu-id="e06de-1726">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="e06de-1726">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e06de-1727">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="e06de-1727">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e06de-1728">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="e06de-1728">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e06de-1729">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="e06de-1729">Initial Release</span></span>
