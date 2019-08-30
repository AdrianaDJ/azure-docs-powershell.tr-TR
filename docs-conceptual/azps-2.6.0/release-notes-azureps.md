---
ms.openlocfilehash: f89d13d6bbedaea29b62287942d8c7a509abe32b
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052643"
---
## <a name="260---august-2019"></a><span data-ttu-id="124de-101">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="124de-101">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="124de-102">Genel</span><span class="sxs-lookup"><span data-stu-id="124de-102">General</span></span>
* <span data-ttu-id="124de-103">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-103">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="124de-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-104">Az.Accounts</span></span>
* <span data-ttu-id="124de-105">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="124de-105">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="124de-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="124de-106">Az.Aks</span></span>
* <span data-ttu-id="124de-107">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-107">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="124de-108">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="124de-108">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="124de-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="124de-109">Az.ApiManagement</span></span>
* <span data-ttu-id="124de-110">https://github.com/Azure/azure-powershell/issues/9351 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-110">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="124de-111">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-111">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="124de-112">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-112">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="124de-113">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="124de-113">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="124de-114">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-114">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="124de-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="124de-115">Az.Batch</span></span>
* <span data-ttu-id="124de-116">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-116">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="124de-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="124de-117">Az.Cdn</span></span>
* <span data-ttu-id="124de-118">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-118">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-119">Az.Compute</span></span>
* <span data-ttu-id="124de-120">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-120">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="124de-121">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-121">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="124de-122">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-122">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="124de-123">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-123">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="124de-124">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="124de-124">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="124de-125">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-125">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="124de-126">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-126">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="124de-127">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-127">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="124de-128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="124de-128">Az.DataFactory</span></span>
* <span data-ttu-id="124de-129">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-129">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="124de-130">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-130">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="124de-131">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-131">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="124de-132">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-132">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="124de-133">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="124de-133">Az.DataLakeStore</span></span>
* <span data-ttu-id="124de-134">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-134">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="124de-135">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="124de-135">Az.EventHub</span></span>
* <span data-ttu-id="124de-136">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="124de-136">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="124de-137">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="124de-137">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="124de-138">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-138">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="124de-139">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="124de-139">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="124de-140">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="124de-140">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="124de-141">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-141">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="124de-142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="124de-142">Az.Monitor</span></span>
* <span data-ttu-id="124de-143">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-143">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-144">Az.Network</span></span>
* <span data-ttu-id="124de-145">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-145">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="124de-146">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-146">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="124de-147">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-147">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="124de-148">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="124de-148">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="124de-149">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="124de-149">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="124de-150">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-150">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="124de-151">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-151">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="124de-152">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="124de-152">Az.OperationalInsights</span></span>
* <span data-ttu-id="124de-153">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-153">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="124de-154">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-154">Added example</span></span>
    - <span data-ttu-id="124de-155">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-155">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="124de-156">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-156">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="124de-157">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-157">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="124de-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="124de-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="124de-159">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-159">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-160">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-160">Az.Resources</span></span>
* <span data-ttu-id="124de-161">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-161">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="124de-162">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-162">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="124de-163">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="124de-163">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="124de-164">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-164">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="124de-165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="124de-165">Az.ServiceBus</span></span>
* <span data-ttu-id="124de-166">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="124de-166">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="124de-167">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="124de-167">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="124de-168">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-168">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="124de-169">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="124de-169">Az.ServiceFabric</span></span>
* <span data-ttu-id="124de-170">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="124de-170">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="124de-171">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="124de-171">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="124de-172">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="124de-172">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="124de-173">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-173">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="124de-174">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="124de-174">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="124de-175">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="124de-175">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-176">Az.Sql</span></span>
* <span data-ttu-id="124de-177">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-177">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="124de-178">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="124de-178">Az.Storage</span></span>
* <span data-ttu-id="124de-179">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-179">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="124de-180">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="124de-180">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="124de-181">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="124de-181">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="124de-182">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="124de-182">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="124de-183">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="124de-183">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="124de-184">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="124de-184">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="124de-185">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-185">Az.Websites</span></span>
* <span data-ttu-id="124de-186">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-186">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="124de-187">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="124de-187">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="124de-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-188">Az.Accounts</span></span>
* <span data-ttu-id="124de-189">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-189">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="124de-190">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="124de-190">Az.ApplicationInsights</span></span>
* <span data-ttu-id="124de-191">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-191">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="124de-192">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="124de-192">Az.Automation</span></span>
* <span data-ttu-id="124de-193">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-193">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="124de-194">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="124de-194">Az.CognitiveServices</span></span>
* <span data-ttu-id="124de-195">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-195">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-196">Az.Compute</span></span>
* <span data-ttu-id="124de-197">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-197">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="124de-198">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="124de-198">Az.ContainerRegistry</span></span>
* <span data-ttu-id="124de-199">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-199">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="124de-200">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="124de-200">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="124de-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="124de-201">Az.DataFactory</span></span>
* <span data-ttu-id="124de-202">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-202">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="124de-203">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-203">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="124de-204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="124de-204">Az.EventHub</span></span>
* <span data-ttu-id="124de-205">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="124de-205">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="124de-206">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-206">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="124de-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="124de-207">Az.KeyVault</span></span>
* <span data-ttu-id="124de-208">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-208">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="124de-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="124de-209">Az.LogicApp</span></span>
* <span data-ttu-id="124de-210">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="124de-210">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="124de-211">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-211">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="124de-212">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="124de-212">Az.ManagedServices</span></span>
* <span data-ttu-id="124de-213">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="124de-213">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-214">Az.Network</span></span>
* <span data-ttu-id="124de-215">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-215">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="124de-216">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="124de-216">New cmdlets</span></span>
        - <span data-ttu-id="124de-217">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="124de-217">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="124de-218">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="124de-218">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="124de-219">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="124de-219">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="124de-220">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="124de-220">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="124de-221">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="124de-221">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="124de-222">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="124de-222">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="124de-223">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="124de-223">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="124de-224">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="124de-224">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="124de-225">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="124de-225">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="124de-226">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-226">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="124de-227">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanmasını etkinleştirmeyi veya devre dışı bırakmayı göstermek için isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-227">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="124de-228">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanmasını etkinleştirmeyi veya devre dışı bırakmayı göstermek için isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-228">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="124de-229">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="124de-229">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="124de-230">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-230">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="124de-231">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-231">Updated cmdlets</span></span>
        - <span data-ttu-id="124de-232">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="124de-232">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="124de-233">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="124de-233">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="124de-234">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="124de-234">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="124de-235">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-235">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="124de-236">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-236">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="124de-237">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="124de-237">Updated cmdlet:</span></span>
        - <span data-ttu-id="124de-238">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="124de-238">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="124de-239">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="124de-239">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="124de-240">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="124de-240">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="124de-241">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-241">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="124de-242">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-242">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="124de-243">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="124de-243">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="124de-244">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="124de-244">Az.OperationalInsights</span></span>
