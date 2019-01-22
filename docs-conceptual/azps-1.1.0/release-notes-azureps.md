---
ms.openlocfilehash: 179d22fa065944695e4769f2698e3cabc7666b04
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342156"
---
## <a name="110---january-2019"></a><span data-ttu-id="fa8dc-101">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="fa8dc-101">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fa8dc-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fa8dc-102">Az.Accounts</span></span>
* <span data-ttu-id="fa8dc-103">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-103">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fa8dc-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fa8dc-104">Az.Compute</span></span>
* <span data-ttu-id="fa8dc-105">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="fa8dc-105">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="fa8dc-106">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-106">Updated the description of ID in help files</span></span>
* <span data-ttu-id="fa8dc-107">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="fa8dc-107">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fa8dc-108">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fa8dc-108">Az.DataLakeStore</span></span>
* <span data-ttu-id="fa8dc-109">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-109">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="fa8dc-110">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-110">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fa8dc-111">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fa8dc-111">Az.EventGrid</span></span>
* <span data-ttu-id="fa8dc-112">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-112">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="fa8dc-113">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-113">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="fa8dc-114">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="fa8dc-114">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="fa8dc-115">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="fa8dc-115">Event Time-To-Live,</span></span>
        - <span data-ttu-id="fa8dc-116">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="fa8dc-116">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="fa8dc-117">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-117">Dead letter endpoint.</span></span>
    - <span data-ttu-id="fa8dc-118">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="fa8dc-118">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="fa8dc-119">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="fa8dc-119">Event Time-To-Live,</span></span>
        - <span data-ttu-id="fa8dc-120">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="fa8dc-120">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="fa8dc-121">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-121">Dead letter endpoint.</span></span>
* <span data-ttu-id="fa8dc-122">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-122">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="fa8dc-123">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-123">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fa8dc-124">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fa8dc-124">Az.IotHub</span></span>
* <span data-ttu-id="fa8dc-125">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-125">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fa8dc-126">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fa8dc-126">Az.LogicApp</span></span>
* <span data-ttu-id="fa8dc-127">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="fa8dc-127">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="fa8dc-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fa8dc-128">Az.Resources</span></span>
* <span data-ttu-id="fa8dc-129">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-129">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="fa8dc-130">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="fa8dc-130">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="fa8dc-131">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-131">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="fa8dc-132">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-132">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="fa8dc-133">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-133">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="fa8dc-134">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="fa8dc-134">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="fa8dc-135">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="fa8dc-135">Az.SignalR</span></span>
* <span data-ttu-id="fa8dc-136">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="fa8dc-136">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="fa8dc-137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fa8dc-137">Az.Sql</span></span>
* <span data-ttu-id="fa8dc-138">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-138">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fa8dc-139">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fa8dc-139">Az.Storage</span></span>
* <span data-ttu-id="fa8dc-140">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="fa8dc-140">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="fa8dc-141">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fa8dc-141">New-AzStorageContext</span></span>
* <span data-ttu-id="fa8dc-142">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-142">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="fa8dc-143">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="fa8dc-143">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fa8dc-144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fa8dc-144">Az.Websites</span></span>
* <span data-ttu-id="fa8dc-145">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-145">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="fa8dc-146">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="fa8dc-146">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="fa8dc-147">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="fa8dc-147">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="fa8dc-148">Genel</span><span class="sxs-lookup"><span data-stu-id="fa8dc-148">General</span></span>

