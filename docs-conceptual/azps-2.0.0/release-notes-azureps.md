---
ms.openlocfilehash: 3848f7fb8e298d137c747405f32a0776c1a8f029
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048640"
---
## <a name="200---may-2019"></a><span data-ttu-id="31af2-101">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="31af2-101">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31af2-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31af2-102">Az.Accounts</span></span>
* <span data-ttu-id="31af2-103">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="31af2-103">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="31af2-104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31af2-104">Az.CognitiveServices</span></span>
* <span data-ttu-id="31af2-105">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="31af2-105">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="31af2-106">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="31af2-106">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31af2-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-107">Az.Compute</span></span>
* <span data-ttu-id="31af2-108">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="31af2-108">Proximity placement group feature.</span></span>
    - <span data-ttu-id="31af2-109">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="31af2-109">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="31af2-110">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="31af2-110">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="31af2-111">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-111">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="31af2-112">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="31af2-112">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="31af2-113">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-113">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="31af2-114">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="31af2-114">Breaking changes</span></span>
    - <span data-ttu-id="31af2-115">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-115">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="31af2-116">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-116">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="31af2-117">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="31af2-117">Az.DeploymentManager</span></span>
* <span data-ttu-id="31af2-118">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="31af2-118">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="31af2-119">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="31af2-119">Az.Dns</span></span>
* <span data-ttu-id="31af2-120">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="31af2-120">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="31af2-121">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="31af2-121">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="31af2-122">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="31af2-122">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="31af2-123">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="31af2-123">Az.FrontDoor</span></span>
* <span data-ttu-id="31af2-124">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="31af2-124">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="31af2-125">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="31af2-125">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="31af2-126">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="31af2-126">Az.HDInsight</span></span>
* <span data-ttu-id="31af2-127">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="31af2-127">Removed two cmdlets:</span></span>
    - <span data-ttu-id="31af2-128">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="31af2-128">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="31af2-129">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="31af2-129">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="31af2-130">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-130">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="31af2-131">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="31af2-131">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="31af2-132">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="31af2-132">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="31af2-133">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="31af2-133">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="31af2-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31af2-134">Az.Monitor</span></span>