* <span data-ttu-id="124de-245">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-245">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="124de-246">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-246">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="124de-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="124de-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="124de-248">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-248">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="124de-249">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-249">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="124de-250">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-250">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="124de-251">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-251">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="124de-252">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-252">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="124de-253">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-253">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="124de-254">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-254">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="124de-255">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-255">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="124de-256">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-256">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="124de-257">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-257">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-258">Az.Resources</span></span>
- <span data-ttu-id="124de-259">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="124de-259">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="124de-260">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-260">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="124de-261">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="124de-261">Az.ServiceBus</span></span>
* <span data-ttu-id="124de-262">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="124de-262">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="124de-263">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-263">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-264">Az.Sql</span></span>
* <span data-ttu-id="124de-265">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-265">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="124de-266">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-266">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="124de-267">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-267">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="124de-268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="124de-268">Az.Storage</span></span>
* <span data-ttu-id="124de-269">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-269">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="124de-270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="124de-270">Az.StorageSync</span></span>
* <span data-ttu-id="124de-271">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="124de-271">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="124de-272">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-272">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="124de-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-273">Az.Websites</span></span>
* <span data-ttu-id="124de-274">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-274">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="124de-275">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-275">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="124de-276">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-276">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="124de-277">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="124de-277">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="124de-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-278">Az.Accounts</span></span>
* <span data-ttu-id="124de-279">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-279">Add support for profile cmdlets</span></span>
* <span data-ttu-id="124de-280">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-280">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="124de-281">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-281">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="124de-282">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="124de-282">Az.Advisor</span></span>
* <span data-ttu-id="124de-283">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="124de-283">GA release of Az.Advisor</span></span>
* <span data-ttu-id="124de-284">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="124de-284">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="124de-285">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="124de-285">Az.ApiManagement</span></span>
* <span data-ttu-id="124de-286">https://github.com/Azure/azure-powershell/issues/8671 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-286">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="124de-287">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="124de-287">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="124de-288">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-288">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="124de-289">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="124de-289">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="124de-290">https://github.com/Azure/azure-powershell/issues/9307 ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="124de-290">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="124de-291">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="124de-291">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="124de-292">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-292">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="124de-293">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="124de-293">Az.Automation</span></span>
* <span data-ttu-id="124de-294">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-294">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-295">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-295">Az.Compute</span></span>
* <span data-ttu-id="124de-296">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-296">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="124de-297">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="124de-297">Az.DataFactory</span></span>
* <span data-ttu-id="124de-298">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="124de-298">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="124de-299">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="124de-299">Az.EventGrid</span></span>
* <span data-ttu-id="124de-300">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-300">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="124de-301">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="124de-301">Az.IotHub</span></span>
* <span data-ttu-id="124de-302">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-302">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-303">Az.Network</span></span>
* <span data-ttu-id="124de-304">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-304">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="124de-305">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-305">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="124de-306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="124de-306">Az.PolicyInsights</span></span>
* <span data-ttu-id="124de-307">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-307">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="124de-308">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="124de-308">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="124de-309">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="124de-309">Az.OperationalInsights</span></span>
* <span data-ttu-id="124de-310">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-310">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="124de-311">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="124de-311">Az.RecoveryServices</span></span>
* <span data-ttu-id="124de-312">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="124de-312">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-313">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-313">Az.Resources</span></span>
    - <span data-ttu-id="124de-314">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="124de-314">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="124de-315">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-315">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="124de-316">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-316">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="124de-317">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-317">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="124de-318">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="124de-318">Az.ServiceBus</span></span>
* <span data-ttu-id="124de-319">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-319">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-320">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-320">Az.Sql</span></span>
* <span data-ttu-id="124de-321">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-321">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="124de-322">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="124de-322">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="124de-323">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="124de-323">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="124de-324">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="124de-324">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="124de-325">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="124de-325">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="124de-326">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="124de-326">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="124de-327">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="124de-327">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="124de-328">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="124de-328">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="124de-329">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="124de-329">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="124de-330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="124de-330">Az.Storage</span></span>
* <span data-ttu-id="124de-331">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="124de-331">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="124de-332">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="124de-332">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="124de-333">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-333">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="124de-334">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="124de-334">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="124de-335">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-335">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="124de-336">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="124de-336">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="124de-337">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="124de-337">Set-AzStorageAccount</span></span>
* <span data-ttu-id="124de-338">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-338">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="124de-339">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="124de-339">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="124de-340">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="124de-340">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="124de-341">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="124de-341">Az.StorageSync</span></span>
* <span data-ttu-id="124de-342">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="124de-342">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="124de-343">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="124de-343">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="124de-344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-344">Az.Accounts</span></span>
* <span data-ttu-id="124de-345">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-345">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="124de-346">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="124de-346">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="124de-347">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-347">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="124de-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="124de-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="124de-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="124de-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-350">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-350">Az.Compute</span></span>
* <span data-ttu-id="124de-351">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="124de-351">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="124de-352">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-352">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="124de-353">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="124de-353">Az.Dns</span></span>
* <span data-ttu-id="124de-354">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-354">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="124de-355">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="124de-355">Az.EventGrid</span></span>
* <span data-ttu-id="124de-356">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-356">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="124de-357">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="124de-357">New cmdlets:</span></span>
    - <span data-ttu-id="124de-358">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="124de-358">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="124de-359">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="124de-359">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="124de-360">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="124de-360">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="124de-361">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="124de-361">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="124de-362">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="124de-362">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="124de-363">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="124de-363">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="124de-364">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="124de-364">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="124de-365">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="124de-365">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="124de-366">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="124de-366">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="124de-367">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="124de-367">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="124de-368">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="124de-368">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="124de-369">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="124de-369">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="124de-370">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="124de-370">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="124de-371">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="124de-371">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="124de-372">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="124de-372">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="124de-373">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="124de-373">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="124de-374">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="124de-374">Updated cmdlets:</span></span>
    - <span data-ttu-id="124de-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="124de-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="124de-376">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="124de-376">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="124de-377">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="124de-377">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="124de-378">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="124de-378">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="124de-379">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="124de-379">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="124de-380">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="124de-380">Event subscription expiration date,</span></span>
            - <span data-ttu-id="124de-381">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="124de-381">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="124de-382">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="124de-382">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="124de-383">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="124de-383">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="124de-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="124de-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="124de-385">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="124de-385">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="124de-386">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="124de-386">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="124de-387">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="124de-387">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="124de-388">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="124de-388">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="124de-389">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="124de-389">Az.FrontDoor</span></span>
* <span data-ttu-id="124de-390">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="124de-390">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="124de-391">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="124de-391">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="124de-392">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="124de-392">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="124de-393">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="124de-393">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-394">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-394">Az.Network</span></span>
* <span data-ttu-id="124de-395">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="124de-395">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="124de-396">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="124de-396">New cmdlets</span></span>
        - <span data-ttu-id="124de-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="124de-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="124de-398">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="124de-398">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="124de-399">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="124de-399">New cmdlets</span></span> 
        - <span data-ttu-id="124de-400">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="124de-400">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="124de-401">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="124de-401">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="124de-402">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="124de-402">New cmdlets</span></span> 
        - <span data-ttu-id="124de-403">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="124de-403">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="124de-404">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="124de-404">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="124de-405">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="124de-405">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="124de-406">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="124de-406">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="124de-407">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="124de-407">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="124de-408">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="124de-408">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="124de-409">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="124de-409">New cmdlets</span></span>
        - <span data-ttu-id="124de-410">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="124de-410">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="124de-411">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="124de-411">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="124de-412">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="124de-412">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="124de-413">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="124de-413">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="124de-414">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="124de-414">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="124de-415">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-415">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="124de-416">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-416">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="124de-417">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-417">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="124de-418">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-418">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="124de-419">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-419">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="124de-420">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-420">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="124de-421">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-421">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="124de-422">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-422">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="124de-423">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-423">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="124de-424">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-424">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="124de-425">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-425">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="124de-426">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-426">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="124de-427">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-427">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="124de-428">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="124de-428">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="124de-429">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-429">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="124de-430">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-430">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="124de-431">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="124de-431">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="124de-432">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="124de-432">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="124de-433">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="124de-433">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="124de-434">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-434">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="124de-435">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-435">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="124de-436">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-436">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="124de-437">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="124de-437">Az.OperationalInsights</span></span>
