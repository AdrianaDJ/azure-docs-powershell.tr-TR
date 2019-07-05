---
ms.openlocfilehash: ac8513b3eee4adfcaf0be8bf7b4e8d09190811df
ms.sourcegitcommit: a4e527d3deba004007cfa22fa536e8255dd23b37
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67516649"
---
## <a name="240---july-2019"></a><span data-ttu-id="7b924-101">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-101">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7b924-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7b924-102">Az.Accounts</span></span>
* <span data-ttu-id="7b924-103">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-103">Add support for profile cmdlets</span></span>
* <span data-ttu-id="7b924-104">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-104">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="7b924-105">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-105">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7b924-106">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7b924-106">Az.Advisor</span></span>
* <span data-ttu-id="7b924-107">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7b924-107">GA release of Az.Advisor</span></span>
* <span data-ttu-id="7b924-108">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="7b924-108">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7b924-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7b924-109">Az.ApiManagement</span></span>
* <span data-ttu-id="7b924-110">https://github.com/Azure/azure-powershell/issues/8671 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-110">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="7b924-111">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7b924-111">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="7b924-112">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-112">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="7b924-113">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="7b924-113">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="7b924-114">https://github.com/Azure/azure-powershell/issues/9307 ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="7b924-114">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="7b924-115">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7b924-115">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="7b924-116">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-116">Added support for specifiying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7b924-117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7b924-117">Az.Automation</span></span>
* <span data-ttu-id="7b924-118">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-118">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-119">Az.Compute</span></span>
* <span data-ttu-id="7b924-120">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-120">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7b924-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7b924-121">Az.DataFactory</span></span>
* <span data-ttu-id="7b924-122">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="7b924-122">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7b924-123">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7b924-123">Az.EventGrid</span></span>
* <span data-ttu-id="7b924-124">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-124">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7b924-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7b924-125">Az.IotHub</span></span>
* <span data-ttu-id="7b924-126">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-126">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-127">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-127">Az.Network</span></span>
* <span data-ttu-id="7b924-128">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-128">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="7b924-129">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-129">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7b924-130">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7b924-130">Az.PolicyInsights</span></span>
* <span data-ttu-id="7b924-131">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-131">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="7b924-132">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="7b924-132">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7b924-133">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7b924-133">Az.OperationalInsights</span></span>
* <span data-ttu-id="7b924-134">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-134">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7b924-135">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7b924-135">Az.RecoveryServices</span></span>
* <span data-ttu-id="7b924-136">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7b924-136">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-137">Az.Resources</span></span>
    - <span data-ttu-id="7b924-138">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7b924-138">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="7b924-139">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-139">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="7b924-140">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-140">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="7b924-141">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-141">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7b924-142">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7b924-142">Az.ServiceBus</span></span>
* <span data-ttu-id="7b924-143">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-143">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-144">Az.Sql</span></span>
* <span data-ttu-id="7b924-145">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-145">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="7b924-146">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="7b924-146">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="7b924-147">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7b924-147">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7b924-148">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7b924-148">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7b924-149">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7b924-149">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7b924-150">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7b924-150">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7b924-151">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7b924-151">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7b924-152">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7b924-152">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="7b924-153">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7b924-153">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7b924-154">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7b924-154">Az.Storage</span></span>
* <span data-ttu-id="7b924-155">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="7b924-155">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="7b924-156">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7b924-156">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="7b924-157">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-157">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="7b924-158">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="7b924-158">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="7b924-159">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-159">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="7b924-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b924-160">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7b924-161">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b924-161">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7b924-162">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-162">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="7b924-163">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7b924-163">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="7b924-164">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7b924-164">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7b924-165">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7b924-165">Az.StorageSync</span></span>
* <span data-ttu-id="7b924-166">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="7b924-166">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="7b924-167">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-167">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7b924-168">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7b924-168">Az.Accounts</span></span>
* <span data-ttu-id="7b924-169">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-169">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="7b924-170">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="7b924-170">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="7b924-171">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-171">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="7b924-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7b924-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="7b924-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="7b924-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-174">Az.Compute</span></span>
* <span data-ttu-id="7b924-175">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="7b924-175">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="7b924-176">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-176">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="7b924-177">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7b924-177">Az.Dns</span></span>
* <span data-ttu-id="7b924-178">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-178">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7b924-179">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7b924-179">Az.EventGrid</span></span>
* <span data-ttu-id="7b924-180">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-180">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="7b924-181">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="7b924-181">New cmdlets:</span></span>
    - <span data-ttu-id="7b924-182">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7b924-182">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7b924-183">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b924-183">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7b924-184">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7b924-184">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7b924-185">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="7b924-185">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="7b924-186">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7b924-186">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7b924-187">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7b924-187">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7b924-188">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7b924-188">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7b924-189">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="7b924-189">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7b924-190">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7b924-190">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7b924-191">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="7b924-191">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="7b924-192">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7b924-192">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7b924-193">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b924-193">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="7b924-194">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7b924-194">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="7b924-195">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="7b924-195">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="7b924-196">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7b924-196">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7b924-197">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7b924-197">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="7b924-198">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7b924-198">Updated cmdlets:</span></span>
    - <span data-ttu-id="7b924-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7b924-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="7b924-200">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="7b924-200">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7b924-201">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="7b924-201">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7b924-202">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="7b924-202">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="7b924-203">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7b924-203">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="7b924-204">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="7b924-204">Event subscription expiration date,</span></span>
            - <span data-ttu-id="7b924-205">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="7b924-205">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="7b924-206">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="7b924-206">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="7b924-207">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="7b924-207">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="7b924-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7b924-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="7b924-209">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="7b924-209">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="7b924-210">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7b924-210">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="7b924-211">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="7b924-211">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="7b924-212">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="7b924-212">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7b924-213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7b924-213">Az.FrontDoor</span></span>