* <span data-ttu-id="31af2-135">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="31af2-135">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="31af2-136">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="31af2-136">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="31af2-137">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="31af2-137">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="31af2-138">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="31af2-138">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="31af2-139">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="31af2-139">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="31af2-140">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="31af2-140">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="31af2-141">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="31af2-141">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="31af2-142">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="31af2-142">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="31af2-143">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="31af2-143">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="31af2-144">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="31af2-144">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="31af2-145">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="31af2-145">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="31af2-146">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="31af2-146">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="31af2-147">SQR API hakkında [daha fazla](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="31af2-147">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="31af2-148">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-148">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31af2-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31af2-149">Az.Network</span></span>
* <span data-ttu-id="31af2-150">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="31af2-150">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="31af2-151">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="31af2-151">New cmdlets</span></span>
        - <span data-ttu-id="31af2-152">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="31af2-152">New-AzNatGateway</span></span>
        - <span data-ttu-id="31af2-153">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="31af2-153">Get-AzNatGateway</span></span>
        - <span data-ttu-id="31af2-154">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="31af2-154">Set-AzNatGateway</span></span>
        - <span data-ttu-id="31af2-155">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="31af2-155">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="31af2-156">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-156">Updated cmdlets</span></span>
        - <span data-ttu-id="31af2-157">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="31af2-157">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="31af2-158">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="31af2-158">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="31af2-159">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="31af2-159">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="31af2-160">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-160">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="31af2-161">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-161">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="31af2-162">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="31af2-162">Az.PolicyInsights</span></span>
* <span data-ttu-id="31af2-163">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="31af2-163">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="31af2-164">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="31af2-164">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="31af2-165">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="31af2-165">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31af2-166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31af2-166">Az.RecoveryServices</span></span>
* <span data-ttu-id="31af2-167">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="31af2-167">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="31af2-168">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="31af2-168">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="31af2-169">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="31af2-169">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="31af2-170">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="31af2-170">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="31af2-171">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="31af2-171">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="31af2-172">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="31af2-172">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="31af2-173">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="31af2-173">Az.Relay</span></span>
* <span data-ttu-id="31af2-174">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="31af2-174">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="31af2-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31af2-175">Az.ServiceBus</span></span>
* <span data-ttu-id="31af2-176">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-176">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31af2-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31af2-177">Az.Storage</span></span>
* <span data-ttu-id="31af2-178">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage.*' ad alanı, 'Microsoft.Azure.Storage.*' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="31af2-178">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="31af2-179">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="31af2-179">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="31af2-180">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="31af2-180">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="31af2-181">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31af2-181">New-AzStorageAccount</span></span>
* <span data-ttu-id="31af2-182">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="31af2-182">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="31af2-183">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31af2-183">New-AzStorageAccount</span></span>
    - <span data-ttu-id="31af2-184">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31af2-184">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="31af2-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31af2-185">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31af2-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31af2-186">Az.Websites</span></span>
* <span data-ttu-id="31af2-187">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="31af2-187">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="31af2-188">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="31af2-188">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="31af2-189">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="31af2-189">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="31af2-190">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="31af2-190">Highlights since the last major release</span></span>
* <span data-ttu-id="31af2-191">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="31af2-191">General availability of `Az` module</span></span>
* <span data-ttu-id="31af2-192">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="31af2-192">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="31af2-193">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="31af2-193">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="31af2-194">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-194">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="31af2-195">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-195">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="31af2-196">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-196">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="31af2-197">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="31af2-197">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="31af2-198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31af2-198">Az.Accounts</span></span>
* <span data-ttu-id="31af2-199">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-199">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="31af2-200">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="31af2-200">Az.Batch</span></span>
* <span data-ttu-id="31af2-201">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="31af2-202">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="31af2-202">Az.Cdn</span></span>
* <span data-ttu-id="31af2-203">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="31af2-204">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31af2-204">Az.CognitiveServices</span></span>
* <span data-ttu-id="31af2-205">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31af2-206">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-206">Az.Compute</span></span>
* <span data-ttu-id="31af2-207">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-207">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="31af2-208">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="31af2-209">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-209">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31af2-210">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31af2-210">Az.DataFactory</span></span>
* <span data-ttu-id="31af2-211">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-211">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31af2-212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31af2-212">Az.DataLakeStore</span></span>
* <span data-ttu-id="31af2-213">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-213">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="31af2-214">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="31af2-214">Az.EventGrid</span></span>
* <span data-ttu-id="31af2-215">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-215">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="31af2-216">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="31af2-216">Az.EventHub</span></span>
* <span data-ttu-id="31af2-217">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-217">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="31af2-218">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="31af2-218">Az.HDInsight</span></span>
* <span data-ttu-id="31af2-219">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="31af2-220">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="31af2-220">Az.IotHub</span></span>
* <span data-ttu-id="31af2-221">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="31af2-222">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31af2-222">Az.KeyVault</span></span>
* <span data-ttu-id="31af2-223">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="31af2-224">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-224">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="31af2-225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="31af2-225">Az.MachineLearning</span></span>
* <span data-ttu-id="31af2-226">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-226">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="31af2-227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="31af2-227">Az.Media</span></span>
* <span data-ttu-id="31af2-228">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-228">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="31af2-229">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31af2-229">Az.Monitor</span></span>
  * <span data-ttu-id="31af2-230">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="31af2-230">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="31af2-231">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="31af2-231">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="31af2-232">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="31af2-232">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="31af2-233">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="31af2-233">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="31af2-234">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="31af2-234">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="31af2-235">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="31af2-235">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="31af2-236">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-236">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31af2-237">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31af2-237">Az.Network</span></span>
* <span data-ttu-id="31af2-238">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="31af2-239">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-239">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="31af2-240">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="31af2-240">Az.NotificationHubs</span></span>
* <span data-ttu-id="31af2-241">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-241">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="31af2-242">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31af2-242">Az.OperationalInsights</span></span>
* <span data-ttu-id="31af2-243">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="31af2-244">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="31af2-244">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="31af2-245">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31af2-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31af2-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="31af2-247">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="31af2-248">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="31af2-248">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="31af2-249">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-249">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="31af2-250">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-250">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="31af2-251">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="31af2-251">Az.RedisCache</span></span>
* <span data-ttu-id="31af2-252">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31af2-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-253">Az.Resources</span></span>
* <span data-ttu-id="31af2-254">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-254">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="31af2-255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31af2-255">Az.Sql</span></span>
* <span data-ttu-id="31af2-256">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-256">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="31af2-257">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="31af2-258">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-258">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="31af2-259">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-259">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="31af2-260">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-260">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="31af2-261">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="31af2-261">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="31af2-262">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-262">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31af2-263">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31af2-263">Az.Websites</span></span>
* <span data-ttu-id="31af2-264">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-264">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="31af2-265">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="31af2-266">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-266">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="31af2-267">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="31af2-267">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="31af2-268">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="31af2-268">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="31af2-269">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="31af2-269">Highlights since the last major release</span></span>
* <span data-ttu-id="31af2-270">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="31af2-270">General availability of `Az` module</span></span>
* <span data-ttu-id="31af2-271">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="31af2-271">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="31af2-272">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="31af2-272">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="31af2-273">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-273">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="31af2-274">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-274">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="31af2-275">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-275">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="31af2-276">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="31af2-276">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="31af2-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31af2-277">Az.Accounts</span></span>
* <span data-ttu-id="31af2-278">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-278">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="31af2-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="31af2-279">Az.AnalysisServices</span></span>
* <span data-ttu-id="31af2-280">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="31af2-280">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="31af2-281">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="31af2-281">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31af2-282">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31af2-282">Az.Automation</span></span>
* <span data-ttu-id="31af2-283">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-283">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="31af2-284">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="31af2-284">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="31af2-285">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="31af2-285">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31af2-286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-286">Az.Compute</span></span>
* <span data-ttu-id="31af2-287">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-287">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="31af2-288">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-288">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="31af2-289">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="31af2-289">Az.ContainerInstance</span></span>
* <span data-ttu-id="31af2-290">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-290">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31af2-291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31af2-291">Az.DataFactory</span></span>
* <span data-ttu-id="31af2-292">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-292">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="31af2-293">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-293">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31af2-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-294">Az.Resources</span></span>
* <span data-ttu-id="31af2-295">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-295">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="31af2-296">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-296">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="31af2-297">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="31af2-297">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="31af2-298">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="31af2-298">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="31af2-299">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-299">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="31af2-300">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="31af2-300">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="31af2-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31af2-301">Az.Sql</span></span>
* <span data-ttu-id="31af2-302">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="31af2-302">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31af2-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31af2-303">Az.Storage</span></span>
* <span data-ttu-id="31af2-304">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="31af2-304">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="31af2-305">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="31af2-305">New-AzStorageContext</span></span>
* <span data-ttu-id="31af2-306">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="31af2-306">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="31af2-307">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="31af2-307">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="31af2-308">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="31af2-308">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="31af2-309">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="31af2-309">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="31af2-310">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="31af2-310">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="31af2-311">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="31af2-311">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="31af2-312">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="31af2-312">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="31af2-313">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="31af2-313">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="31af2-314">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="31af2-314">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="31af2-315">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="31af2-315">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="31af2-316">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="31af2-316">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="31af2-317">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="31af2-317">Highlights since the last major release</span></span>
* <span data-ttu-id="31af2-318">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="31af2-318">General availability of `Az` module</span></span>
* <span data-ttu-id="31af2-319">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="31af2-319">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="31af2-320">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="31af2-320">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="31af2-321">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-321">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="31af2-322">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-322">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="31af2-323">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-323">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="31af2-324">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="31af2-324">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31af2-325">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31af2-325">Az.Automation</span></span>
* <span data-ttu-id="31af2-326">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="31af2-326">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="31af2-327">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="31af2-327">Dynamic grouping</span></span>
    * <span data-ttu-id="31af2-328">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="31af2-328">Pre-Post script</span></span>
    * <span data-ttu-id="31af2-329">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="31af2-329">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31af2-330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-330">Az.Compute</span></span>
* <span data-ttu-id="31af2-331">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="31af2-331">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="31af2-332">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-332">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="31af2-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31af2-333">Az.KeyVault</span></span>
* <span data-ttu-id="31af2-334">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-334">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31af2-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31af2-335">Az.Network</span></span>
* <span data-ttu-id="31af2-336">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-336">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="31af2-337">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-337">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31af2-338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31af2-338">Az.RecoveryServices</span></span>
* <span data-ttu-id="31af2-339">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-339">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="31af2-340">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-340">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="31af2-341">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-341">Az.Resources</span></span>
* <span data-ttu-id="31af2-342">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-342">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="31af2-343">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-343">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="31af2-344">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31af2-344">Az.Sql</span></span>
* <span data-ttu-id="31af2-345">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-345">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31af2-346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31af2-346">Az.Storage</span></span>
* <span data-ttu-id="31af2-347">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="31af2-347">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="31af2-348">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="31af2-348">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="31af2-349">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="31af2-349">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="31af2-350">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="31af2-350">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="31af2-351">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="31af2-351">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="31af2-352">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="31af2-352">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="31af2-353">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="31af2-353">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31af2-354">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31af2-354">Az.Websites</span></span>
* <span data-ttu-id="31af2-355">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-355">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="31af2-356">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="31af2-356">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31af2-357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31af2-357">Az.Accounts</span></span>
* <span data-ttu-id="31af2-358">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-358">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="31af2-359">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-359">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31af2-360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31af2-360">Az.Automation</span></span>
* <span data-ttu-id="31af2-361">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-361">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="31af2-362">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-362">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="31af2-363">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="31af2-363">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="31af2-364">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="31af2-364">Az.Cdn</span></span>
* <span data-ttu-id="31af2-365">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="31af2-365">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31af2-366">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-366">Az.Compute</span></span>
* <span data-ttu-id="31af2-367">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-367">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31af2-368">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31af2-368">Az.DataFactory</span></span>
* <span data-ttu-id="31af2-369">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-369">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="31af2-370">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="31af2-370">Az.LogicApp</span></span>
* <span data-ttu-id="31af2-371">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="31af2-371">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31af2-372">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31af2-372">Az.Network</span></span>
* <span data-ttu-id="31af2-373">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-373">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31af2-374">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31af2-374">Az.RecoveryServices</span></span>
* <span data-ttu-id="31af2-375">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-375">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="31af2-376">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="31af2-376">SDK Update</span></span>
* <span data-ttu-id="31af2-377">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="31af2-377">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="31af2-378">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-378">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="31af2-379">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-379">Az.Resources</span></span>
* <span data-ttu-id="31af2-380">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-380">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="31af2-381">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="31af2-381">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="31af2-382">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-382">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="31af2-383">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="31af2-383">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="31af2-384">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-384">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="31af2-385">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="31af2-385">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="31af2-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31af2-386">Az.Sql</span></span>
* <span data-ttu-id="31af2-387">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="31af2-387">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="31af2-388">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="31af2-388">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31af2-389">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31af2-389">Az.Storage</span></span>
* <span data-ttu-id="31af2-390">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31af2-390">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="31af2-391">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="31af2-391">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="31af2-392">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="31af2-392">Az.AnalysisServices</span></span>
* <span data-ttu-id="31af2-393">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="31af2-393">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31af2-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31af2-394">Az.Automation</span></span>
* <span data-ttu-id="31af2-395">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-395">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="31af2-396">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-396">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="31af2-397">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-397">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="31af2-398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31af2-398">Az.CognitiveServices</span></span>
* <span data-ttu-id="31af2-399">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-399">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31af2-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-400">Az.Compute</span></span>
* <span data-ttu-id="31af2-401">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-401">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="31af2-402">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-402">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="31af2-403">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-403">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="31af2-404">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="31af2-404">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31af2-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31af2-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="31af2-406">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-406">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="31af2-407">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="31af2-407">Az.EventHub</span></span>
* <span data-ttu-id="31af2-408">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-408">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="31af2-409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31af2-409">Az.KeyVault</span></span>
* <span data-ttu-id="31af2-410">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-410">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="31af2-411">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="31af2-411">Az.LogicApp</span></span>
* <span data-ttu-id="31af2-412">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-412">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="31af2-413">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-413">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="31af2-414">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="31af2-414">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="31af2-415">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="31af2-415">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="31af2-416">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="31af2-416">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="31af2-417">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="31af2-417">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="31af2-418">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="31af2-418">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="31af2-419">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="31af2-419">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="31af2-420">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="31af2-420">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="31af2-421">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="31af2-421">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="31af2-422">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="31af2-422">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="31af2-423">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="31af2-423">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="31af2-424">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-424">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="31af2-425">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31af2-425">Az.Monitor</span></span>
* <span data-ttu-id="31af2-426">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-426">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31af2-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31af2-427">Az.Network</span></span>
* <span data-ttu-id="31af2-428">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-428">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="31af2-429">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31af2-429">Az.OperationalInsights</span></span>
* <span data-ttu-id="31af2-430">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="31af2-430">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="31af2-431">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-431">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="31af2-432">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-432">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="31af2-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-433">Az.Resources</span></span>
* <span data-ttu-id="31af2-434">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-434">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="31af2-435">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-435">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="31af2-436">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-436">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="31af2-437">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-437">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="31af2-438">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31af2-438">Az.Sql</span></span>
* <span data-ttu-id="31af2-439">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-439">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="31af2-440">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-440">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31af2-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31af2-441">Az.Websites</span></span>
* <span data-ttu-id="31af2-442">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-442">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="31af2-443">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="31af2-443">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31af2-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31af2-444">Az.Accounts</span></span>
* <span data-ttu-id="31af2-445">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="31af2-445">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="31af2-446">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="31af2-446">Az.AnalysisServices</span></span>
<span data-ttu-id="31af2-447">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="31af2-447">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31af2-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-448">Az.Compute</span></span>
* <span data-ttu-id="31af2-449">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-449">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="31af2-450">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-450">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="31af2-451">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-451">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31af2-452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31af2-452">Az.RecoveryServices</span></span>
<span data-ttu-id="31af2-453">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="31af2-453">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31af2-454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-454">Az.Resources</span></span>
* <span data-ttu-id="31af2-455">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-455">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="31af2-456">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="31af2-456">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="31af2-457">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-457">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="31af2-458">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="31af2-458">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="31af2-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31af2-459">Az.Sql</span></span>
* <span data-ttu-id="31af2-460">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="31af2-460">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="31af2-461">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-461">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="31af2-462">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-462">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="31af2-463">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="31af2-463">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31af2-464">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31af2-464">Az.Accounts</span></span>
* <span data-ttu-id="31af2-465">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="31af2-465">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="31af2-466">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="31af2-466">Az.AnalysisServices</span></span>
* <span data-ttu-id="31af2-467">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="31af2-467">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31af2-468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31af2-468">Az.RecoveryServices</span></span>
* <span data-ttu-id="31af2-469">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="31af2-469">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="31af2-470">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="31af2-470">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31af2-471">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31af2-471">Az.Accounts</span></span>
* <span data-ttu-id="31af2-472">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-472">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="31af2-473">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-473">Update incorrect online help URLs</span></span>
* <span data-ttu-id="31af2-474">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-474">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="31af2-475">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="31af2-475">Az.Aks</span></span>
* <span data-ttu-id="31af2-476">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-476">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31af2-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31af2-477">Az.Automation</span></span>
* <span data-ttu-id="31af2-478">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-478">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="31af2-479">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-479">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="31af2-480">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="31af2-480">Az.Cdn</span></span>
* <span data-ttu-id="31af2-481">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-481">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31af2-482">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-482">Az.Compute</span></span>
* <span data-ttu-id="31af2-483">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-483">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="31af2-484">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-484">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="31af2-485">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-485">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="31af2-486">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="31af2-486">Az.ContainerRegistry</span></span>
* <span data-ttu-id="31af2-487">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-487">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31af2-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31af2-488">Az.DataFactory</span></span>
* <span data-ttu-id="31af2-489">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-489">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31af2-490">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31af2-490">Az.DataLakeStore</span></span>
* <span data-ttu-id="31af2-491">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-491">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="31af2-492">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="31af2-492">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="31af2-493">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-493">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="31af2-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="31af2-494">Az.IotHub</span></span>
* <span data-ttu-id="31af2-495">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-495">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="31af2-496">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31af2-496">Az.KeyVault</span></span>
* <span data-ttu-id="31af2-497">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-497">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31af2-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31af2-498">Az.Network</span></span>
* <span data-ttu-id="31af2-499">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-499">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="31af2-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-500">Az.Resources</span></span>
* <span data-ttu-id="31af2-501">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-501">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="31af2-502">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-502">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="31af2-503">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-503">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="31af2-504">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-504">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="31af2-505">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-505">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="31af2-506">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-506">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="31af2-507">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="31af2-507">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="31af2-508">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31af2-508">Az.ServiceFabric</span></span>
* <span data-ttu-id="31af2-509">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="31af2-509">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="31af2-510">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-510">Fix some error messages.</span></span>
* <span data-ttu-id="31af2-511">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-511">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="31af2-512">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-512">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="31af2-513">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="31af2-513">Az.SignalR</span></span>
* <span data-ttu-id="31af2-514">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-514">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="31af2-515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31af2-515">Az.Sql</span></span>
* <span data-ttu-id="31af2-516">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="31af2-517">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-517">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="31af2-518">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-518">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="31af2-519">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="31af2-519">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31af2-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31af2-520">Az.Storage</span></span>
* <span data-ttu-id="31af2-521">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-521">Update incorrect online help URLs</span></span>
* <span data-ttu-id="31af2-522">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="31af2-522">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="31af2-523">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="31af2-523">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="31af2-524">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="31af2-524">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="31af2-525">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="31af2-525">Az.TrafficManager</span></span>
* <span data-ttu-id="31af2-526">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-526">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31af2-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31af2-527">Az.Websites</span></span>
* <span data-ttu-id="31af2-528">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-528">Update incorrect online help URLs</span></span>
* <span data-ttu-id="31af2-529">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-529">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="31af2-530">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-530">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="31af2-531">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="31af2-531">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31af2-532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31af2-532">Az.Accounts</span></span>
* <span data-ttu-id="31af2-533">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-533">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31af2-534">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-534">Az.Compute</span></span>
* <span data-ttu-id="31af2-535">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="31af2-535">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="31af2-536">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-536">Updated the description of ID in help files</span></span>
* <span data-ttu-id="31af2-537">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="31af2-537">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31af2-538">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31af2-538">Az.DataLakeStore</span></span>
* <span data-ttu-id="31af2-539">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-539">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="31af2-540">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-540">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="31af2-541">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="31af2-541">Az.EventGrid</span></span>
* <span data-ttu-id="31af2-542">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-542">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="31af2-543">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-543">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="31af2-544">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="31af2-544">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="31af2-545">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="31af2-545">Event Time-To-Live,</span></span>
        - <span data-ttu-id="31af2-546">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="31af2-546">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="31af2-547">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="31af2-547">Dead letter endpoint.</span></span>
    - <span data-ttu-id="31af2-548">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="31af2-548">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="31af2-549">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="31af2-549">Event Time-To-Live,</span></span>
        - <span data-ttu-id="31af2-550">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="31af2-550">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="31af2-551">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="31af2-551">Dead letter endpoint.</span></span>
* <span data-ttu-id="31af2-552">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-552">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="31af2-553">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="31af2-553">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="31af2-554">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="31af2-554">Az.IotHub</span></span>
* <span data-ttu-id="31af2-555">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-555">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="31af2-556">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="31af2-556">Az.LogicApp</span></span>
* <span data-ttu-id="31af2-557">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="31af2-557">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="31af2-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-558">Az.Resources</span></span>
* <span data-ttu-id="31af2-559">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-559">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="31af2-560">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="31af2-560">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="31af2-561">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-561">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="31af2-562">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-562">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="31af2-563">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-563">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="31af2-564">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="31af2-564">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="31af2-565">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="31af2-565">Az.SignalR</span></span>
* <span data-ttu-id="31af2-566">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="31af2-566">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="31af2-567">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31af2-567">Az.Sql</span></span>
* <span data-ttu-id="31af2-568">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="31af2-568">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31af2-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31af2-569">Az.Storage</span></span>
* <span data-ttu-id="31af2-570">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="31af2-570">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="31af2-571">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="31af2-571">New-AzStorageContext</span></span>
* <span data-ttu-id="31af2-572">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-572">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="31af2-573">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="31af2-573">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31af2-574">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31af2-574">Az.Websites</span></span>
* <span data-ttu-id="31af2-575">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-575">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="31af2-576">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="31af2-576">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="31af2-577">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="31af2-577">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="31af2-578">Genel</span><span class="sxs-lookup"><span data-stu-id="31af2-578">General</span></span>

- <span data-ttu-id="31af2-579">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="31af2-579">General Availability of Az Module</span></span>
- <span data-ttu-id="31af2-580">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="31af2-580">Online help for each module</span></span>
- <span data-ttu-id="31af2-581">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="31af2-581">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="31af2-582">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-582">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="31af2-583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31af2-583">Az.Accounts</span></span>
- <span data-ttu-id="31af2-584">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="31af2-584">Changed from Az.Profile</span></span>
- <span data-ttu-id="31af2-585">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-585">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="31af2-586">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31af2-586">Az.ApiManagement</span></span>
- <span data-ttu-id="31af2-587">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="31af2-587">Fixes for #7002</span></span>
- <span data-ttu-id="31af2-588">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="31af2-589">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="31af2-589">Az.Batch</span></span>
- <span data-ttu-id="31af2-590">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-590">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="31af2-591">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="31af2-591">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="31af2-592">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="31af2-593">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="31af2-593">Az.Billing</span></span>
- <span data-ttu-id="31af2-594">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-594">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="31af2-595">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="31af2-595">Az.CognitivServices</span></span>
- <span data-ttu-id="31af2-596">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-596">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="31af2-597">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="31af2-597">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="31af2-598">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="31af2-598">Az.ContainerInstance</span></span>
- <span data-ttu-id="31af2-599">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-599">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="31af2-600">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="31af2-600">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="31af2-601">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="31af2-602">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31af2-602">Az.DataLakeStore</span></span>
- <span data-ttu-id="31af2-603">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="31af2-604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31af2-604">Az.Monitor</span></span>
- <span data-ttu-id="31af2-605">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-605">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="31af2-606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31af2-606">Az.KeyVault</span></span>
- <span data-ttu-id="31af2-607">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="31af2-607">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="31af2-608">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="31af2-608">Az.MachineLearning</span></span>
- <span data-ttu-id="31af2-609">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-609">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="31af2-610">Az.Media</span><span class="sxs-lookup"><span data-stu-id="31af2-610">Az.Media</span></span>
- <span data-ttu-id="31af2-611">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="31af2-611">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="31af2-612">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31af2-612">Az.Network</span></span>
<span data-ttu-id="31af2-613">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-613">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="31af2-614">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="31af2-614">New cmdlets added:</span></span>
        - <span data-ttu-id="31af2-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31af2-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31af2-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31af2-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31af2-617">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31af2-617">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31af2-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31af2-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31af2-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31af2-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31af2-620">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="31af2-620">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="31af2-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="31af2-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="31af2-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="31af2-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="31af2-623">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-623">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="31af2-624">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31af2-624">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="31af2-625">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="31af2-625">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="31af2-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="31af2-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="31af2-627">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31af2-627">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="31af2-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="31af2-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="31af2-629">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="31af2-629">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="31af2-630">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-630">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="31af2-631">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="31af2-631">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="31af2-632">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="31af2-632">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="31af2-633">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="31af2-633">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="31af2-634">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-634">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="31af2-635">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-635">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="31af2-636">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31af2-636">Az.OperationalInsights</span></span>
- <span data-ttu-id="31af2-637">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-637">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="31af2-638">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="31af2-638">Az.Profile</span></span>
- <span data-ttu-id="31af2-639">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-639">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="31af2-640">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31af2-640">Az.RecoveryServices</span></span>
- <span data-ttu-id="31af2-641">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-641">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="31af2-642">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-642">Az.Resources</span></span>
- <span data-ttu-id="31af2-643">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-643">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="31af2-644">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31af2-644">Az.ServiceFabric</span></span>
- <span data-ttu-id="31af2-645">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="31af2-645">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="31af2-646">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-646">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="31af2-647">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="31af2-647">Az.SIgnalR</span></span>
- <span data-ttu-id="31af2-648">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="31af2-648">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="31af2-649">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31af2-649">Az.Sql</span></span>
- <span data-ttu-id="31af2-650">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-650">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="31af2-651">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-651">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="31af2-652">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="31af2-653">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31af2-653">Az.Storage</span></span>
- <span data-ttu-id="31af2-654">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="31af2-655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31af2-655">Az.Websites</span></span>
- <span data-ttu-id="31af2-656">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="31af2-656">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="31af2-657">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="31af2-657">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="31af2-658">Genel</span><span class="sxs-lookup"><span data-stu-id="31af2-658">General</span></span>

* <span data-ttu-id="31af2-659">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="31af2-659">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="31af2-660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-660">Az.Compute</span></span>

* <span data-ttu-id="31af2-661">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-661">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="31af2-662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31af2-662">Az.DataLakeStore</span></span>

* <span data-ttu-id="31af2-663">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-663">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="31af2-664">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="31af2-664">Az.FrontDoor</span></span>

* <span data-ttu-id="31af2-665">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-665">Fixed some broken links</span></span>
    - <span data-ttu-id="31af2-666">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-666">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="31af2-667">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-667">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="31af2-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31af2-668">Az.RecoveryServices</span></span>

* <span data-ttu-id="31af2-669">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-669">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="31af2-670">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-670">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="31af2-671">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-671">Az.Resources</span></span>

* <span data-ttu-id="31af2-672">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="31af2-672">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="31af2-673">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-673">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="31af2-674">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31af2-674">Az.Sql</span></span>

* <span data-ttu-id="31af2-675">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="31af2-675">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="31af2-676">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-676">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="31af2-677">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-677">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="31af2-678">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31af2-678">Az.Storage</span></span>

* <span data-ttu-id="31af2-679">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-679">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="31af2-680">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-680">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="31af2-681">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="31af2-681">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="31af2-682">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-682">Support Static Website configuration</span></span>
    - <span data-ttu-id="31af2-683">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="31af2-683">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="31af2-684">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="31af2-684">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="31af2-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31af2-685">Az.Websites</span></span>

* <span data-ttu-id="31af2-686">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="31af2-686">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="31af2-687">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-687">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="31af2-688">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="31af2-688">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="31af2-689">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="31af2-689">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="31af2-690">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31af2-690">Az.ApiManagement</span></span>
* <span data-ttu-id="31af2-691">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="31af2-691">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="31af2-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31af2-692">Az.Automation</span></span>
* <span data-ttu-id="31af2-693">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="31af2-693">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="31af2-694">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-694">Added Update Management cmdlets</span></span>
* <span data-ttu-id="31af2-695">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-695">Added Source Control cmdlets</span></span>
* <span data-ttu-id="31af2-696">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-696">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="31af2-697">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-697">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="31af2-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-698">Az.Compute</span></span>
* <span data-ttu-id="31af2-699">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-699">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="31af2-700">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="31af2-700">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="31af2-701">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="31af2-701">Az.ContainerInstance</span></span>
* <span data-ttu-id="31af2-702">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="31af2-702">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="31af2-703">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="31af2-703">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="31af2-704">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-704">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="31af2-705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31af2-705">Az.Network</span></span>
* <span data-ttu-id="31af2-706">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-706">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="31af2-707">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-707">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="31af2-708">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-708">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="31af2-709">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-709">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="31af2-710">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="31af2-710">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="31af2-711">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-711">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="31af2-712">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="31af2-712">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="31af2-713">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="31af2-713">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="31af2-714">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-714">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="31af2-715">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="31af2-715">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="31af2-716">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="31af2-716">Az.Relay</span></span>
* <span data-ttu-id="31af2-717">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-717">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="31af2-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-718">Az.Resources</span></span>
* <span data-ttu-id="31af2-719">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-719">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="31af2-720">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-720">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="31af2-721">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="31af2-721">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="31af2-722">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31af2-722">Az.ServiceFabric</span></span>
* <span data-ttu-id="31af2-723">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-723">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="31af2-724">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31af2-724">Az.Sql</span></span>
* <span data-ttu-id="31af2-725">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-725">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="31af2-726">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31af2-726">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="31af2-727">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31af2-727">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="31af2-728">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31af2-728">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="31af2-729">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31af2-729">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="31af2-730">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="31af2-730">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="31af2-731">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="31af2-731">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="31af2-732">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="31af2-732">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="31af2-733">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="31af2-733">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="31af2-734">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-734">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="31af2-735">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-735">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="31af2-736">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-736">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="31af2-737">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="31af2-737">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="31af2-738">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="31af2-738">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="31af2-739">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="31af2-739">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="31af2-740">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="31af2-740">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="31af2-741">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-741">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="31af2-742">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="31af2-742">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="31af2-743">Genel</span><span class="sxs-lookup"><span data-stu-id="31af2-743">General</span></span>
* <span data-ttu-id="31af2-744">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="31af2-744">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="31af2-745">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="31af2-745">Az.Profile</span></span>
* <span data-ttu-id="31af2-746">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-746">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="31af2-747">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-747">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="31af2-748">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-748">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="31af2-749">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-749">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="31af2-750">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-750">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="31af2-751">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-751">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="31af2-752">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-752">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="31af2-753">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31af2-753">Az.CognitiveServices</span></span>
* <span data-ttu-id="31af2-754">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-754">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31af2-755">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-755">Az.Compute</span></span>
* <span data-ttu-id="31af2-756">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-756">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="31af2-757">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="31af2-757">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="31af2-758">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-758">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31af2-759">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31af2-759">Az.DataLakeStore</span></span>
* <span data-ttu-id="31af2-760">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-760">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="31af2-761">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-761">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="31af2-762">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="31af2-762">Az.Insights</span></span>
* <span data-ttu-id="31af2-763">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-763">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="31af2-764">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="31af2-764">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="31af2-765">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-765">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="31af2-766">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="31af2-766">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31af2-767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31af2-767">Az.Network</span></span>
* <span data-ttu-id="31af2-768">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="31af2-768">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="31af2-769">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="31af2-769">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="31af2-770">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="31af2-770">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="31af2-771">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="31af2-771">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="31af2-772">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="31af2-772">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="31af2-773">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="31af2-773">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="31af2-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="31af2-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="31af2-775">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="31af2-775">Az.PolicyInsights</span></span>
* <span data-ttu-id="31af2-776">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-776">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="31af2-777">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-777">Az.Resources</span></span>
* <span data-ttu-id="31af2-778">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="31af2-778">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="31af2-779">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="31af2-779">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="31af2-780">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31af2-780">Az.ServiceBus</span></span>
* <span data-ttu-id="31af2-781">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-781">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="31af2-782">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31af2-782">Az.ServiceFabric</span></span>
* <span data-ttu-id="31af2-783">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-783">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="31af2-784">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-784">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="31af2-785">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="31af2-785">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="31af2-786">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="31af2-786">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="31af2-787">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-787">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="31af2-788">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="31af2-788">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="31af2-789">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="31af2-789">Az.Profile</span></span>
* <span data-ttu-id="31af2-790">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="31af2-790">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="31af2-791">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="31af2-791">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31af2-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-792">Az.Compute</span></span>
* <span data-ttu-id="31af2-793">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-793">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="31af2-794">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-794">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31af2-795">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31af2-795">Az.DataLakeStore</span></span>
* <span data-ttu-id="31af2-796">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="31af2-796">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="31af2-797">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="31af2-797">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="31af2-798">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="31af2-798">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="31af2-799">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="31af2-799">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="31af2-800">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="31af2-800">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31af2-801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31af2-801">Az.Network</span></span>
* <span data-ttu-id="31af2-802">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="31af2-802">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="31af2-803">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-803">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31af2-804">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-804">Az.Resources</span></span>
* <span data-ttu-id="31af2-805">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-805">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="31af2-806">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="31af2-806">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="31af2-807">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="31af2-807">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="31af2-808">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="31af2-808">Azure.Storage</span></span>
* <span data-ttu-id="31af2-809">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="31af2-809">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="31af2-810">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="31af2-810">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="31af2-811">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="31af2-811">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="31af2-812">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="31af2-812">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="31af2-813">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="31af2-813">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="31af2-814">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31af2-814">Az.CognitiveServices</span></span>
* <span data-ttu-id="31af2-815">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="31af2-815">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31af2-816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31af2-816">Az.Compute</span></span>
* <span data-ttu-id="31af2-817">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-817">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="31af2-818">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-818">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="31af2-819">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-819">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="31af2-820">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="31af2-820">Az.DataFactoryV2</span></span>
* <span data-ttu-id="31af2-821">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="31af2-821">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31af2-822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31af2-822">Az.Network</span></span>
* <span data-ttu-id="31af2-823">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="31af2-823">Added NetworkProfile functionality.</span></span> <span data-ttu-id="31af2-824">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-824">new cmdlets added</span></span>
    - <span data-ttu-id="31af2-825">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31af2-825">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="31af2-826">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31af2-826">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="31af2-827">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31af2-827">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="31af2-828">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31af2-828">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="31af2-829">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="31af2-829">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="31af2-830">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="31af2-830">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="31af2-831">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-831">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="31af2-832">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-832">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="31af2-833">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-833">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="31af2-834">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="31af2-834">Az.RedisCache</span></span>
* <span data-ttu-id="31af2-835">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="31af2-835">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="31af2-836">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-836">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="31af2-837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31af2-837">Az.Resources</span></span>
* <span data-ttu-id="31af2-838">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="31af2-838">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="31af2-839">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-839">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="31af2-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31af2-840">Az.Sql</span></span>
* <span data-ttu-id="31af2-841">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="31af2-841">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31af2-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31af2-842">Az.Websites</span></span>
* <span data-ttu-id="31af2-843">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="31af2-843">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="31af2-844">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="31af2-844">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="31af2-845">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="31af2-845">0.2.0 - September 2018</span></span>
 <span data-ttu-id="31af2-846">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="31af2-846">Initial Release</span></span>