* <span data-ttu-id="124de-438">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-438">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-439">Az.Resources</span></span>
* <span data-ttu-id="124de-440">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="124de-440">Support for additional Template Export options</span></span>
    - <span data-ttu-id="124de-441">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-441">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="124de-442">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-442">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="124de-443">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-443">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="124de-444">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="124de-444">Az.ServiceFabric</span></span>
* <span data-ttu-id="124de-445">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-445">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-446">Az.Sql</span></span>
* <span data-ttu-id="124de-447">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-447">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="124de-448">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-448">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="124de-449">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="124de-449">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="124de-450">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="124de-450">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="124de-451">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="124de-451">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="124de-452">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="124de-452">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="124de-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="124de-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="124de-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="124de-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="124de-455">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="124de-455">Az.Storage</span></span>
* <span data-ttu-id="124de-456">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="124de-456">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="124de-457">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="124de-457">New-AzStorageAccount</span></span>
* <span data-ttu-id="124de-458">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-458">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="124de-459">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="124de-459">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="124de-460">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-460">Az.Websites</span></span>
* <span data-ttu-id="124de-461">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="124de-461">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="124de-462">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="124de-462">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="124de-463">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="124de-463">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="124de-464">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="124de-464">Az.Cdn</span></span>
* <span data-ttu-id="124de-465">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-465">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-466">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-466">Az.Compute</span></span>
* <span data-ttu-id="124de-467">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-467">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="124de-468">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="124de-468">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="124de-469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="124de-469">Az.EventHub</span></span>
* <span data-ttu-id="124de-470">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="124de-470">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="124de-471">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="124de-471">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-472">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-472">Az.Network</span></span>
* <span data-ttu-id="124de-473">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-473">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="124de-474">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-474">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="124de-475">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="124de-475">Az.PolicyInsights</span></span>
* <span data-ttu-id="124de-476">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-476">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="124de-477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="124de-477">Az.RecoveryServices</span></span>
* <span data-ttu-id="124de-478">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-478">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="124de-479">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="124de-479">Az.ServiceBus</span></span>
* <span data-ttu-id="124de-480">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="124de-480">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="124de-481">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="124de-481">Az.ServiceFabric</span></span>
* <span data-ttu-id="124de-482">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-482">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="124de-483">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-483">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-484">Az.Sql</span></span>
* <span data-ttu-id="124de-485">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-485">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="124de-486">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="124de-486">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="124de-487">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="124de-487">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="124de-488">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="124de-488">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="124de-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-489">Az.Websites</span></span>
* <span data-ttu-id="124de-490">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="124de-490">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="124de-491">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="124de-491">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="124de-492">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="124de-492">Az.ApiManagement</span></span>
* <span data-ttu-id="124de-493">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="124de-493">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="124de-494">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="124de-494">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="124de-495">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="124de-495">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="124de-496">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="124de-496">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="124de-497">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="124de-497">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="124de-498">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="124de-498">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="124de-499">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="124de-499">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="124de-500">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="124de-500">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="124de-501">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="124de-501">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="124de-502">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="124de-502">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="124de-503">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="124de-503">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="124de-504">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="124de-504">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="124de-505">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="124de-505">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="124de-506">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="124de-506">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="124de-507">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="124de-507">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="124de-508">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="124de-508">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="124de-509">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="124de-509">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="124de-510">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="124de-510">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="124de-511">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="124de-511">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="124de-512">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="124de-512">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="124de-513">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="124de-513">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="124de-514">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="124de-514">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="124de-515">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="124de-515">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="124de-516">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-516">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="124de-517">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-517">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="124de-518">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-518">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="124de-519">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="124de-519">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="124de-520">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="124de-520">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="124de-521">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-521">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="124de-522">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-522">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="124de-523">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-523">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="124de-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="124de-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="124de-525">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-525">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="124de-526">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-526">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="124de-527">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="124de-527">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="124de-528">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="124de-528">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="124de-529">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="124de-529">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="124de-530">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-530">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="124de-531">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-531">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="124de-532">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-532">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="124de-533">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="124de-533">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="124de-534">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="124de-534">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="124de-535">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="124de-535">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="124de-536">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="124de-536">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="124de-537">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-537">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="124de-538">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="124de-538">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="124de-539">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="124de-539">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="124de-540">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="124de-540">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="124de-541">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-541">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="124de-542">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="124de-542">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="124de-543">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="124de-543">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="124de-544">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="124de-544">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="124de-545">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="124de-545">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="124de-546">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-546">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="124de-547">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="124de-547">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="124de-548">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="124de-548">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="124de-549">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-549">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="124de-550">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="124de-550">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="124de-551">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="124de-551">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="124de-552">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-552">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="124de-553">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-553">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="124de-554">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="124de-554">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="124de-555">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="124de-555">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="124de-556">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-556">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="124de-557">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-557">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="124de-558">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="124de-558">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="124de-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="124de-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="124de-560">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="124de-560">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="124de-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="124de-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="124de-562">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="124de-562">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="124de-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="124de-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="124de-564">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="124de-564">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="124de-565">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="124de-565">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="124de-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="124de-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="124de-567">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="124de-567">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="124de-568">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="124de-568">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="124de-569">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="124de-569">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="124de-570">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="124de-570">Az.Automation</span></span>
* <span data-ttu-id="124de-571">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-571">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="124de-572">https://github.com/Azure/azure-powershell/issues/7977 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-572">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="124de-573">https://github.com/Azure/azure-powershell/issues/8600 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-573">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="124de-574">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-574">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="124de-575">https://github.com/Azure/azure-powershell/issues/8347 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-575">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="124de-576">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-576">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="124de-577">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="124de-577">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-578">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-578">Az.Compute</span></span>
* <span data-ttu-id="124de-579">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-579">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="124de-580">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="124de-580">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="124de-581">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="124de-581">Az.DataLakeStore</span></span>
* <span data-ttu-id="124de-582">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-582">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="124de-583">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="124de-583">Az.Monitor</span></span>
* <span data-ttu-id="124de-584">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-584">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-585">Az.Network</span></span>
* <span data-ttu-id="124de-586">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-586">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="124de-587">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="124de-587">Updated cmdlet:</span></span>
        - <span data-ttu-id="124de-588">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="124de-588">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="124de-589">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-589">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-590">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-590">Az.Resources</span></span>