* <span data-ttu-id="7b924-214">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="7b924-214">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="7b924-215">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="7b924-215">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="7b924-216">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="7b924-216">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="7b924-217">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="7b924-217">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-218">Az.Network</span></span>
* <span data-ttu-id="7b924-219">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="7b924-219">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="7b924-220">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7b924-220">New cmdlets</span></span>
        - <span data-ttu-id="7b924-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7b924-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="7b924-222">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="7b924-222">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="7b924-223">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7b924-223">New cmdlets</span></span> 
        - <span data-ttu-id="7b924-224">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7b924-224">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="7b924-225">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="7b924-225">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="7b924-226">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7b924-226">New cmdlets</span></span> 
        - <span data-ttu-id="7b924-227">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7b924-227">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="7b924-228">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7b924-228">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7b924-229">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7b924-229">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7b924-230">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7b924-230">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="7b924-231">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7b924-231">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7b924-232">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="7b924-232">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="7b924-233">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7b924-233">New cmdlets</span></span>
        - <span data-ttu-id="7b924-234">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b924-234">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7b924-235">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b924-235">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7b924-236">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b924-236">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7b924-237">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="7b924-237">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="7b924-238">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="7b924-238">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="7b924-239">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-239">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="7b924-240">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-240">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="7b924-241">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-241">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="7b924-242">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-242">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="7b924-243">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-243">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="7b924-244">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-244">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="7b924-245">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-245">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="7b924-246">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-246">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="7b924-247">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-247">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="7b924-248">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-248">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="7b924-249">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-249">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="7b924-250">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-250">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="7b924-251">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-251">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="7b924-252">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7b924-252">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7b924-253">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-253">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="7b924-254">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-254">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="7b924-255">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7b924-255">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="7b924-256">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7b924-256">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="7b924-257">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="7b924-257">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="7b924-258">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-258">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7b924-259">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-259">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7b924-260">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-260">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7b924-261">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7b924-261">Az.OperationalInsights</span></span>
* <span data-ttu-id="7b924-262">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-262">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-263">Az.Resources</span></span>
* <span data-ttu-id="7b924-264">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="7b924-264">Support for additional Template Export options</span></span>
    - <span data-ttu-id="7b924-265">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-265">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7b924-266">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-266">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7b924-267">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-267">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7b924-268">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7b924-268">Az.ServiceFabric</span></span>
* <span data-ttu-id="7b924-269">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-269">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-270">Az.Sql</span></span>
* <span data-ttu-id="7b924-271">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-271">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="7b924-272">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-272">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="7b924-273">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7b924-273">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="7b924-274">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7b924-274">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7b924-275">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7b924-275">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7b924-276">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7b924-276">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7b924-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7b924-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="7b924-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7b924-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7b924-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7b924-279">Az.Storage</span></span>
* <span data-ttu-id="7b924-280">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="7b924-280">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="7b924-281">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b924-281">New-AzStorageAccount</span></span>
* <span data-ttu-id="7b924-282">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-282">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="7b924-283">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7b924-283">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7b924-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7b924-284">Az.Websites</span></span>
* <span data-ttu-id="7b924-285">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="7b924-285">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="7b924-286">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="7b924-286">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="7b924-287">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-287">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="7b924-288">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7b924-288">Az.Cdn</span></span>
* <span data-ttu-id="7b924-289">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-289">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-290">Az.Compute</span></span>
* <span data-ttu-id="7b924-291">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-291">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="7b924-292">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7b924-292">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7b924-293">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7b924-293">Az.EventHub</span></span>
* <span data-ttu-id="7b924-294">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7b924-294">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="7b924-295">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7b924-295">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-296">Az.Network</span></span>
* <span data-ttu-id="7b924-297">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-297">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="7b924-298">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-298">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7b924-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7b924-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="7b924-300">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-300">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7b924-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7b924-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="7b924-302">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-302">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7b924-303">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7b924-303">Az.ServiceBus</span></span>
* <span data-ttu-id="7b924-304">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7b924-304">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7b924-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7b924-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="7b924-306">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-306">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="7b924-307">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-307">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-308">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-308">Az.Sql</span></span>
* <span data-ttu-id="7b924-309">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-309">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="7b924-310">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="7b924-310">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7b924-311">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="7b924-311">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="7b924-312">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="7b924-312">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7b924-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7b924-313">Az.Websites</span></span>
* <span data-ttu-id="7b924-314">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="7b924-314">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="7b924-315">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-315">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7b924-316">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7b924-316">Az.ApiManagement</span></span>
* <span data-ttu-id="7b924-317">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7b924-317">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="7b924-318">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="7b924-318">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="7b924-319">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="7b924-319">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="7b924-320">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="7b924-320">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="7b924-321">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b924-321">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="7b924-322">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="7b924-322">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="7b924-323">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="7b924-323">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="7b924-324">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7b924-324">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="7b924-325">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7b924-325">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="7b924-326">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="7b924-326">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="7b924-327">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="7b924-327">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="7b924-328">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="7b924-328">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="7b924-329">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7b924-329">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="7b924-330">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7b924-330">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="7b924-331">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="7b924-331">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="7b924-332">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="7b924-332">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="7b924-333">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="7b924-333">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="7b924-334">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7b924-334">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="7b924-335">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="7b924-335">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="7b924-336">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="7b924-336">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="7b924-337">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7b924-337">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="7b924-338">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7b924-338">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="7b924-339">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="7b924-339">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="7b924-340">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-340">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="7b924-341">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-341">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="7b924-342">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-342">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="7b924-343">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7b924-343">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="7b924-344">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7b924-344">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="7b924-345">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-345">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="7b924-346">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-346">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="7b924-347">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-347">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="7b924-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="7b924-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="7b924-349">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-349">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="7b924-350">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-350">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7b924-351">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="7b924-351">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="7b924-352">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="7b924-352">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="7b924-353">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="7b924-353">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="7b924-354">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-354">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="7b924-355">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-355">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="7b924-356">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-356">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="7b924-357">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="7b924-357">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7b924-358">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="7b924-358">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7b924-359">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="7b924-359">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="7b924-360">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="7b924-360">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7b924-361">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-361">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7b924-362">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="7b924-362">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7b924-363">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="7b924-363">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="7b924-364">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="7b924-364">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7b924-365">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-365">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="7b924-366">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="7b924-366">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="7b924-367">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="7b924-367">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="7b924-368">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="7b924-368">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="7b924-369">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="7b924-369">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="7b924-370">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-370">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="7b924-371">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="7b924-371">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="7b924-372">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="7b924-372">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="7b924-373">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-373">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7b924-374">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="7b924-374">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7b924-375">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="7b924-375">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7b924-376">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-376">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7b924-377">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-377">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7b924-378">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="7b924-378">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7b924-379">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="7b924-379">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7b924-380">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-380">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7b924-381">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-381">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="7b924-382">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="7b924-382">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="7b924-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="7b924-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="7b924-384">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="7b924-384">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="7b924-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="7b924-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="7b924-386">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7b924-386">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="7b924-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="7b924-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="7b924-388">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="7b924-388">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="7b924-389">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="7b924-389">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="7b924-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="7b924-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="7b924-391">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="7b924-391">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="7b924-392">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7b924-392">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="7b924-393">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="7b924-393">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7b924-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7b924-394">Az.Automation</span></span>
* <span data-ttu-id="7b924-395">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-395">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="7b924-396">https://github.com/Azure/azure-powershell/issues/7977 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-396">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="7b924-397">https://github.com/Azure/azure-powershell/issues/8600 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-397">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="7b924-398">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-398">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="7b924-399">https://github.com/Azure/azure-powershell/issues/8347 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-399">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="7b924-400">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-400">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="7b924-401">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="7b924-401">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-402">Az.Compute</span></span>
* <span data-ttu-id="7b924-403">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-403">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="7b924-404">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="7b924-404">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7b924-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7b924-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="7b924-406">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-406">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7b924-407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7b924-407">Az.Monitor</span></span>
* <span data-ttu-id="7b924-408">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-408">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-409">Az.Network</span></span>
* <span data-ttu-id="7b924-410">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-410">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="7b924-411">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7b924-411">Updated cmdlet:</span></span>
        - <span data-ttu-id="7b924-412">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7b924-412">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="7b924-413">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-413">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-414">Az.Resources</span></span>
