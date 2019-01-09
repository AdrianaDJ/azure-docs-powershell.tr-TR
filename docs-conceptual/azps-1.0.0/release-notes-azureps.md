## <a name="100---december-2018"></a><span data-ttu-id="e1648-101">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="e1648-101">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e1648-102">Genel</span><span class="sxs-lookup"><span data-stu-id="e1648-102">General</span></span>

- <span data-ttu-id="e1648-103">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="e1648-103">General Availability of Az Module</span></span>
- <span data-ttu-id="e1648-104">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="e1648-104">Online help for each module</span></span>
- <span data-ttu-id="e1648-105">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="e1648-105">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e1648-106">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-106">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e1648-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e1648-107">Az.Accounts</span></span>
- <span data-ttu-id="e1648-108">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e1648-108">Changed from Az.Profile</span></span>
- <span data-ttu-id="e1648-109">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-109">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e1648-110">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e1648-110">Az.ApiManagement</span></span>
- <span data-ttu-id="e1648-111">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="e1648-111">Fixes for #7002</span></span>
- <span data-ttu-id="e1648-112">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-112">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e1648-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e1648-113">Az.Batch</span></span>
- <span data-ttu-id="e1648-114">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-114">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e1648-115">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="e1648-115">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e1648-116">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-116">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e1648-117">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e1648-117">Az.Billing</span></span>
- <span data-ttu-id="e1648-118">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-118">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e1648-119">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e1648-119">Az.CognitivServices</span></span>
- <span data-ttu-id="e1648-120">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-120">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e1648-121">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e1648-121">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e1648-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e1648-122">Az.ContainerInstance</span></span>
- <span data-ttu-id="e1648-123">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-123">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e1648-124">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e1648-124">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e1648-125">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-125">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e1648-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e1648-126">Az.DataLakeStore</span></span>
- <span data-ttu-id="e1648-127">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-127">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e1648-128">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e1648-128">Az.Monitor</span></span>
- <span data-ttu-id="e1648-129">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-129">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e1648-130">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e1648-130">Az.KeyVault</span></span>
- <span data-ttu-id="e1648-131">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e1648-131">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e1648-132">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e1648-132">Az.MachineLearning</span></span>
- <span data-ttu-id="e1648-133">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-133">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e1648-134">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e1648-134">Az.Media</span></span>
- <span data-ttu-id="e1648-135">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="e1648-135">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e1648-136">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1648-136">Az.Network</span></span>
<span data-ttu-id="e1648-137">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-137">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e1648-138">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="e1648-138">New cmdlets added:</span></span>
        - <span data-ttu-id="e1648-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1648-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e1648-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1648-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e1648-141">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1648-141">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e1648-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1648-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e1648-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1648-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e1648-144">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e1648-144">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e1648-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e1648-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e1648-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1648-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e1648-147">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e1648-147">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e1648-148">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1648-148">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e1648-149">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e1648-149">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e1648-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e1648-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e1648-151">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e1648-151">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e1648-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e1648-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e1648-153">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="e1648-153">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e1648-154">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e1648-154">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e1648-155">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e1648-155">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e1648-156">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e1648-156">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e1648-157">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e1648-157">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e1648-158">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e1648-158">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e1648-159">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-159">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e1648-160">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e1648-160">Az.OperationalInsights</span></span>
- <span data-ttu-id="e1648-161">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-161">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e1648-162">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e1648-162">Az.Profile</span></span>
- <span data-ttu-id="e1648-163">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="e1648-163">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e1648-164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e1648-164">Az.RecoveryServices</span></span>
- <span data-ttu-id="e1648-165">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-165">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e1648-166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1648-166">Az.Resources</span></span>
- <span data-ttu-id="e1648-167">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-167">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e1648-168">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e1648-168">Az.ServiceFabric</span></span>
- <span data-ttu-id="e1648-169">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="e1648-169">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e1648-170">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-170">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e1648-171">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e1648-171">Az.SIgnalR</span></span>
- <span data-ttu-id="e1648-172">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="e1648-172">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e1648-173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1648-173">Az.Sql</span></span>
- <span data-ttu-id="e1648-174">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-174">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e1648-175">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e1648-175">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e1648-176">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-176">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e1648-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e1648-177">Az.Storage</span></span>
- <span data-ttu-id="e1648-178">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-178">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e1648-179">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e1648-179">Az.Websites</span></span>
- <span data-ttu-id="e1648-180">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e1648-180">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e1648-181">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="e1648-181">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e1648-182">Genel</span><span class="sxs-lookup"><span data-stu-id="e1648-182">General</span></span>