* <span data-ttu-id="124de-591">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-591">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-592">Az.Sql</span></span>
* <span data-ttu-id="124de-593">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="124de-593">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="124de-594">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="124de-594">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="124de-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-595">Az.Accounts</span></span>
* <span data-ttu-id="124de-596">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="124de-596">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="124de-597">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="124de-597">Az.CognitiveServices</span></span>
* <span data-ttu-id="124de-598">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="124de-598">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="124de-599">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="124de-599">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-600">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-600">Az.Compute</span></span>
* <span data-ttu-id="124de-601">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="124de-601">Proximity placement group feature.</span></span>
    - <span data-ttu-id="124de-602">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="124de-602">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="124de-603">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="124de-603">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="124de-604">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-604">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="124de-605">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="124de-605">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="124de-606">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-606">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="124de-607">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="124de-607">Breaking changes</span></span>
    - <span data-ttu-id="124de-608">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-608">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="124de-609">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-609">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="124de-610">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="124de-610">Az.DeploymentManager</span></span>
* <span data-ttu-id="124de-611">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="124de-611">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="124de-612">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="124de-612">Az.Dns</span></span>
* <span data-ttu-id="124de-613">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="124de-613">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="124de-614">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="124de-614">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="124de-615">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="124de-615">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="124de-616">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="124de-616">Az.FrontDoor</span></span>
* <span data-ttu-id="124de-617">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="124de-617">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="124de-618">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="124de-618">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="124de-619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="124de-619">Az.HDInsight</span></span>
* <span data-ttu-id="124de-620">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="124de-620">Removed two cmdlets:</span></span>
    - <span data-ttu-id="124de-621">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="124de-621">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="124de-622">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="124de-622">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="124de-623">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-623">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="124de-624">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="124de-624">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="124de-625">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="124de-625">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="124de-626">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="124de-626">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="124de-627">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="124de-627">Az.Monitor</span></span>
* <span data-ttu-id="124de-628">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="124de-628">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="124de-629">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="124de-629">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="124de-630">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="124de-630">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="124de-631">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="124de-631">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="124de-632">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="124de-632">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="124de-633">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="124de-633">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="124de-634">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="124de-634">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="124de-635">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="124de-635">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="124de-636">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="124de-636">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="124de-637">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="124de-637">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="124de-638">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="124de-638">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="124de-639">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="124de-639">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="124de-640">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="124de-640">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="124de-641">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-641">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-642">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-642">Az.Network</span></span>
* <span data-ttu-id="124de-643">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="124de-643">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="124de-644">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="124de-644">New cmdlets</span></span>
        - <span data-ttu-id="124de-645">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="124de-645">New-AzNatGateway</span></span>
        - <span data-ttu-id="124de-646">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="124de-646">Get-AzNatGateway</span></span>
        - <span data-ttu-id="124de-647">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="124de-647">Set-AzNatGateway</span></span>
        - <span data-ttu-id="124de-648">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="124de-648">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="124de-649">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-649">Updated cmdlets</span></span>
        - <span data-ttu-id="124de-650">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="124de-650">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="124de-651">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="124de-651">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="124de-652">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="124de-652">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="124de-653">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-653">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="124de-654">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-654">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="124de-655">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="124de-655">Az.PolicyInsights</span></span>
* <span data-ttu-id="124de-656">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="124de-656">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="124de-657">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="124de-657">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="124de-658">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="124de-658">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="124de-659">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="124de-659">Az.RecoveryServices</span></span>
* <span data-ttu-id="124de-660">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="124de-660">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="124de-661">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="124de-661">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="124de-662">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="124de-662">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="124de-663">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="124de-663">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="124de-664">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="124de-664">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="124de-665">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="124de-665">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="124de-666">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="124de-666">Az.Relay</span></span>
* <span data-ttu-id="124de-667">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="124de-667">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="124de-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="124de-668">Az.ServiceBus</span></span>
* <span data-ttu-id="124de-669">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-669">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="124de-670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="124de-670">Az.Storage</span></span>
* <span data-ttu-id="124de-671">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="124de-671">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="124de-672">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="124de-672">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="124de-673">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="124de-673">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="124de-674">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="124de-674">New-AzStorageAccount</span></span>
* <span data-ttu-id="124de-675">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="124de-675">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="124de-676">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="124de-676">New-AzStorageAccount</span></span>
    - <span data-ttu-id="124de-677">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="124de-677">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="124de-678">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="124de-678">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="124de-679">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-679">Az.Websites</span></span>
* <span data-ttu-id="124de-680">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="124de-680">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="124de-681">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="124de-681">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="124de-682">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="124de-682">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="124de-683">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="124de-683">Highlights since the last major release</span></span>
* <span data-ttu-id="124de-684">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="124de-684">General availability of `Az` module</span></span>
* <span data-ttu-id="124de-685">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="124de-685">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="124de-686">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="124de-686">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="124de-687">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-687">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="124de-688">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-688">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="124de-689">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-689">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="124de-690">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="124de-690">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="124de-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-691">Az.Accounts</span></span>
* <span data-ttu-id="124de-692">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-692">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="124de-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="124de-693">Az.Batch</span></span>
* <span data-ttu-id="124de-694">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="124de-695">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="124de-695">Az.Cdn</span></span>
* <span data-ttu-id="124de-696">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="124de-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="124de-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="124de-698">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-699">Az.Compute</span></span>
* <span data-ttu-id="124de-700">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-700">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="124de-701">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="124de-702">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-702">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="124de-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="124de-703">Az.DataFactory</span></span>
* <span data-ttu-id="124de-704">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-704">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="124de-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="124de-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="124de-706">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-706">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="124de-707">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="124de-707">Az.EventGrid</span></span>
* <span data-ttu-id="124de-708">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-708">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="124de-709">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="124de-709">Az.EventHub</span></span>
* <span data-ttu-id="124de-710">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-710">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="124de-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="124de-711">Az.HDInsight</span></span>
* <span data-ttu-id="124de-712">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-712">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="124de-713">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="124de-713">Az.IotHub</span></span>
* <span data-ttu-id="124de-714">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-714">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="124de-715">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="124de-715">Az.KeyVault</span></span>
* <span data-ttu-id="124de-716">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="124de-717">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-717">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="124de-718">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="124de-718">Az.MachineLearning</span></span>
* <span data-ttu-id="124de-719">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-719">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="124de-720">Az.Media</span><span class="sxs-lookup"><span data-stu-id="124de-720">Az.Media</span></span>
* <span data-ttu-id="124de-721">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-721">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="124de-722">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="124de-722">Az.Monitor</span></span>
  * <span data-ttu-id="124de-723">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="124de-723">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="124de-724">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="124de-724">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="124de-725">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="124de-725">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="124de-726">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="124de-726">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="124de-727">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="124de-727">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="124de-728">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="124de-728">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="124de-729">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-729">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-730">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-730">Az.Network</span></span>