* <span data-ttu-id="7b924-415">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-415">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-416">Az.Sql</span></span>
* <span data-ttu-id="7b924-417">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="7b924-417">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="7b924-418">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-418">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7b924-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7b924-419">Az.Accounts</span></span>
* <span data-ttu-id="7b924-420">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="7b924-420">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7b924-421">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7b924-421">Az.CognitiveServices</span></span>
* <span data-ttu-id="7b924-422">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="7b924-422">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="7b924-423">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="7b924-423">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-424">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-424">Az.Compute</span></span>
* <span data-ttu-id="7b924-425">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="7b924-425">Proximity placement group feature.</span></span>
    - <span data-ttu-id="7b924-426">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7b924-426">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="7b924-427">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7b924-427">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="7b924-428">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-428">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="7b924-429">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="7b924-429">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="7b924-430">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-430">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="7b924-431">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="7b924-431">Breaking changes</span></span>
    - <span data-ttu-id="7b924-432">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-432">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="7b924-433">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-433">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7b924-434">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7b924-434">Az.DeploymentManager</span></span>
* <span data-ttu-id="7b924-435">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="7b924-435">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="7b924-436">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7b924-436">Az.Dns</span></span>
* <span data-ttu-id="7b924-437">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="7b924-437">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="7b924-438">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="7b924-438">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="7b924-439">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="7b924-439">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7b924-440">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7b924-440">Az.FrontDoor</span></span>
* <span data-ttu-id="7b924-441">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="7b924-441">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="7b924-442">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="7b924-442">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="7b924-443">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7b924-443">Az.HDInsight</span></span>
* <span data-ttu-id="7b924-444">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="7b924-444">Removed two cmdlets:</span></span>
    - <span data-ttu-id="7b924-445">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7b924-445">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="7b924-446">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7b924-446">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7b924-447">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-447">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7b924-448">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="7b924-448">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="7b924-449">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="7b924-449">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="7b924-450">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="7b924-450">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7b924-451">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7b924-451">Az.Monitor</span></span>