- <span data-ttu-id="fa8dc-149">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="fa8dc-149">General Availability of Az Module</span></span>
- <span data-ttu-id="fa8dc-150">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="fa8dc-150">Online help for each module</span></span>
- <span data-ttu-id="fa8dc-151">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-151">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="fa8dc-152">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-152">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="fa8dc-153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fa8dc-153">Az.Accounts</span></span>
- <span data-ttu-id="fa8dc-154">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fa8dc-154">Changed from Az.Profile</span></span>
- <span data-ttu-id="fa8dc-155">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-155">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="fa8dc-156">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fa8dc-156">Az.ApiManagement</span></span>
- <span data-ttu-id="fa8dc-157">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="fa8dc-157">Fixes for #7002</span></span>
- <span data-ttu-id="fa8dc-158">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-158">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="fa8dc-159">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fa8dc-159">Az.Batch</span></span>
- <span data-ttu-id="fa8dc-160">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-160">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="fa8dc-161">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-161">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="fa8dc-162">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-162">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="fa8dc-163">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="fa8dc-163">Az.Billing</span></span>
- <span data-ttu-id="fa8dc-164">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-164">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="fa8dc-165">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="fa8dc-165">Az.CognitivServices</span></span>
- <span data-ttu-id="fa8dc-166">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-166">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="fa8dc-167">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="fa8dc-167">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="fa8dc-168">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fa8dc-168">Az.ContainerInstance</span></span>
- <span data-ttu-id="fa8dc-169">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-169">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="fa8dc-170">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fa8dc-170">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="fa8dc-171">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-171">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="fa8dc-172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fa8dc-172">Az.DataLakeStore</span></span>
- <span data-ttu-id="fa8dc-173">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-173">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="fa8dc-174">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fa8dc-174">Az.Monitor</span></span>
- <span data-ttu-id="fa8dc-175">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-175">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="fa8dc-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fa8dc-176">Az.KeyVault</span></span>
- <span data-ttu-id="fa8dc-177">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="fa8dc-177">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="fa8dc-178">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fa8dc-178">Az.MachineLearning</span></span>
- <span data-ttu-id="fa8dc-179">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-179">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="fa8dc-180">Az.Media</span><span class="sxs-lookup"><span data-stu-id="fa8dc-180">Az.Media</span></span>
- <span data-ttu-id="fa8dc-181">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="fa8dc-181">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="fa8dc-182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fa8dc-182">Az.Network</span></span>
<span data-ttu-id="fa8dc-183">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-183">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="fa8dc-184">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="fa8dc-184">New cmdlets added:</span></span>
        - <span data-ttu-id="fa8dc-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa8dc-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fa8dc-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa8dc-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fa8dc-187">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa8dc-187">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fa8dc-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa8dc-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fa8dc-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa8dc-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fa8dc-190">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="fa8dc-190">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="fa8dc-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="fa8dc-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="fa8dc-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="fa8dc-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="fa8dc-193">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-193">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="fa8dc-194">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fa8dc-194">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="fa8dc-195">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fa8dc-195">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="fa8dc-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fa8dc-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="fa8dc-197">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fa8dc-197">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="fa8dc-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fa8dc-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="fa8dc-199">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-199">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="fa8dc-200">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-200">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="fa8dc-201">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fa8dc-201">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="fa8dc-202">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fa8dc-202">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="fa8dc-203">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fa8dc-203">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="fa8dc-204">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-204">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="fa8dc-205">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="fa8dc-206">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fa8dc-206">Az.OperationalInsights</span></span>
- <span data-ttu-id="fa8dc-207">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="fa8dc-208">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fa8dc-208">Az.Profile</span></span>
- <span data-ttu-id="fa8dc-209">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-209">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="fa8dc-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fa8dc-210">Az.RecoveryServices</span></span>
- <span data-ttu-id="fa8dc-211">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-211">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="fa8dc-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fa8dc-212">Az.Resources</span></span>
- <span data-ttu-id="fa8dc-213">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-213">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="fa8dc-214">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fa8dc-214">Az.ServiceFabric</span></span>
- <span data-ttu-id="fa8dc-215">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="fa8dc-215">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="fa8dc-216">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-216">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="fa8dc-217">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="fa8dc-217">Az.SIgnalR</span></span>
- <span data-ttu-id="fa8dc-218">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="fa8dc-218">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="fa8dc-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fa8dc-219">Az.Sql</span></span>
- <span data-ttu-id="fa8dc-220">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-220">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="fa8dc-221">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-221">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="fa8dc-222">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-222">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="fa8dc-223">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fa8dc-223">Az.Storage</span></span>
- <span data-ttu-id="fa8dc-224">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-224">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="fa8dc-225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fa8dc-225">Az.Websites</span></span>
- <span data-ttu-id="fa8dc-226">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="fa8dc-226">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="fa8dc-227">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="fa8dc-227">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="fa8dc-228">Genel</span><span class="sxs-lookup"><span data-stu-id="fa8dc-228">General</span></span>

* <span data-ttu-id="fa8dc-229">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="fa8dc-229">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="fa8dc-230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fa8dc-230">Az.Compute</span></span>

* <span data-ttu-id="fa8dc-231">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-231">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="fa8dc-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fa8dc-232">Az.DataLakeStore</span></span>

* <span data-ttu-id="fa8dc-233">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-233">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="fa8dc-234">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fa8dc-234">Az.FrontDoor</span></span>

* <span data-ttu-id="fa8dc-235">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-235">Fixed some broken links</span></span>
    - <span data-ttu-id="fa8dc-236">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-236">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="fa8dc-237">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-237">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="fa8dc-238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fa8dc-238">Az.RecoveryServices</span></span>

* <span data-ttu-id="fa8dc-239">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-239">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="fa8dc-240">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-240">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="fa8dc-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fa8dc-241">Az.Resources</span></span>

* <span data-ttu-id="fa8dc-242">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-242">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="fa8dc-243">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-243">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="fa8dc-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fa8dc-244">Az.Sql</span></span>

* <span data-ttu-id="fa8dc-245">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="fa8dc-245">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="fa8dc-246">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-246">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="fa8dc-247">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-247">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="fa8dc-248">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fa8dc-248">Az.Storage</span></span>