* <span data-ttu-id="124de-731">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-731">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="124de-732">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-732">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="124de-733">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="124de-733">Az.NotificationHubs</span></span>
* <span data-ttu-id="124de-734">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-734">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="124de-735">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="124de-735">Az.OperationalInsights</span></span>
* <span data-ttu-id="124de-736">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-736">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="124de-737">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="124de-737">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="124de-738">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-738">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="124de-739">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="124de-739">Az.RecoveryServices</span></span>
* <span data-ttu-id="124de-740">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="124de-741">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="124de-741">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="124de-742">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-742">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="124de-743">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-743">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="124de-744">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="124de-744">Az.RedisCache</span></span>
* <span data-ttu-id="124de-745">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-745">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-746">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-746">Az.Resources</span></span>
* <span data-ttu-id="124de-747">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-747">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-748">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-748">Az.Sql</span></span>
* <span data-ttu-id="124de-749">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-749">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="124de-750">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-750">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="124de-751">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-751">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="124de-752">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-752">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="124de-753">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-753">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="124de-754">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="124de-754">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="124de-755">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-755">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="124de-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-756">Az.Websites</span></span>
* <span data-ttu-id="124de-757">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-757">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="124de-758">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-758">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="124de-759">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-759">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="124de-760">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="124de-760">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="124de-761">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="124de-761">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="124de-762">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="124de-762">Highlights since the last major release</span></span>
* <span data-ttu-id="124de-763">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="124de-763">General availability of `Az` module</span></span>
* <span data-ttu-id="124de-764">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="124de-764">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="124de-765">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="124de-765">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="124de-766">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-766">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="124de-767">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-767">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="124de-768">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-768">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="124de-769">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="124de-769">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="124de-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-770">Az.Accounts</span></span>
* <span data-ttu-id="124de-771">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-771">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="124de-772">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="124de-772">Az.AnalysisServices</span></span>
* <span data-ttu-id="124de-773">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="124de-773">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="124de-774">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="124de-774">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="124de-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="124de-775">Az.Automation</span></span>
* <span data-ttu-id="124de-776">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-776">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="124de-777">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="124de-777">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="124de-778">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="124de-778">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-779">Az.Compute</span></span>
* <span data-ttu-id="124de-780">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-780">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="124de-781">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="124de-781">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="124de-782">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="124de-782">Az.ContainerInstance</span></span>
* <span data-ttu-id="124de-783">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-783">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="124de-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="124de-784">Az.DataFactory</span></span>
* <span data-ttu-id="124de-785">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-785">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="124de-786">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-786">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-787">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-787">Az.Resources</span></span>
* <span data-ttu-id="124de-788">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-788">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="124de-789">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-789">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="124de-790">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="124de-790">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="124de-791">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="124de-791">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="124de-792">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-792">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="124de-793">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="124de-793">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-794">Az.Sql</span></span>
* <span data-ttu-id="124de-795">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="124de-795">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="124de-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="124de-796">Az.Storage</span></span>
* <span data-ttu-id="124de-797">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="124de-797">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="124de-798">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="124de-798">New-AzStorageContext</span></span>
* <span data-ttu-id="124de-799">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="124de-799">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="124de-800">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="124de-800">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="124de-801">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="124de-801">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="124de-802">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="124de-802">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="124de-803">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="124de-803">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="124de-804">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="124de-804">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="124de-805">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="124de-805">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="124de-806">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="124de-806">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="124de-807">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="124de-807">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="124de-808">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="124de-808">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="124de-809">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="124de-809">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="124de-810">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="124de-810">Highlights since the last major release</span></span>
* <span data-ttu-id="124de-811">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="124de-811">General availability of `Az` module</span></span>
* <span data-ttu-id="124de-812">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="124de-812">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="124de-813">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="124de-813">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="124de-814">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-814">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="124de-815">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-815">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="124de-816">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-816">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="124de-817">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="124de-817">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="124de-818">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="124de-818">Az.Automation</span></span>
* <span data-ttu-id="124de-819">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="124de-819">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="124de-820">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="124de-820">Dynamic grouping</span></span>
    * <span data-ttu-id="124de-821">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="124de-821">Pre-Post script</span></span>
    * <span data-ttu-id="124de-822">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="124de-822">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-823">Az.Compute</span></span>