* <span data-ttu-id="7b924-452">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="7b924-452">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="7b924-453">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7b924-453">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="7b924-454">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="7b924-454">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="7b924-455">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7b924-455">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="7b924-456">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="7b924-456">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="7b924-457">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="7b924-457">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="7b924-458">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="7b924-458">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="7b924-459">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7b924-459">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7b924-460">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7b924-460">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7b924-461">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7b924-461">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7b924-462">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7b924-462">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7b924-463">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7b924-463">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7b924-464">SQR API hakkında [daha fazla](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="7b924-464">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="7b924-465">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-465">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-466">Az.Network</span></span>
* <span data-ttu-id="7b924-467">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="7b924-467">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="7b924-468">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7b924-468">New cmdlets</span></span>
        - <span data-ttu-id="7b924-469">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7b924-469">New-AzNatGateway</span></span>
        - <span data-ttu-id="7b924-470">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7b924-470">Get-AzNatGateway</span></span>
        - <span data-ttu-id="7b924-471">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7b924-471">Set-AzNatGateway</span></span>
        - <span data-ttu-id="7b924-472">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7b924-472">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="7b924-473">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-473">Updated cmdlets</span></span>
        - <span data-ttu-id="7b924-474">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7b924-474">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="7b924-475">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7b924-475">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="7b924-476">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="7b924-476">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="7b924-477">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-477">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="7b924-478">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-478">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7b924-479">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7b924-479">Az.PolicyInsights</span></span>
* <span data-ttu-id="7b924-480">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="7b924-480">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="7b924-481">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7b924-481">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="7b924-482">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="7b924-482">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7b924-483">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7b924-483">Az.RecoveryServices</span></span>
* <span data-ttu-id="7b924-484">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="7b924-484">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="7b924-485">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="7b924-485">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="7b924-486">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="7b924-486">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="7b924-487">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="7b924-487">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="7b924-488">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="7b924-488">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="7b924-489">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="7b924-489">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="7b924-490">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7b924-490">Az.Relay</span></span>
* <span data-ttu-id="7b924-491">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="7b924-491">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7b924-492">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7b924-492">Az.ServiceBus</span></span>
* <span data-ttu-id="7b924-493">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-493">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7b924-494">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7b924-494">Az.Storage</span></span>
* <span data-ttu-id="7b924-495">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="7b924-495">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="7b924-496">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="7b924-496">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="7b924-497">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="7b924-497">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="7b924-498">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b924-498">New-AzStorageAccount</span></span>
* <span data-ttu-id="7b924-499">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="7b924-499">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="7b924-500">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b924-500">New-AzStorageAccount</span></span>
    - <span data-ttu-id="7b924-501">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b924-501">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="7b924-502">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b924-502">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7b924-503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7b924-503">Az.Websites</span></span>
* <span data-ttu-id="7b924-504">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="7b924-504">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="7b924-505">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="7b924-505">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="7b924-506">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-506">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7b924-507">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7b924-507">Highlights since the last major release</span></span>
* <span data-ttu-id="7b924-508">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7b924-508">General availability of `Az` module</span></span>
* <span data-ttu-id="7b924-509">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7b924-509">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7b924-510">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7b924-510">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7b924-511">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-511">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7b924-512">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-512">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7b924-513">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-513">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7b924-514">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7b924-514">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7b924-515">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7b924-515">Az.Accounts</span></span>
* <span data-ttu-id="7b924-516">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-516">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7b924-517">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7b924-517">Az.Batch</span></span>
* <span data-ttu-id="7b924-518">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-518">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7b924-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7b924-519">Az.Cdn</span></span>
* <span data-ttu-id="7b924-520">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7b924-521">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7b924-521">Az.CognitiveServices</span></span>
* <span data-ttu-id="7b924-522">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-522">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-523">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-523">Az.Compute</span></span>
* <span data-ttu-id="7b924-524">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-524">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7b924-525">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7b924-526">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-526">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7b924-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7b924-527">Az.DataFactory</span></span>
* <span data-ttu-id="7b924-528">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-528">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7b924-529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7b924-529">Az.DataLakeStore</span></span>
* <span data-ttu-id="7b924-530">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-530">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7b924-531">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7b924-531">Az.EventGrid</span></span>
* <span data-ttu-id="7b924-532">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-532">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7b924-533">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7b924-533">Az.EventHub</span></span>
* <span data-ttu-id="7b924-534">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-534">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="7b924-535">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7b924-535">Az.HDInsight</span></span>
* <span data-ttu-id="7b924-536">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-536">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7b924-537">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7b924-537">Az.IotHub</span></span>
* <span data-ttu-id="7b924-538">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-538">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7b924-539">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7b924-539">Az.KeyVault</span></span>
* <span data-ttu-id="7b924-540">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-540">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7b924-541">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-541">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7b924-542">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7b924-542">Az.MachineLearning</span></span>
* <span data-ttu-id="7b924-543">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7b924-544">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7b924-544">Az.Media</span></span>
* <span data-ttu-id="7b924-545">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7b924-546">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7b924-546">Az.Monitor</span></span>
  * <span data-ttu-id="7b924-547">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="7b924-547">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7b924-548">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7b924-548">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7b924-549">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7b924-549">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7b924-550">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7b924-550">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7b924-551">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7b924-551">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7b924-552">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7b924-552">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7b924-553">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-553">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-554">Az.Network</span></span>
* <span data-ttu-id="7b924-555">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-555">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7b924-556">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-556">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7b924-557">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7b924-557">Az.NotificationHubs</span></span>
* <span data-ttu-id="7b924-558">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-558">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7b924-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7b924-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="7b924-560">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-560">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7b924-561">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7b924-561">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7b924-562">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7b924-563">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7b924-563">Az.RecoveryServices</span></span>
* <span data-ttu-id="7b924-564">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-564">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7b924-565">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="7b924-565">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7b924-566">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-566">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7b924-567">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-567">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7b924-568">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7b924-568">Az.RedisCache</span></span>
* <span data-ttu-id="7b924-569">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-570">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-570">Az.Resources</span></span>
* <span data-ttu-id="7b924-571">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-571">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-572">Az.Sql</span></span>
* <span data-ttu-id="7b924-573">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-573">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7b924-574">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7b924-575">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-575">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7b924-576">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-576">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7b924-577">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-577">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7b924-578">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="7b924-578">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7b924-579">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-579">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7b924-580">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7b924-580">Az.Websites</span></span>
* <span data-ttu-id="7b924-581">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-581">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7b924-582">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-582">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7b924-583">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-583">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7b924-584">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7b924-584">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7b924-585">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-585">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7b924-586">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7b924-586">Highlights since the last major release</span></span>
* <span data-ttu-id="7b924-587">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7b924-587">General availability of `Az` module</span></span>
* <span data-ttu-id="7b924-588">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7b924-588">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7b924-589">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7b924-589">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7b924-590">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-590">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7b924-591">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-591">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7b924-592">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-592">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7b924-593">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7b924-593">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7b924-594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7b924-594">Az.Accounts</span></span>
* <span data-ttu-id="7b924-595">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-595">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7b924-596">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7b924-596">Az.AnalysisServices</span></span>
* <span data-ttu-id="7b924-597">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7b924-597">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7b924-598">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="7b924-598">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7b924-599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7b924-599">Az.Automation</span></span>
* <span data-ttu-id="7b924-600">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-600">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7b924-601">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="7b924-601">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7b924-602">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7b924-602">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-603">Az.Compute</span></span>
* <span data-ttu-id="7b924-604">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-604">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7b924-605">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-605">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="7b924-606">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7b924-606">Az.ContainerInstance</span></span>
* <span data-ttu-id="7b924-607">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-607">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7b924-608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7b924-608">Az.DataFactory</span></span>
* <span data-ttu-id="7b924-609">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-609">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7b924-610">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-610">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-611">Az.Resources</span></span>
* <span data-ttu-id="7b924-612">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-612">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7b924-613">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-613">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7b924-614">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="7b924-614">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7b924-615">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7b924-615">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7b924-616">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-616">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7b924-617">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7b924-617">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-618">Az.Sql</span></span>
* <span data-ttu-id="7b924-619">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="7b924-619">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7b924-620">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7b924-620">Az.Storage</span></span>
* <span data-ttu-id="7b924-621">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="7b924-621">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7b924-622">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7b924-622">New-AzStorageContext</span></span>
* <span data-ttu-id="7b924-623">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="7b924-623">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7b924-624">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7b924-624">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7b924-625">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7b924-625">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7b924-626">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b924-626">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7b924-627">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b924-627">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7b924-628">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="7b924-628">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7b924-629">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7b924-629">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7b924-630">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7b924-630">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7b924-631">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7b924-631">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7b924-632">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7b924-632">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7b924-633">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-633">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7b924-634">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7b924-634">Highlights since the last major release</span></span>
* <span data-ttu-id="7b924-635">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7b924-635">General availability of `Az` module</span></span>
* <span data-ttu-id="7b924-636">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7b924-636">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7b924-637">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7b924-637">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7b924-638">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-638">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7b924-639">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-639">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7b924-640">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-640">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7b924-641">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7b924-641">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7b924-642">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7b924-642">Az.Automation</span></span>
* <span data-ttu-id="7b924-643">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="7b924-643">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7b924-644">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="7b924-644">Dynamic grouping</span></span>
    * <span data-ttu-id="7b924-645">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="7b924-645">Pre-Post script</span></span>
    * <span data-ttu-id="7b924-646">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="7b924-646">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-647">Az.Compute</span></span>
* <span data-ttu-id="7b924-648">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7b924-648">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7b924-649">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-649">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7b924-650">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7b924-650">Az.KeyVault</span></span>
* <span data-ttu-id="7b924-651">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-651">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-652">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-652">Az.Network</span></span>
* <span data-ttu-id="7b924-653">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-653">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7b924-654">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-654">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7b924-655">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7b924-655">Az.RecoveryServices</span></span>
* <span data-ttu-id="7b924-656">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-656">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7b924-657">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-657">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-658">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-658">Az.Resources</span></span>
* <span data-ttu-id="7b924-659">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-659">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7b924-660">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-660">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-661">Az.Sql</span></span>
* <span data-ttu-id="7b924-662">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-662">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7b924-663">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7b924-663">Az.Storage</span></span>
* <span data-ttu-id="7b924-664">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="7b924-664">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7b924-665">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7b924-665">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7b924-666">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7b924-666">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7b924-667">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7b924-667">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7b924-668">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7b924-668">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7b924-669">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7b924-669">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7b924-670">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7b924-670">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7b924-671">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7b924-671">Az.Websites</span></span>
* <span data-ttu-id="7b924-672">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-672">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="7b924-673">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-673">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7b924-674">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7b924-674">Az.Accounts</span></span>
* <span data-ttu-id="7b924-675">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-675">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7b924-676">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-676">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7b924-677">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7b924-677">Az.Automation</span></span>
* <span data-ttu-id="7b924-678">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-678">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7b924-679">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-679">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7b924-680">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="7b924-680">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7b924-681">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7b924-681">Az.Cdn</span></span>
* <span data-ttu-id="7b924-682">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="7b924-682">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-683">Az.Compute</span></span>
* <span data-ttu-id="7b924-684">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-684">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7b924-685">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7b924-685">Az.DataFactory</span></span>
* <span data-ttu-id="7b924-686">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-686">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7b924-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7b924-687">Az.LogicApp</span></span>
* <span data-ttu-id="7b924-688">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="7b924-688">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-689">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-689">Az.Network</span></span>
* <span data-ttu-id="7b924-690">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-690">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7b924-691">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7b924-691">Az.RecoveryServices</span></span>
* <span data-ttu-id="7b924-692">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-692">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7b924-693">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="7b924-693">SDK Update</span></span>
* <span data-ttu-id="7b924-694">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7b924-694">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7b924-695">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-695">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-696">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-696">Az.Resources</span></span>
* <span data-ttu-id="7b924-697">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-697">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7b924-698">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="7b924-698">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7b924-699">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-699">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7b924-700">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="7b924-700">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7b924-701">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-701">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7b924-702">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="7b924-702">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-703">Az.Sql</span></span>
* <span data-ttu-id="7b924-704">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="7b924-704">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7b924-705">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="7b924-705">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7b924-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7b924-706">Az.Storage</span></span>
* <span data-ttu-id="7b924-707">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b924-707">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7b924-708">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-708">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7b924-709">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7b924-709">Az.AnalysisServices</span></span>
* <span data-ttu-id="7b924-710">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="7b924-710">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7b924-711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7b924-711">Az.Automation</span></span>
* <span data-ttu-id="7b924-712">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-712">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7b924-713">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-713">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7b924-714">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-714">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7b924-715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7b924-715">Az.CognitiveServices</span></span>
* <span data-ttu-id="7b924-716">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-716">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-717">Az.Compute</span></span>
* <span data-ttu-id="7b924-718">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-718">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7b924-719">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-719">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7b924-720">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-720">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7b924-721">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="7b924-721">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7b924-722">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7b924-722">Az.DataLakeStore</span></span>
* <span data-ttu-id="7b924-723">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-723">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7b924-724">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7b924-724">Az.EventHub</span></span>
* <span data-ttu-id="7b924-725">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-725">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="7b924-726">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7b924-726">Az.KeyVault</span></span>
* <span data-ttu-id="7b924-727">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-727">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7b924-728">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7b924-728">Az.LogicApp</span></span>
* <span data-ttu-id="7b924-729">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-729">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7b924-730">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-730">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7b924-731">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7b924-731">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7b924-732">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7b924-732">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7b924-733">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7b924-733">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7b924-734">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7b924-734">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7b924-735">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7b924-735">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7b924-736">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7b924-736">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7b924-737">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b924-737">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7b924-738">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b924-738">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7b924-739">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b924-739">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7b924-740">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b924-740">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7b924-741">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-741">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7b924-742">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7b924-742">Az.Monitor</span></span>
* <span data-ttu-id="7b924-743">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-743">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-744">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-744">Az.Network</span></span>
* <span data-ttu-id="7b924-745">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-745">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7b924-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7b924-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="7b924-747">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="7b924-747">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7b924-748">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-748">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="7b924-749">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-749">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="7b924-750">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-750">Az.Resources</span></span>
* <span data-ttu-id="7b924-751">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-751">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7b924-752">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-752">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7b924-753">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-753">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7b924-754">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-754">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-755">Az.Sql</span></span>
* <span data-ttu-id="7b924-756">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-756">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7b924-757">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-757">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7b924-758">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7b924-758">Az.Websites</span></span>
* <span data-ttu-id="7b924-759">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-759">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7b924-760">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-760">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7b924-761">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7b924-761">Az.Accounts</span></span>
* <span data-ttu-id="7b924-762">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7b924-762">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7b924-763">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7b924-763">Az.AnalysisServices</span></span>
<span data-ttu-id="7b924-764">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="7b924-764">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-765">Az.Compute</span></span>
* <span data-ttu-id="7b924-766">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-766">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7b924-767">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-767">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7b924-768">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-768">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7b924-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7b924-769">Az.RecoveryServices</span></span>
<span data-ttu-id="7b924-770">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="7b924-770">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-771">Az.Resources</span></span>
* <span data-ttu-id="7b924-772">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-772">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="7b924-773">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7b924-773">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7b924-774">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-774">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="7b924-775">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7b924-775">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-776">Az.Sql</span></span>
* <span data-ttu-id="7b924-777">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b924-777">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7b924-778">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-778">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7b924-779">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-779">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7b924-780">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-780">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7b924-781">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7b924-781">Az.Accounts</span></span>
* <span data-ttu-id="7b924-782">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="7b924-782">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7b924-783">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7b924-783">Az.AnalysisServices</span></span>
* <span data-ttu-id="7b924-784">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="7b924-784">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7b924-785">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7b924-785">Az.RecoveryServices</span></span>
* <span data-ttu-id="7b924-786">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="7b924-786">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7b924-787">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-787">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7b924-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7b924-788">Az.Accounts</span></span>
* <span data-ttu-id="7b924-789">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-789">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7b924-790">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-790">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7b924-791">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-791">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7b924-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7b924-792">Az.Aks</span></span>
* <span data-ttu-id="7b924-793">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-793">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7b924-794">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7b924-794">Az.Automation</span></span>
* <span data-ttu-id="7b924-795">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-795">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7b924-796">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-796">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7b924-797">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7b924-797">Az.Cdn</span></span>
* <span data-ttu-id="7b924-798">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-798">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-799">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-799">Az.Compute</span></span>
* <span data-ttu-id="7b924-800">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-800">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7b924-801">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-801">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7b924-802">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-802">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7b924-803">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7b924-803">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7b924-804">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-804">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7b924-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7b924-805">Az.DataFactory</span></span>
* <span data-ttu-id="7b924-806">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-806">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7b924-807">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7b924-807">Az.DataLakeStore</span></span>
* <span data-ttu-id="7b924-808">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-808">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7b924-809">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="7b924-809">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7b924-810">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-810">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7b924-811">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7b924-811">Az.IotHub</span></span>
* <span data-ttu-id="7b924-812">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-812">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7b924-813">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7b924-813">Az.KeyVault</span></span>
* <span data-ttu-id="7b924-814">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-814">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-815">Az.Network</span></span>
* <span data-ttu-id="7b924-816">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-816">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-817">Az.Resources</span></span>
* <span data-ttu-id="7b924-818">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-818">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7b924-819">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-819">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7b924-820">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-820">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7b924-821">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-821">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7b924-822">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-822">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7b924-823">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-823">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7b924-824">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="7b924-824">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7b924-825">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7b924-825">Az.ServiceFabric</span></span>
* <span data-ttu-id="7b924-826">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="7b924-826">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7b924-827">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-827">Fix some error messages.</span></span>
* <span data-ttu-id="7b924-828">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-828">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7b924-829">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-829">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7b924-830">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7b924-830">Az.SignalR</span></span>
* <span data-ttu-id="7b924-831">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-831">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-832">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-832">Az.Sql</span></span>
* <span data-ttu-id="7b924-833">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-833">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7b924-834">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-834">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7b924-835">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-835">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7b924-836">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="7b924-836">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7b924-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7b924-837">Az.Storage</span></span>
* <span data-ttu-id="7b924-838">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-838">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7b924-839">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="7b924-839">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7b924-840">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7b924-840">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7b924-841">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7b924-841">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7b924-842">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7b924-842">Az.TrafficManager</span></span>
* <span data-ttu-id="7b924-843">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-843">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7b924-844">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7b924-844">Az.Websites</span></span>
* <span data-ttu-id="7b924-845">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7b924-846">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-846">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7b924-847">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-847">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7b924-848">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="7b924-848">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7b924-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7b924-849">Az.Accounts</span></span>
* <span data-ttu-id="7b924-850">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-850">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-851">Az.Compute</span></span>
* <span data-ttu-id="7b924-852">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="7b924-852">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7b924-853">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-853">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7b924-854">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7b924-854">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7b924-855">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7b924-855">Az.DataLakeStore</span></span>
* <span data-ttu-id="7b924-856">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-856">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7b924-857">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-857">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7b924-858">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7b924-858">Az.EventGrid</span></span>
* <span data-ttu-id="7b924-859">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-859">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7b924-860">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-860">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7b924-861">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7b924-861">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7b924-862">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="7b924-862">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7b924-863">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="7b924-863">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7b924-864">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="7b924-864">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7b924-865">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7b924-865">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7b924-866">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="7b924-866">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7b924-867">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="7b924-867">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7b924-868">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="7b924-868">Dead letter endpoint.</span></span>
* <span data-ttu-id="7b924-869">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-869">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7b924-870">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="7b924-870">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7b924-871">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7b924-871">Az.IotHub</span></span>
* <span data-ttu-id="7b924-872">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-872">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7b924-873">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7b924-873">Az.LogicApp</span></span>
* <span data-ttu-id="7b924-874">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="7b924-874">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-875">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-875">Az.Resources</span></span>
* <span data-ttu-id="7b924-876">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-876">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7b924-877">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="7b924-877">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7b924-878">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-878">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7b924-879">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-879">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7b924-880">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-880">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7b924-881">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="7b924-881">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7b924-882">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7b924-882">Az.SignalR</span></span>
* <span data-ttu-id="7b924-883">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7b924-883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-884">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-884">Az.Sql</span></span>
* <span data-ttu-id="7b924-885">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="7b924-885">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7b924-886">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7b924-886">Az.Storage</span></span>
* <span data-ttu-id="7b924-887">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="7b924-887">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7b924-888">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7b924-888">New-AzStorageContext</span></span>
* <span data-ttu-id="7b924-889">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-889">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7b924-890">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7b924-890">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7b924-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7b924-891">Az.Websites</span></span>
* <span data-ttu-id="7b924-892">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-892">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7b924-893">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7b924-893">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7b924-894">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="7b924-894">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7b924-895">Genel</span><span class="sxs-lookup"><span data-stu-id="7b924-895">General</span></span>

- <span data-ttu-id="7b924-896">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="7b924-896">General Availability of Az Module</span></span>
- <span data-ttu-id="7b924-897">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="7b924-897">Online help for each module</span></span>
- <span data-ttu-id="7b924-898">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="7b924-898">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7b924-899">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-899">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7b924-900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7b924-900">Az.Accounts</span></span>
- <span data-ttu-id="7b924-901">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7b924-901">Changed from Az.Profile</span></span>
- <span data-ttu-id="7b924-902">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-902">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7b924-903">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7b924-903">Az.ApiManagement</span></span>
- <span data-ttu-id="7b924-904">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="7b924-904">Fixes for #7002</span></span>
- <span data-ttu-id="7b924-905">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-905">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7b924-906">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7b924-906">Az.Batch</span></span>
- <span data-ttu-id="7b924-907">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-907">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7b924-908">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="7b924-908">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7b924-909">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7b924-910">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7b924-910">Az.Billing</span></span>
- <span data-ttu-id="7b924-911">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-911">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7b924-912">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7b924-912">Az.CognitivServices</span></span>
- <span data-ttu-id="7b924-913">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-913">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7b924-914">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7b924-914">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7b924-915">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7b924-915">Az.ContainerInstance</span></span>
- <span data-ttu-id="7b924-916">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-916">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7b924-917">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7b924-917">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7b924-918">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-918">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7b924-919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7b924-919">Az.DataLakeStore</span></span>
- <span data-ttu-id="7b924-920">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-920">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7b924-921">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7b924-921">Az.Monitor</span></span>
- <span data-ttu-id="7b924-922">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-922">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7b924-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7b924-923">Az.KeyVault</span></span>
- <span data-ttu-id="7b924-924">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7b924-924">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7b924-925">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7b924-925">Az.MachineLearning</span></span>
- <span data-ttu-id="7b924-926">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-926">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7b924-927">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7b924-927">Az.Media</span></span>
- <span data-ttu-id="7b924-928">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7b924-928">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7b924-929">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-929">Az.Network</span></span>
<span data-ttu-id="7b924-930">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-930">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7b924-931">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7b924-931">New cmdlets added:</span></span>
        - <span data-ttu-id="7b924-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b924-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7b924-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b924-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7b924-934">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b924-934">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7b924-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b924-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7b924-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b924-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7b924-937">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7b924-937">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7b924-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7b924-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7b924-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b924-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7b924-940">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-940">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7b924-941">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b924-941">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7b924-942">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7b924-942">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7b924-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7b924-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7b924-944">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b924-944">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7b924-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7b924-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7b924-946">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="7b924-946">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7b924-947">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-947">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7b924-948">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7b924-948">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7b924-949">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7b924-949">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7b924-950">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7b924-950">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7b924-951">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-951">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7b924-952">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-952">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7b924-953">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7b924-953">Az.OperationalInsights</span></span>
- <span data-ttu-id="7b924-954">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-954">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7b924-955">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7b924-955">Az.Profile</span></span>
- <span data-ttu-id="7b924-956">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-956">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7b924-957">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7b924-957">Az.RecoveryServices</span></span>
- <span data-ttu-id="7b924-958">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-958">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7b924-959">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-959">Az.Resources</span></span>
- <span data-ttu-id="7b924-960">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-960">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7b924-961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7b924-961">Az.ServiceFabric</span></span>
- <span data-ttu-id="7b924-962">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="7b924-962">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7b924-963">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-963">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7b924-964">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7b924-964">Az.SIgnalR</span></span>
- <span data-ttu-id="7b924-965">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7b924-965">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7b924-966">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-966">Az.Sql</span></span>
- <span data-ttu-id="7b924-967">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-967">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7b924-968">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-968">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7b924-969">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-969">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7b924-970">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7b924-970">Az.Storage</span></span>
- <span data-ttu-id="7b924-971">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-971">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7b924-972">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7b924-972">Az.Websites</span></span>
- <span data-ttu-id="7b924-973">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7b924-973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7b924-974">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="7b924-974">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7b924-975">Genel</span><span class="sxs-lookup"><span data-stu-id="7b924-975">General</span></span>

* <span data-ttu-id="7b924-976">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="7b924-976">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7b924-977">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-977">Az.Compute</span></span>

* <span data-ttu-id="7b924-978">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-978">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7b924-979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7b924-979">Az.DataLakeStore</span></span>

* <span data-ttu-id="7b924-980">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-980">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7b924-981">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7b924-981">Az.FrontDoor</span></span>

* <span data-ttu-id="7b924-982">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-982">Fixed some broken links</span></span>
    - <span data-ttu-id="7b924-983">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-983">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7b924-984">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-984">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7b924-985">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7b924-985">Az.RecoveryServices</span></span>

* <span data-ttu-id="7b924-986">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-986">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7b924-987">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-987">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7b924-988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-988">Az.Resources</span></span>

* <span data-ttu-id="7b924-989">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7b924-989">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7b924-990">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-990">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7b924-991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-991">Az.Sql</span></span>

* <span data-ttu-id="7b924-992">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="7b924-992">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7b924-993">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-993">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7b924-994">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-994">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7b924-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7b924-995">Az.Storage</span></span>

* <span data-ttu-id="7b924-996">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-996">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7b924-997">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-997">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7b924-998">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7b924-998">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7b924-999">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-999">Support Static Website configuration</span></span>
    - <span data-ttu-id="7b924-1000">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7b924-1000">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7b924-1001">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7b924-1001">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7b924-1002">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7b924-1002">Az.Websites</span></span>

* <span data-ttu-id="7b924-1003">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7b924-1003">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="7b924-1004">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1004">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7b924-1005">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="7b924-1005">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7b924-1006">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="7b924-1006">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7b924-1007">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7b924-1007">Az.ApiManagement</span></span>
* <span data-ttu-id="7b924-1008">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="7b924-1008">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7b924-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7b924-1009">Az.Automation</span></span>
* <span data-ttu-id="7b924-1010">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="7b924-1010">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7b924-1011">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1011">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7b924-1012">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1012">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7b924-1013">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1013">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7b924-1014">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1014">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7b924-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-1015">Az.Compute</span></span>
* <span data-ttu-id="7b924-1016">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1016">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7b924-1017">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="7b924-1017">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7b924-1018">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7b924-1018">Az.ContainerInstance</span></span>
* <span data-ttu-id="7b924-1019">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="7b924-1019">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7b924-1020">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7b924-1020">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7b924-1021">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1021">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7b924-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-1022">Az.Network</span></span>
* <span data-ttu-id="7b924-1023">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1023">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7b924-1024">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1024">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7b924-1025">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1025">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="7b924-1026">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1026">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7b924-1027">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7b924-1027">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7b924-1028">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1028">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7b924-1029">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="7b924-1029">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7b924-1030">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7b924-1030">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7b924-1031">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1031">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7b924-1032">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="7b924-1032">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7b924-1033">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7b924-1033">Az.Relay</span></span>
* <span data-ttu-id="7b924-1034">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1034">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7b924-1035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-1035">Az.Resources</span></span>
* <span data-ttu-id="7b924-1036">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1036">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7b924-1037">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1037">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7b924-1038">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="7b924-1038">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7b924-1039">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7b924-1039">Az.ServiceFabric</span></span>
* <span data-ttu-id="7b924-1040">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1040">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7b924-1041">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-1041">Az.Sql</span></span>
* <span data-ttu-id="7b924-1042">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1042">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7b924-1043">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7b924-1043">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7b924-1044">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7b924-1044">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7b924-1045">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7b924-1045">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7b924-1046">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7b924-1046">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7b924-1047">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7b924-1047">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7b924-1048">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7b924-1048">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7b924-1049">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7b924-1049">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7b924-1050">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7b924-1050">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7b924-1051">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1051">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7b924-1052">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1052">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7b924-1053">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1053">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7b924-1054">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7b924-1054">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7b924-1055">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7b924-1055">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7b924-1056">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7b924-1056">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7b924-1057">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7b924-1057">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7b924-1058">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1058">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7b924-1059">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="7b924-1059">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7b924-1060">Genel</span><span class="sxs-lookup"><span data-stu-id="7b924-1060">General</span></span>
* <span data-ttu-id="7b924-1061">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="7b924-1061">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7b924-1062">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7b924-1062">Az.Profile</span></span>
* <span data-ttu-id="7b924-1063">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1063">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7b924-1064">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1064">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7b924-1065">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1065">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7b924-1066">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1066">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7b924-1067">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1067">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7b924-1068">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1068">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7b924-1069">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1069">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7b924-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7b924-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="7b924-1071">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1071">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-1072">Az.Compute</span></span>
* <span data-ttu-id="7b924-1073">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1073">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7b924-1074">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="7b924-1074">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7b924-1075">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1075">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7b924-1076">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7b924-1076">Az.DataLakeStore</span></span>
* <span data-ttu-id="7b924-1077">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1077">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7b924-1078">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1078">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7b924-1079">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7b924-1079">Az.Insights</span></span>
* <span data-ttu-id="7b924-1080">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1080">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7b924-1081">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="7b924-1081">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7b924-1082">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1082">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7b924-1083">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="7b924-1083">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-1084">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-1084">Az.Network</span></span>
* <span data-ttu-id="7b924-1085">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="7b924-1085">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7b924-1086">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7b924-1086">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7b924-1087">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7b924-1087">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7b924-1088">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7b924-1088">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7b924-1089">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7b924-1089">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7b924-1090">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7b924-1090">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7b924-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7b924-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7b924-1092">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7b924-1092">Az.PolicyInsights</span></span>
* <span data-ttu-id="7b924-1093">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1093">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-1094">Az.Resources</span></span>
* <span data-ttu-id="7b924-1095">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7b924-1095">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7b924-1096">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="7b924-1096">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7b924-1097">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7b924-1097">Az.ServiceBus</span></span>
* <span data-ttu-id="7b924-1098">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1098">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7b924-1099">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7b924-1099">Az.ServiceFabric</span></span>
* <span data-ttu-id="7b924-1100">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1100">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7b924-1101">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1101">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7b924-1102">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="7b924-1102">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7b924-1103">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="7b924-1103">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7b924-1104">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1104">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7b924-1105">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="7b924-1105">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7b924-1106">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7b924-1106">Az.Profile</span></span>
* <span data-ttu-id="7b924-1107">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7b924-1107">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7b924-1108">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-1109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-1109">Az.Compute</span></span>
* <span data-ttu-id="7b924-1110">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1110">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7b924-1111">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1111">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7b924-1112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7b924-1112">Az.DataLakeStore</span></span>
* <span data-ttu-id="7b924-1113">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="7b924-1113">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7b924-1114">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="7b924-1114">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7b924-1115">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="7b924-1115">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7b924-1116">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7b924-1116">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7b924-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="7b924-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-1118">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-1118">Az.Network</span></span>
* <span data-ttu-id="7b924-1119">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="7b924-1119">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7b924-1120">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1120">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-1121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-1121">Az.Resources</span></span>
* <span data-ttu-id="7b924-1122">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1122">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7b924-1123">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="7b924-1123">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7b924-1124">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="7b924-1124">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7b924-1125">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="7b924-1125">Azure.Storage</span></span>
* <span data-ttu-id="7b924-1126">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="7b924-1126">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7b924-1127">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7b924-1127">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7b924-1128">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7b924-1128">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7b924-1129">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="7b924-1129">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7b924-1130">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7b924-1130">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="7b924-1131">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7b924-1131">Az.CognitiveServices</span></span>
* <span data-ttu-id="7b924-1132">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="7b924-1132">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7b924-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7b924-1133">Az.Compute</span></span>
* <span data-ttu-id="7b924-1134">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1134">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7b924-1135">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1135">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7b924-1136">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7b924-1137">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7b924-1137">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7b924-1138">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7b924-1139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7b924-1139">Az.Network</span></span>
* <span data-ttu-id="7b924-1140">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7b924-1140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7b924-1141">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1141">new cmdlets added</span></span>
    - <span data-ttu-id="7b924-1142">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7b924-1142">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7b924-1143">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7b924-1143">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7b924-1144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7b924-1144">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7b924-1145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7b924-1145">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7b924-1146">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7b924-1146">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7b924-1147">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7b924-1147">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7b924-1148">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7b924-1149">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1149">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7b924-1150">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1150">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7b924-1151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7b924-1151">Az.RedisCache</span></span>
* <span data-ttu-id="7b924-1152">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="7b924-1152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7b924-1153">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7b924-1154">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7b924-1154">Az.Resources</span></span>
* <span data-ttu-id="7b924-1155">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7b924-1155">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7b924-1156">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1156">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7b924-1157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7b924-1157">Az.Sql</span></span>
* <span data-ttu-id="7b924-1158">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7b924-1158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7b924-1159">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7b924-1159">Az.Websites</span></span>
* <span data-ttu-id="7b924-1160">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="7b924-1160">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7b924-1161">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="7b924-1161">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7b924-1162">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="7b924-1162">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7b924-1163">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="7b924-1163">Initial Release</span></span>