* <span data-ttu-id="e1648-183">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="e1648-183">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e1648-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1648-184">Az.Compute</span></span>

* <span data-ttu-id="e1648-185">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-185">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e1648-186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e1648-186">Az.DataLakeStore</span></span>

* <span data-ttu-id="e1648-187">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-187">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e1648-188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e1648-188">Az.FrontDoor</span></span>

* <span data-ttu-id="e1648-189">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-189">Fixed some broken links</span></span>
    - <span data-ttu-id="e1648-190">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-190">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e1648-191">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-191">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e1648-192">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e1648-192">Az.RecoveryServices</span></span>

* <span data-ttu-id="e1648-193">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-193">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e1648-194">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-194">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e1648-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1648-195">Az.Resources</span></span>

* <span data-ttu-id="e1648-196">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="e1648-196">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e1648-197">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-197">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e1648-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1648-198">Az.Sql</span></span>

* <span data-ttu-id="e1648-199">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="e1648-199">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e1648-200">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-200">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e1648-201">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-201">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e1648-202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e1648-202">Az.Storage</span></span>

* <span data-ttu-id="e1648-203">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-203">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e1648-204">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-204">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e1648-205">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e1648-205">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e1648-206">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-206">Support Static Website configuration</span></span>
    - <span data-ttu-id="e1648-207">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e1648-207">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e1648-208">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e1648-208">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e1648-209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e1648-209">Az.Websites</span></span>