* <span data-ttu-id="124de-824">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="124de-824">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="124de-825">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-825">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="124de-826">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="124de-826">Az.KeyVault</span></span>
* <span data-ttu-id="124de-827">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-827">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-828">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-828">Az.Network</span></span>
* <span data-ttu-id="124de-829">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-829">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="124de-830">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-830">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="124de-831">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="124de-831">Az.RecoveryServices</span></span>
* <span data-ttu-id="124de-832">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-832">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="124de-833">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-833">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-834">Az.Resources</span></span>
* <span data-ttu-id="124de-835">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-835">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="124de-836">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-836">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-837">Az.Sql</span></span>
* <span data-ttu-id="124de-838">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-838">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="124de-839">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="124de-839">Az.Storage</span></span>
* <span data-ttu-id="124de-840">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="124de-840">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="124de-841">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="124de-841">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="124de-842">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="124de-842">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="124de-843">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="124de-843">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="124de-844">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="124de-844">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="124de-845">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="124de-845">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="124de-846">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="124de-846">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="124de-847">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-847">Az.Websites</span></span>
* <span data-ttu-id="124de-848">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-848">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="124de-849">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="124de-849">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="124de-850">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-850">Az.Accounts</span></span>
* <span data-ttu-id="124de-851">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-851">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="124de-852">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-852">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="124de-853">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="124de-853">Az.Automation</span></span>
* <span data-ttu-id="124de-854">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-854">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="124de-855">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-855">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="124de-856">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="124de-856">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="124de-857">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="124de-857">Az.Cdn</span></span>
* <span data-ttu-id="124de-858">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="124de-858">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-859">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-859">Az.Compute</span></span>
* <span data-ttu-id="124de-860">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-860">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="124de-861">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="124de-861">Az.DataFactory</span></span>
* <span data-ttu-id="124de-862">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-862">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="124de-863">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="124de-863">Az.LogicApp</span></span>
* <span data-ttu-id="124de-864">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="124de-864">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-865">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-865">Az.Network</span></span>
* <span data-ttu-id="124de-866">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-866">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="124de-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="124de-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="124de-868">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-868">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="124de-869">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="124de-869">SDK Update</span></span>
* <span data-ttu-id="124de-870">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="124de-870">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="124de-871">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-871">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-872">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-872">Az.Resources</span></span>
* <span data-ttu-id="124de-873">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-873">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="124de-874">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="124de-874">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="124de-875">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-875">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="124de-876">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="124de-876">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="124de-877">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-877">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="124de-878">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="124de-878">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-879">Az.Sql</span></span>
* <span data-ttu-id="124de-880">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="124de-880">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="124de-881">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="124de-881">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="124de-882">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="124de-882">Az.Storage</span></span>
* <span data-ttu-id="124de-883">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="124de-883">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="124de-884">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="124de-884">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="124de-885">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="124de-885">Az.AnalysisServices</span></span>
* <span data-ttu-id="124de-886">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="124de-886">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="124de-887">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="124de-887">Az.Automation</span></span>
* <span data-ttu-id="124de-888">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-888">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="124de-889">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-889">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="124de-890">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-890">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="124de-891">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="124de-891">Az.CognitiveServices</span></span>
* <span data-ttu-id="124de-892">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-892">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-893">Az.Compute</span></span>
* <span data-ttu-id="124de-894">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-894">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="124de-895">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-895">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="124de-896">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-896">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="124de-897">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="124de-897">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="124de-898">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="124de-898">Az.DataLakeStore</span></span>
* <span data-ttu-id="124de-899">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-899">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="124de-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="124de-900">Az.EventHub</span></span>
* <span data-ttu-id="124de-901">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-901">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="124de-902">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="124de-902">Az.KeyVault</span></span>
* <span data-ttu-id="124de-903">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-903">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="124de-904">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="124de-904">Az.LogicApp</span></span>
* <span data-ttu-id="124de-905">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-905">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="124de-906">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-906">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="124de-907">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="124de-907">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="124de-908">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="124de-908">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="124de-909">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="124de-909">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="124de-910">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="124de-910">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="124de-911">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="124de-911">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="124de-912">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="124de-912">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="124de-913">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="124de-913">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="124de-914">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="124de-914">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="124de-915">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="124de-915">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="124de-916">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="124de-916">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="124de-917">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-917">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="124de-918">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="124de-918">Az.Monitor</span></span>
* <span data-ttu-id="124de-919">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-919">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-920">Az.Network</span></span>
* <span data-ttu-id="124de-921">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-921">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="124de-922">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="124de-922">Az.OperationalInsights</span></span>
* <span data-ttu-id="124de-923">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="124de-923">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="124de-924">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-924">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="124de-925">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-925">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="124de-926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-926">Az.Resources</span></span>
* <span data-ttu-id="124de-927">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-927">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="124de-928">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-928">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="124de-929">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-929">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="124de-930">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-930">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-931">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-931">Az.Sql</span></span>
* <span data-ttu-id="124de-932">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-932">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="124de-933">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-933">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="124de-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-934">Az.Websites</span></span>
* <span data-ttu-id="124de-935">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-935">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="124de-936">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="124de-936">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="124de-937">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-937">Az.Accounts</span></span>
* <span data-ttu-id="124de-938">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="124de-938">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="124de-939">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="124de-939">Az.AnalysisServices</span></span>
<span data-ttu-id="124de-940">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="124de-940">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-941">Az.Compute</span></span>
* <span data-ttu-id="124de-942">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-942">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="124de-943">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-943">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="124de-944">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-944">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="124de-945">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="124de-945">Az.RecoveryServices</span></span>
<span data-ttu-id="124de-946">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="124de-946">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-947">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-947">Az.Resources</span></span>
* <span data-ttu-id="124de-948">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-948">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="124de-949">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="124de-949">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="124de-950">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-950">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="124de-951">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="124de-951">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-952">Az.Sql</span></span>
* <span data-ttu-id="124de-953">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="124de-953">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="124de-954">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-954">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="124de-955">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-955">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="124de-956">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="124de-956">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="124de-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-957">Az.Accounts</span></span>
* <span data-ttu-id="124de-958">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="124de-958">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="124de-959">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="124de-959">Az.AnalysisServices</span></span>
* <span data-ttu-id="124de-960">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="124de-960">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="124de-961">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="124de-961">Az.RecoveryServices</span></span>
* <span data-ttu-id="124de-962">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="124de-962">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="124de-963">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="124de-963">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="124de-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-964">Az.Accounts</span></span>
* <span data-ttu-id="124de-965">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-965">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="124de-966">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-966">Update incorrect online help URLs</span></span>
* <span data-ttu-id="124de-967">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-967">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="124de-968">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="124de-968">Az.Aks</span></span>
* <span data-ttu-id="124de-969">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-969">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="124de-970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="124de-970">Az.Automation</span></span>
* <span data-ttu-id="124de-971">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-971">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="124de-972">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-972">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="124de-973">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="124de-973">Az.Cdn</span></span>
* <span data-ttu-id="124de-974">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-974">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-975">Az.Compute</span></span>
* <span data-ttu-id="124de-976">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-976">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="124de-977">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-977">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="124de-978">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-978">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="124de-979">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="124de-979">Az.ContainerRegistry</span></span>
* <span data-ttu-id="124de-980">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-980">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="124de-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="124de-981">Az.DataFactory</span></span>
* <span data-ttu-id="124de-982">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-982">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="124de-983">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="124de-983">Az.DataLakeStore</span></span>
* <span data-ttu-id="124de-984">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-984">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="124de-985">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="124de-985">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="124de-986">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-986">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="124de-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="124de-987">Az.IotHub</span></span>
* <span data-ttu-id="124de-988">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-988">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="124de-989">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="124de-989">Az.KeyVault</span></span>
* <span data-ttu-id="124de-990">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-990">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-991">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-991">Az.Network</span></span>
* <span data-ttu-id="124de-992">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-992">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-993">Az.Resources</span></span>
* <span data-ttu-id="124de-994">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-994">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="124de-995">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-995">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="124de-996">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-996">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="124de-997">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-997">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="124de-998">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-998">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="124de-999">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-999">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="124de-1000">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="124de-1000">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="124de-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="124de-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="124de-1002">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="124de-1002">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="124de-1003">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1003">Fix some error messages.</span></span>
* <span data-ttu-id="124de-1004">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1004">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="124de-1005">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1005">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="124de-1006">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="124de-1006">Az.SignalR</span></span>
* <span data-ttu-id="124de-1007">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1007">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-1008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-1008">Az.Sql</span></span>
* <span data-ttu-id="124de-1009">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1009">Update incorrect online help URLs</span></span>
* <span data-ttu-id="124de-1010">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1010">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="124de-1011">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1011">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="124de-1012">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="124de-1012">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="124de-1013">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="124de-1013">Az.Storage</span></span>
* <span data-ttu-id="124de-1014">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1014">Update incorrect online help URLs</span></span>
* <span data-ttu-id="124de-1015">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="124de-1015">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="124de-1016">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="124de-1016">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="124de-1017">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="124de-1017">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="124de-1018">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="124de-1018">Az.TrafficManager</span></span>
* <span data-ttu-id="124de-1019">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1019">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="124de-1020">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-1020">Az.Websites</span></span>
* <span data-ttu-id="124de-1021">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1021">Update incorrect online help URLs</span></span>
* <span data-ttu-id="124de-1022">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1022">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="124de-1023">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1023">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="124de-1024">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="124de-1024">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="124de-1025">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-1025">Az.Accounts</span></span>
* <span data-ttu-id="124de-1026">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1026">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-1027">Az.Compute</span></span>
* <span data-ttu-id="124de-1028">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="124de-1028">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="124de-1029">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1029">Updated the description of ID in help files</span></span>
* <span data-ttu-id="124de-1030">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="124de-1030">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="124de-1031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="124de-1031">Az.DataLakeStore</span></span>
* <span data-ttu-id="124de-1032">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1032">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="124de-1033">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1033">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="124de-1034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="124de-1034">Az.EventGrid</span></span>
* <span data-ttu-id="124de-1035">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1035">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="124de-1036">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1036">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="124de-1037">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="124de-1037">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="124de-1038">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="124de-1038">Event Time-To-Live,</span></span>
        - <span data-ttu-id="124de-1039">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="124de-1039">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="124de-1040">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="124de-1040">Dead letter endpoint.</span></span>
    - <span data-ttu-id="124de-1041">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="124de-1041">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="124de-1042">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="124de-1042">Event Time-To-Live,</span></span>
        - <span data-ttu-id="124de-1043">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="124de-1043">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="124de-1044">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="124de-1044">Dead letter endpoint.</span></span>