* <span data-ttu-id="fa8dc-249">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-249">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="fa8dc-250">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-250">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="fa8dc-251">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fa8dc-251">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="fa8dc-252">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-252">Support Static Website configuration</span></span>
    - <span data-ttu-id="fa8dc-253">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fa8dc-253">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="fa8dc-254">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fa8dc-254">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="fa8dc-255">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fa8dc-255">Az.Websites</span></span>

* <span data-ttu-id="fa8dc-256">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fa8dc-256">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="fa8dc-257">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-257">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="fa8dc-258">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-258">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="fa8dc-259">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="fa8dc-259">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="fa8dc-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fa8dc-260">Az.ApiManagement</span></span>
* <span data-ttu-id="fa8dc-261">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="fa8dc-261">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="fa8dc-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fa8dc-262">Az.Automation</span></span>
* <span data-ttu-id="fa8dc-263">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="fa8dc-263">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="fa8dc-264">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-264">Added Update Management cmdlets</span></span>
* <span data-ttu-id="fa8dc-265">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-265">Added Source Control cmdlets</span></span>
* <span data-ttu-id="fa8dc-266">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-266">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="fa8dc-267">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-267">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="fa8dc-268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fa8dc-268">Az.Compute</span></span>
* <span data-ttu-id="fa8dc-269">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-269">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="fa8dc-270">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="fa8dc-270">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="fa8dc-271">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fa8dc-271">Az.ContainerInstance</span></span>
* <span data-ttu-id="fa8dc-272">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="fa8dc-272">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="fa8dc-273">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="fa8dc-273">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="fa8dc-274">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-274">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="fa8dc-275">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fa8dc-275">Az.Network</span></span>
* <span data-ttu-id="fa8dc-276">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-276">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="fa8dc-277">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-277">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="fa8dc-278">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-278">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="fa8dc-279">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-279">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="fa8dc-280">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fa8dc-280">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fa8dc-281">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-281">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="fa8dc-282">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-282">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="fa8dc-283">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fa8dc-283">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fa8dc-284">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-284">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="fa8dc-285">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="fa8dc-285">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="fa8dc-286">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="fa8dc-286">Az.Relay</span></span>
* <span data-ttu-id="fa8dc-287">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-287">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="fa8dc-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fa8dc-288">Az.Resources</span></span>
* <span data-ttu-id="fa8dc-289">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-289">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="fa8dc-290">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-290">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="fa8dc-291">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="fa8dc-291">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="fa8dc-292">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fa8dc-292">Az.ServiceFabric</span></span>
* <span data-ttu-id="fa8dc-293">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-293">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="fa8dc-294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fa8dc-294">Az.Sql</span></span>
* <span data-ttu-id="fa8dc-295">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-295">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="fa8dc-296">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fa8dc-296">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fa8dc-297">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fa8dc-297">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fa8dc-298">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fa8dc-298">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fa8dc-299">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fa8dc-299">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fa8dc-300">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fa8dc-300">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fa8dc-301">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fa8dc-301">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fa8dc-302">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fa8dc-302">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fa8dc-303">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fa8dc-303">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="fa8dc-304">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-304">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="fa8dc-305">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-305">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="fa8dc-306">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-306">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="fa8dc-307">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-307">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="fa8dc-308">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-308">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="fa8dc-309">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-309">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="fa8dc-310">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-310">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="fa8dc-311">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-311">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="fa8dc-312">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="fa8dc-312">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fa8dc-313">Genel</span><span class="sxs-lookup"><span data-stu-id="fa8dc-313">General</span></span>
* <span data-ttu-id="fa8dc-314">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="fa8dc-314">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="fa8dc-315">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fa8dc-315">Az.Profile</span></span>
* <span data-ttu-id="fa8dc-316">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-316">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="fa8dc-317">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-317">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="fa8dc-318">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-318">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="fa8dc-319">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-319">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="fa8dc-320">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-320">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="fa8dc-321">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-321">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="fa8dc-322">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-322">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="fa8dc-323">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fa8dc-323">Az.CognitiveServices</span></span>
* <span data-ttu-id="fa8dc-324">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-324">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fa8dc-325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fa8dc-325">Az.Compute</span></span>
* <span data-ttu-id="fa8dc-326">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-326">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="fa8dc-327">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="fa8dc-327">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="fa8dc-328">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-328">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fa8dc-329">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fa8dc-329">Az.DataLakeStore</span></span>
* <span data-ttu-id="fa8dc-330">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-330">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="fa8dc-331">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-331">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="fa8dc-332">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="fa8dc-332">Az.Insights</span></span>
* <span data-ttu-id="fa8dc-333">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-333">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="fa8dc-334">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="fa8dc-334">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="fa8dc-335">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-335">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="fa8dc-336">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="fa8dc-336">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fa8dc-337">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fa8dc-337">Az.Network</span></span>
* <span data-ttu-id="fa8dc-338">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="fa8dc-338">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="fa8dc-339">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="fa8dc-339">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="fa8dc-340">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="fa8dc-340">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="fa8dc-341">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fa8dc-341">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="fa8dc-342">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="fa8dc-342">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="fa8dc-343">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="fa8dc-343">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="fa8dc-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fa8dc-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fa8dc-345">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fa8dc-345">Az.PolicyInsights</span></span>
* <span data-ttu-id="fa8dc-346">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-346">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="fa8dc-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fa8dc-347">Az.Resources</span></span>
* <span data-ttu-id="fa8dc-348">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-348">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="fa8dc-349">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="fa8dc-349">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fa8dc-350">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fa8dc-350">Az.ServiceBus</span></span>
* <span data-ttu-id="fa8dc-351">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-351">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fa8dc-352">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fa8dc-352">Az.ServiceFabric</span></span>
* <span data-ttu-id="fa8dc-353">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-353">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="fa8dc-354">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-354">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="fa8dc-355">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="fa8dc-355">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="fa8dc-356">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="fa8dc-356">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="fa8dc-357">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-357">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="fa8dc-358">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="fa8dc-358">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="fa8dc-359">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fa8dc-359">Az.Profile</span></span>
* <span data-ttu-id="fa8dc-360">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="fa8dc-360">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="fa8dc-361">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-361">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fa8dc-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fa8dc-362">Az.Compute</span></span>
* <span data-ttu-id="fa8dc-363">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-363">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="fa8dc-364">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-364">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fa8dc-365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fa8dc-365">Az.DataLakeStore</span></span>
* <span data-ttu-id="fa8dc-366">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="fa8dc-366">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="fa8dc-367">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-367">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="fa8dc-368">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-368">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fa8dc-369">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-369">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fa8dc-370">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-370">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fa8dc-371">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fa8dc-371">Az.Network</span></span>
* <span data-ttu-id="fa8dc-372">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-372">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="fa8dc-373">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-373">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fa8dc-374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fa8dc-374">Az.Resources</span></span>
* <span data-ttu-id="fa8dc-375">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-375">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="fa8dc-376">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-376">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="fa8dc-377">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="fa8dc-377">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="fa8dc-378">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="fa8dc-378">Azure.Storage</span></span>
* <span data-ttu-id="fa8dc-379">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="fa8dc-379">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="fa8dc-380">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fa8dc-380">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="fa8dc-381">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fa8dc-381">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="fa8dc-382">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-382">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="fa8dc-383">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="fa8dc-383">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="fa8dc-384">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fa8dc-384">Az.CognitiveServices</span></span>
* <span data-ttu-id="fa8dc-385">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-385">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fa8dc-386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fa8dc-386">Az.Compute</span></span>
* <span data-ttu-id="fa8dc-387">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-387">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="fa8dc-388">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-388">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="fa8dc-389">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-389">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="fa8dc-390">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fa8dc-390">Az.DataFactoryV2</span></span>
* <span data-ttu-id="fa8dc-391">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-391">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fa8dc-392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fa8dc-392">Az.Network</span></span>
* <span data-ttu-id="fa8dc-393">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-393">Added NetworkProfile functionality.</span></span> <span data-ttu-id="fa8dc-394">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-394">new cmdlets added</span></span>
    - <span data-ttu-id="fa8dc-395">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fa8dc-395">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="fa8dc-396">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fa8dc-396">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="fa8dc-397">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fa8dc-397">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="fa8dc-398">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fa8dc-398">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="fa8dc-399">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="fa8dc-399">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="fa8dc-400">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="fa8dc-400">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="fa8dc-401">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-401">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="fa8dc-402">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-402">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="fa8dc-403">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-403">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fa8dc-404">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fa8dc-404">Az.RedisCache</span></span>
* <span data-ttu-id="fa8dc-405">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="fa8dc-405">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="fa8dc-406">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-406">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="fa8dc-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fa8dc-407">Az.Resources</span></span>
* <span data-ttu-id="fa8dc-408">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-408">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="fa8dc-409">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-409">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="fa8dc-410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fa8dc-410">Az.Sql</span></span>
* <span data-ttu-id="fa8dc-411">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="fa8dc-411">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fa8dc-412">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fa8dc-412">Az.Websites</span></span>
* <span data-ttu-id="fa8dc-413">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="fa8dc-413">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="fa8dc-414">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="fa8dc-414">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="fa8dc-415">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="fa8dc-415">0.2.0 - September 2018</span></span>
 <span data-ttu-id="fa8dc-416">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="fa8dc-416">Initial Release</span></span>