* <span data-ttu-id="e1648-210">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e1648-210">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="e1648-211">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-211">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e1648-212">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="e1648-212">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e1648-213">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="e1648-213">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e1648-214">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e1648-214">Az.ApiManagement</span></span>
* <span data-ttu-id="e1648-215">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="e1648-215">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e1648-216">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e1648-216">Az.Automation</span></span>
* <span data-ttu-id="e1648-217">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="e1648-217">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e1648-218">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-218">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e1648-219">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-219">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e1648-220">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-220">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e1648-221">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-221">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e1648-222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1648-222">Az.Compute</span></span>
* <span data-ttu-id="e1648-223">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-223">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e1648-224">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="e1648-224">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e1648-225">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e1648-225">Az.ContainerInstance</span></span>
* <span data-ttu-id="e1648-226">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="e1648-226">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e1648-227">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e1648-227">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e1648-228">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e1648-228">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e1648-229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1648-229">Az.Network</span></span>
* <span data-ttu-id="e1648-230">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-230">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e1648-231">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-231">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e1648-232">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-232">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="e1648-233">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-233">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e1648-234">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e1648-234">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e1648-235">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-235">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e1648-236">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="e1648-236">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e1648-237">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e1648-237">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e1648-238">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-238">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e1648-239">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="e1648-239">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e1648-240">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e1648-240">Az.Relay</span></span>
* <span data-ttu-id="e1648-241">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-241">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e1648-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1648-242">Az.Resources</span></span>
* <span data-ttu-id="e1648-243">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e1648-243">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e1648-244">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-244">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e1648-245">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="e1648-245">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e1648-246">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e1648-246">Az.ServiceFabric</span></span>
* <span data-ttu-id="e1648-247">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-247">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e1648-248">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1648-248">Az.Sql</span></span>
* <span data-ttu-id="e1648-249">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-249">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e1648-250">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e1648-250">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e1648-251">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e1648-251">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e1648-252">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e1648-252">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e1648-253">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e1648-253">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e1648-254">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e1648-254">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e1648-255">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e1648-255">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e1648-256">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e1648-256">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e1648-257">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e1648-257">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e1648-258">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-258">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e1648-259">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-259">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e1648-260">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-260">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e1648-261">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e1648-261">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e1648-262">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e1648-262">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e1648-263">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e1648-263">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e1648-264">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e1648-264">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e1648-265">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-265">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e1648-266">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="e1648-266">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e1648-267">Genel</span><span class="sxs-lookup"><span data-stu-id="e1648-267">General</span></span>
* <span data-ttu-id="e1648-268">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="e1648-268">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e1648-269">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e1648-269">Az.Profile</span></span>
* <span data-ttu-id="e1648-270">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e1648-270">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e1648-271">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-271">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e1648-272">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e1648-272">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e1648-273">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-273">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e1648-274">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-274">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e1648-275">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-275">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e1648-276">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-276">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e1648-277">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e1648-277">Az.CognitiveServices</span></span>
* <span data-ttu-id="e1648-278">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-278">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1648-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1648-279">Az.Compute</span></span>
* <span data-ttu-id="e1648-280">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-280">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e1648-281">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="e1648-281">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e1648-282">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-282">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e1648-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e1648-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="e1648-284">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-284">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e1648-285">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-285">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e1648-286">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e1648-286">Az.Insights</span></span>
* <span data-ttu-id="e1648-287">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-287">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e1648-288">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="e1648-288">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e1648-289">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-289">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e1648-290">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="e1648-290">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e1648-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1648-291">Az.Network</span></span>
* <span data-ttu-id="e1648-292">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="e1648-292">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e1648-293">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1648-293">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e1648-294">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e1648-294">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e1648-295">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e1648-295">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e1648-296">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e1648-296">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e1648-297">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1648-297">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e1648-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e1648-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e1648-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e1648-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="e1648-300">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-300">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1648-301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1648-301">Az.Resources</span></span>
* <span data-ttu-id="e1648-302">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="e1648-302">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e1648-303">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="e1648-303">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e1648-304">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e1648-304">Az.ServiceBus</span></span>
* <span data-ttu-id="e1648-305">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-305">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e1648-306">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e1648-306">Az.ServiceFabric</span></span>
* <span data-ttu-id="e1648-307">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-307">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e1648-308">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-308">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e1648-309">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="e1648-309">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e1648-310">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e1648-310">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e1648-311">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-311">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e1648-312">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="e1648-312">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e1648-313">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e1648-313">Az.Profile</span></span>
* <span data-ttu-id="e1648-314">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="e1648-314">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e1648-315">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="e1648-315">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1648-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1648-316">Az.Compute</span></span>
* <span data-ttu-id="e1648-317">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-317">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e1648-318">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-318">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e1648-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e1648-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="e1648-320">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="e1648-320">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e1648-321">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="e1648-321">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e1648-322">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="e1648-322">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e1648-323">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e1648-323">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e1648-324">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="e1648-324">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e1648-325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1648-325">Az.Network</span></span>
* <span data-ttu-id="e1648-326">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="e1648-326">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e1648-327">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-327">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1648-328">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1648-328">Az.Resources</span></span>
* <span data-ttu-id="e1648-329">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-329">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e1648-330">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="e1648-330">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e1648-331">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="e1648-331">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e1648-332">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="e1648-332">Azure.Storage</span></span>
* <span data-ttu-id="e1648-333">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="e1648-333">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e1648-334">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e1648-334">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e1648-335">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e1648-335">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e1648-336">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="e1648-336">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e1648-337">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e1648-337">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="e1648-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e1648-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="e1648-339">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="e1648-339">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e1648-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e1648-340">Az.Compute</span></span>
* <span data-ttu-id="e1648-341">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-341">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e1648-342">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-342">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e1648-343">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-343">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e1648-344">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e1648-344">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e1648-345">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e1648-345">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e1648-346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e1648-346">Az.Network</span></span>
* <span data-ttu-id="e1648-347">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="e1648-347">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e1648-348">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-348">new cmdlets added</span></span>
    - <span data-ttu-id="e1648-349">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e1648-349">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e1648-350">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e1648-350">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e1648-351">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e1648-351">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e1648-352">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e1648-352">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e1648-353">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e1648-353">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e1648-354">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e1648-354">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e1648-355">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-355">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e1648-356">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-356">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e1648-357">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-357">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e1648-358">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e1648-358">Az.RedisCache</span></span>
* <span data-ttu-id="e1648-359">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="e1648-359">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e1648-360">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-360">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e1648-361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e1648-361">Az.Resources</span></span>
* <span data-ttu-id="e1648-362">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="e1648-362">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e1648-363">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-363">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e1648-364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e1648-364">Az.Sql</span></span>
* <span data-ttu-id="e1648-365">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="e1648-365">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e1648-366">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e1648-366">Az.Websites</span></span>
* <span data-ttu-id="e1648-367">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="e1648-367">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e1648-368">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="e1648-368">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e1648-369">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="e1648-369">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e1648-370">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="e1648-370">Initial Release</span></span>