* <span data-ttu-id="124de-1045">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1045">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="124de-1046">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="124de-1046">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="124de-1047">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="124de-1047">Az.IotHub</span></span>
* <span data-ttu-id="124de-1048">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1048">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="124de-1049">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="124de-1049">Az.LogicApp</span></span>
* <span data-ttu-id="124de-1050">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="124de-1050">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-1051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-1051">Az.Resources</span></span>
* <span data-ttu-id="124de-1052">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1052">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="124de-1053">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="124de-1053">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="124de-1054">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1054">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="124de-1055">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1055">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="124de-1056">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1056">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="124de-1057">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="124de-1057">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="124de-1058">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="124de-1058">Az.SignalR</span></span>
* <span data-ttu-id="124de-1059">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="124de-1059">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-1060">Az.Sql</span></span>
* <span data-ttu-id="124de-1061">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="124de-1061">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="124de-1062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="124de-1062">Az.Storage</span></span>
* <span data-ttu-id="124de-1063">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="124de-1063">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="124de-1064">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="124de-1064">New-AzStorageContext</span></span>
* <span data-ttu-id="124de-1065">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1065">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="124de-1066">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="124de-1066">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="124de-1067">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-1067">Az.Websites</span></span>
* <span data-ttu-id="124de-1068">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1068">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="124de-1069">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="124de-1069">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="124de-1070">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="124de-1070">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="124de-1071">Genel</span><span class="sxs-lookup"><span data-stu-id="124de-1071">General</span></span>

- <span data-ttu-id="124de-1072">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="124de-1072">General Availability of Az Module</span></span>
- <span data-ttu-id="124de-1073">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="124de-1073">Online help for each module</span></span>
- <span data-ttu-id="124de-1074">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="124de-1074">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="124de-1075">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1075">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="124de-1076">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="124de-1076">Az.Accounts</span></span>
- <span data-ttu-id="124de-1077">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="124de-1077">Changed from Az.Profile</span></span>
- <span data-ttu-id="124de-1078">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1078">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="124de-1079">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="124de-1079">Az.ApiManagement</span></span>
- <span data-ttu-id="124de-1080">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="124de-1080">Fixes for #7002</span></span>
- <span data-ttu-id="124de-1081">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="124de-1082">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="124de-1082">Az.Batch</span></span>
- <span data-ttu-id="124de-1083">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1083">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="124de-1084">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="124de-1084">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="124de-1085">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="124de-1086">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="124de-1086">Az.Billing</span></span>
- <span data-ttu-id="124de-1087">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1087">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="124de-1088">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="124de-1088">Az.CognitivServices</span></span>
- <span data-ttu-id="124de-1089">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1089">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="124de-1090">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="124de-1090">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="124de-1091">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="124de-1091">Az.ContainerInstance</span></span>
- <span data-ttu-id="124de-1092">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1092">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="124de-1093">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="124de-1093">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="124de-1094">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1094">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="124de-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="124de-1095">Az.DataLakeStore</span></span>
- <span data-ttu-id="124de-1096">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1096">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="124de-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="124de-1097">Az.Monitor</span></span>
- <span data-ttu-id="124de-1098">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1098">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="124de-1099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="124de-1099">Az.KeyVault</span></span>
- <span data-ttu-id="124de-1100">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="124de-1100">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="124de-1101">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="124de-1101">Az.MachineLearning</span></span>
- <span data-ttu-id="124de-1102">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1102">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="124de-1103">Az.Media</span><span class="sxs-lookup"><span data-stu-id="124de-1103">Az.Media</span></span>
- <span data-ttu-id="124de-1104">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="124de-1104">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="124de-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-1105">Az.Network</span></span>
<span data-ttu-id="124de-1106">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1106">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="124de-1107">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="124de-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="124de-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="124de-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="124de-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="124de-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="124de-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="124de-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="124de-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="124de-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="124de-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="124de-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="124de-1113">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="124de-1113">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="124de-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="124de-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="124de-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="124de-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="124de-1116">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1116">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="124de-1117">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="124de-1117">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="124de-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="124de-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="124de-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="124de-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="124de-1120">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="124de-1120">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="124de-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="124de-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="124de-1122">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="124de-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="124de-1123">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1123">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="124de-1124">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="124de-1124">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="124de-1125">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="124de-1125">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="124de-1126">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="124de-1126">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="124de-1127">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1127">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="124de-1128">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1128">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="124de-1129">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="124de-1129">Az.OperationalInsights</span></span>
- <span data-ttu-id="124de-1130">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1130">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="124de-1131">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="124de-1131">Az.Profile</span></span>
- <span data-ttu-id="124de-1132">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1132">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="124de-1133">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="124de-1133">Az.RecoveryServices</span></span>
- <span data-ttu-id="124de-1134">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="124de-1135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-1135">Az.Resources</span></span>
- <span data-ttu-id="124de-1136">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1136">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="124de-1137">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="124de-1137">Az.ServiceFabric</span></span>
- <span data-ttu-id="124de-1138">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="124de-1138">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="124de-1139">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1139">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="124de-1140">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="124de-1140">Az.SIgnalR</span></span>
- <span data-ttu-id="124de-1141">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="124de-1141">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="124de-1142">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-1142">Az.Sql</span></span>
- <span data-ttu-id="124de-1143">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1143">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="124de-1144">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1144">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="124de-1145">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1145">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="124de-1146">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="124de-1146">Az.Storage</span></span>
- <span data-ttu-id="124de-1147">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="124de-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-1148">Az.Websites</span></span>
- <span data-ttu-id="124de-1149">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="124de-1149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="124de-1150">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="124de-1150">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="124de-1151">Genel</span><span class="sxs-lookup"><span data-stu-id="124de-1151">General</span></span>

* <span data-ttu-id="124de-1152">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="124de-1152">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="124de-1153">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-1153">Az.Compute</span></span>

* <span data-ttu-id="124de-1154">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1154">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="124de-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="124de-1155">Az.DataLakeStore</span></span>

* <span data-ttu-id="124de-1156">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1156">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="124de-1157">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="124de-1157">Az.FrontDoor</span></span>

* <span data-ttu-id="124de-1158">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1158">Fixed some broken links</span></span>
    - <span data-ttu-id="124de-1159">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1159">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="124de-1160">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1160">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="124de-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="124de-1161">Az.RecoveryServices</span></span>

* <span data-ttu-id="124de-1162">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1162">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="124de-1163">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1163">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="124de-1164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-1164">Az.Resources</span></span>

* <span data-ttu-id="124de-1165">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="124de-1165">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="124de-1166">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1166">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="124de-1167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-1167">Az.Sql</span></span>

* <span data-ttu-id="124de-1168">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="124de-1168">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="124de-1169">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1169">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="124de-1170">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1170">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="124de-1171">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="124de-1171">Az.Storage</span></span>

* <span data-ttu-id="124de-1172">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1172">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="124de-1173">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1173">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="124de-1174">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="124de-1174">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="124de-1175">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1175">Support Static Website configuration</span></span>
    - <span data-ttu-id="124de-1176">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="124de-1176">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="124de-1177">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="124de-1177">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="124de-1178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-1178">Az.Websites</span></span>

* <span data-ttu-id="124de-1179">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="124de-1179">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="124de-1180">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1180">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="124de-1181">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="124de-1181">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="124de-1182">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="124de-1182">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="124de-1183">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="124de-1183">Az.ApiManagement</span></span>
* <span data-ttu-id="124de-1184">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="124de-1184">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="124de-1185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="124de-1185">Az.Automation</span></span>
* <span data-ttu-id="124de-1186">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="124de-1186">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="124de-1187">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1187">Added Update Management cmdlets</span></span>
* <span data-ttu-id="124de-1188">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1188">Added Source Control cmdlets</span></span>
* <span data-ttu-id="124de-1189">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1189">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="124de-1190">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1190">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="124de-1191">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-1191">Az.Compute</span></span>
* <span data-ttu-id="124de-1192">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1192">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="124de-1193">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="124de-1193">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="124de-1194">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="124de-1194">Az.ContainerInstance</span></span>
* <span data-ttu-id="124de-1195">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="124de-1195">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="124de-1196">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="124de-1196">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="124de-1197">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1197">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="124de-1198">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-1198">Az.Network</span></span>
* <span data-ttu-id="124de-1199">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1199">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="124de-1200">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1200">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="124de-1201">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1201">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="124de-1202">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1202">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="124de-1203">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="124de-1203">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="124de-1204">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1204">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="124de-1205">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="124de-1205">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="124de-1206">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="124de-1206">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="124de-1207">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1207">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="124de-1208">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="124de-1208">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="124de-1209">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="124de-1209">Az.Relay</span></span>
* <span data-ttu-id="124de-1210">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1210">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="124de-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-1211">Az.Resources</span></span>
* <span data-ttu-id="124de-1212">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1212">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="124de-1213">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1213">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="124de-1214">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="124de-1214">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="124de-1215">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="124de-1215">Az.ServiceFabric</span></span>
* <span data-ttu-id="124de-1216">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1216">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="124de-1217">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-1217">Az.Sql</span></span>
* <span data-ttu-id="124de-1218">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1218">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="124de-1219">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="124de-1219">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="124de-1220">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="124de-1220">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="124de-1221">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="124de-1221">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="124de-1222">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="124de-1222">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="124de-1223">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="124de-1223">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="124de-1224">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="124de-1224">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="124de-1225">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="124de-1225">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="124de-1226">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="124de-1226">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="124de-1227">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1227">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="124de-1228">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1228">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="124de-1229">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1229">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="124de-1230">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="124de-1230">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="124de-1231">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="124de-1231">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="124de-1232">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="124de-1232">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="124de-1233">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="124de-1233">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="124de-1234">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1234">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="124de-1235">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="124de-1235">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="124de-1236">Genel</span><span class="sxs-lookup"><span data-stu-id="124de-1236">General</span></span>
* <span data-ttu-id="124de-1237">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="124de-1237">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="124de-1238">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="124de-1238">Az.Profile</span></span>
* <span data-ttu-id="124de-1239">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1239">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="124de-1240">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1240">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="124de-1241">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1241">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="124de-1242">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1242">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="124de-1243">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1243">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="124de-1244">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1244">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="124de-1245">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1245">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="124de-1246">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="124de-1246">Az.CognitiveServices</span></span>
* <span data-ttu-id="124de-1247">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1247">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-1248">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-1248">Az.Compute</span></span>
* <span data-ttu-id="124de-1249">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1249">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="124de-1250">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="124de-1250">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="124de-1251">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1251">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="124de-1252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="124de-1252">Az.DataLakeStore</span></span>
* <span data-ttu-id="124de-1253">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1253">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="124de-1254">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1254">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="124de-1255">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="124de-1255">Az.Insights</span></span>
* <span data-ttu-id="124de-1256">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1256">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="124de-1257">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="124de-1257">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="124de-1258">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1258">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="124de-1259">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="124de-1259">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-1260">Az.Network</span></span>
* <span data-ttu-id="124de-1261">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="124de-1261">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="124de-1262">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="124de-1262">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="124de-1263">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="124de-1263">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="124de-1264">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="124de-1264">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="124de-1265">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="124de-1265">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="124de-1266">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="124de-1266">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="124de-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="124de-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="124de-1268">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="124de-1268">Az.PolicyInsights</span></span>
* <span data-ttu-id="124de-1269">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1269">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-1270">Az.Resources</span></span>
* <span data-ttu-id="124de-1271">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="124de-1271">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="124de-1272">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="124de-1272">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="124de-1273">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="124de-1273">Az.ServiceBus</span></span>
* <span data-ttu-id="124de-1274">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1274">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="124de-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="124de-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="124de-1276">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1276">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="124de-1277">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1277">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="124de-1278">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="124de-1278">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="124de-1279">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="124de-1279">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="124de-1280">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1280">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="124de-1281">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="124de-1281">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="124de-1282">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="124de-1282">Az.Profile</span></span>
* <span data-ttu-id="124de-1283">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="124de-1283">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="124de-1284">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="124de-1284">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-1285">Az.Compute</span></span>
* <span data-ttu-id="124de-1286">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1286">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="124de-1287">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1287">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="124de-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="124de-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="124de-1289">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="124de-1289">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="124de-1290">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="124de-1290">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="124de-1291">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="124de-1291">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="124de-1292">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="124de-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="124de-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="124de-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-1294">Az.Network</span></span>
* <span data-ttu-id="124de-1295">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="124de-1295">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="124de-1296">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1296">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-1297">Az.Resources</span></span>
* <span data-ttu-id="124de-1298">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1298">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="124de-1299">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="124de-1299">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="124de-1300">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="124de-1300">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="124de-1301">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="124de-1301">Azure.Storage</span></span>
* <span data-ttu-id="124de-1302">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="124de-1302">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="124de-1303">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="124de-1303">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="124de-1304">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="124de-1304">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="124de-1305">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="124de-1305">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="124de-1306">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="124de-1306">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="124de-1307">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="124de-1307">Az.CognitiveServices</span></span>
* <span data-ttu-id="124de-1308">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="124de-1308">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="124de-1309">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="124de-1309">Az.Compute</span></span>
* <span data-ttu-id="124de-1310">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1310">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="124de-1311">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1311">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="124de-1312">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1312">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="124de-1313">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="124de-1313">Az.DataFactoryV2</span></span>
* <span data-ttu-id="124de-1314">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="124de-1314">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="124de-1315">Az.Network</span><span class="sxs-lookup"><span data-stu-id="124de-1315">Az.Network</span></span>
* <span data-ttu-id="124de-1316">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="124de-1316">Added NetworkProfile functionality.</span></span> <span data-ttu-id="124de-1317">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1317">new cmdlets added</span></span>
    - <span data-ttu-id="124de-1318">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="124de-1318">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="124de-1319">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="124de-1319">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="124de-1320">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="124de-1320">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="124de-1321">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="124de-1321">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="124de-1322">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="124de-1322">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="124de-1323">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="124de-1323">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="124de-1324">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1324">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="124de-1325">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1325">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="124de-1326">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1326">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="124de-1327">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="124de-1327">Az.RedisCache</span></span>
* <span data-ttu-id="124de-1328">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="124de-1328">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="124de-1329">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1329">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="124de-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="124de-1330">Az.Resources</span></span>
* <span data-ttu-id="124de-1331">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="124de-1331">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="124de-1332">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1332">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="124de-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="124de-1333">Az.Sql</span></span>
* <span data-ttu-id="124de-1334">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="124de-1334">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="124de-1335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="124de-1335">Az.Websites</span></span>
* <span data-ttu-id="124de-1336">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="124de-1336">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="124de-1337">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="124de-1337">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="124de-1338">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="124de-1338">0.2.0 - September 2018</span></span>
 <span data-ttu-id="124de-1339">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="124de-1339">Initial Release</span></span>