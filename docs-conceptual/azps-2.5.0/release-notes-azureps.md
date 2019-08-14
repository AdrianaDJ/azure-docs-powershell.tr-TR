---
ms.openlocfilehash: 77cb28e47d8dddcf3936edff23f794de3b78442b
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861184"
---
## <a name="250---july-2019"></a><span data-ttu-id="68bc5-101">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="68bc5-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="68bc5-102">Az.Accounts</span></span>
* <span data-ttu-id="68bc5-103">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="68bc5-104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="68bc5-104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="68bc5-105">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="68bc5-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="68bc5-106">Az.Automation</span></span>
* <span data-ttu-id="68bc5-107">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-107">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="68bc5-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="68bc5-109">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-110">Az.Compute</span></span>
* <span data-ttu-id="68bc5-111">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="68bc5-112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="68bc5-112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="68bc5-113">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="68bc5-114">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="68bc5-114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="68bc5-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="68bc5-115">Az.DataFactory</span></span>
* <span data-ttu-id="68bc5-116">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="68bc5-117">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="68bc5-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="68bc5-118">Az.EventHub</span></span>
* <span data-ttu-id="68bc5-119">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="68bc5-119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="68bc5-120">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="68bc5-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="68bc5-121">Az.KeyVault</span></span>
* <span data-ttu-id="68bc5-122">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="68bc5-123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="68bc5-123">Az.LogicApp</span></span>
* <span data-ttu-id="68bc5-124">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="68bc5-124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="68bc5-125">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="68bc5-126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-126">Az.ManagedServices</span></span>
* <span data-ttu-id="68bc5-127">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="68bc5-127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-128">Az.Network</span></span>
* <span data-ttu-id="68bc5-129">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="68bc5-130">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-130">New cmdlets</span></span>
        - <span data-ttu-id="68bc5-131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="68bc5-131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="68bc5-132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="68bc5-132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="68bc5-133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="68bc5-133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="68bc5-134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="68bc5-134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="68bc5-135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="68bc5-135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="68bc5-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="68bc5-136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="68bc5-137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="68bc5-137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="68bc5-138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="68bc5-138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="68bc5-139">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="68bc5-139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="68bc5-140">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="68bc5-141">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanmasını etkinleştirmeyi veya devre dışı bırakmayı göstermek için isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="68bc5-142">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanmasını etkinleştirmeyi veya devre dışı bırakmayı göstermek için isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="68bc5-143">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="68bc5-143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="68bc5-144">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="68bc5-145">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-145">Updated cmdlets</span></span>
        - <span data-ttu-id="68bc5-146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="68bc5-146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="68bc5-147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="68bc5-147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="68bc5-148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="68bc5-148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="68bc5-149">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="68bc5-150">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="68bc5-151">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="68bc5-151">Updated cmdlet:</span></span>
        - <span data-ttu-id="68bc5-152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="68bc5-152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="68bc5-153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="68bc5-153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="68bc5-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="68bc5-154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="68bc5-155">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="68bc5-156">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="68bc5-157">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="68bc5-157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="68bc5-158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="68bc5-158">Az.OperationalInsights</span></span>
* <span data-ttu-id="68bc5-159">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-159">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="68bc5-160">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="68bc5-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="68bc5-162">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="68bc5-163">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="68bc5-164">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="68bc5-165">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="68bc5-166">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="68bc5-167">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="68bc5-168">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="68bc5-169">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="68bc5-170">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="68bc5-171">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-172">Az.Resources</span></span>
- <span data-ttu-id="68bc5-173">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="68bc5-173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="68bc5-174">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="68bc5-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="68bc5-175">Az.ServiceBus</span></span>
* <span data-ttu-id="68bc5-176">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="68bc5-176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="68bc5-177">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-178">Az.Sql</span></span>
* <span data-ttu-id="68bc5-179">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="68bc5-180">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="68bc5-181">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="68bc5-182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="68bc5-182">Az.Storage</span></span>
* <span data-ttu-id="68bc5-183">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="68bc5-184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="68bc5-184">Az.StorageSync</span></span>
* <span data-ttu-id="68bc5-185">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="68bc5-185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="68bc5-186">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="68bc5-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="68bc5-187">Az.Websites</span></span>
* <span data-ttu-id="68bc5-188">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="68bc5-189">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="68bc5-190">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="68bc5-191">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="68bc5-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="68bc5-192">Az.Accounts</span></span>
* <span data-ttu-id="68bc5-193">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="68bc5-194">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="68bc5-195">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="68bc5-196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="68bc5-196">Az.Advisor</span></span>
* <span data-ttu-id="68bc5-197">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="68bc5-197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="68bc5-198">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="68bc5-198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="68bc5-199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="68bc5-199">Az.ApiManagement</span></span>
* <span data-ttu-id="68bc5-200">https://github.com/Azure/azure-powershell/issues/8671 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="68bc5-201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="68bc5-201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="68bc5-202">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="68bc5-203">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="68bc5-203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="68bc5-204">https://github.com/Azure/azure-powershell/issues/9307 ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="68bc5-204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="68bc5-205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="68bc5-205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="68bc5-206">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="68bc5-207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="68bc5-207">Az.Automation</span></span>
* <span data-ttu-id="68bc5-208">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-209">Az.Compute</span></span>
* <span data-ttu-id="68bc5-210">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="68bc5-211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="68bc5-211">Az.DataFactory</span></span>
* <span data-ttu-id="68bc5-212">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="68bc5-212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="68bc5-213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="68bc5-213">Az.EventGrid</span></span>
* <span data-ttu-id="68bc5-214">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="68bc5-215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="68bc5-215">Az.IotHub</span></span>
* <span data-ttu-id="68bc5-216">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-217">Az.Network</span></span>
* <span data-ttu-id="68bc5-218">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="68bc5-219">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="68bc5-220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="68bc5-220">Az.PolicyInsights</span></span>
* <span data-ttu-id="68bc5-221">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="68bc5-222">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="68bc5-222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="68bc5-223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="68bc5-223">Az.OperationalInsights</span></span>
* <span data-ttu-id="68bc5-224">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="68bc5-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="68bc5-226">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="68bc5-226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-227">Az.Resources</span></span>
    - <span data-ttu-id="68bc5-228">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="68bc5-228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="68bc5-229">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="68bc5-230">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="68bc5-231">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="68bc5-232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="68bc5-232">Az.ServiceBus</span></span>
* <span data-ttu-id="68bc5-233">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-234">Az.Sql</span></span>
* <span data-ttu-id="68bc5-235">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="68bc5-236">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="68bc5-236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="68bc5-237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="68bc5-237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="68bc5-238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="68bc5-238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="68bc5-239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="68bc5-239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="68bc5-240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="68bc5-240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="68bc5-241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="68bc5-241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="68bc5-242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="68bc5-242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="68bc5-243">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="68bc5-243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="68bc5-244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="68bc5-244">Az.Storage</span></span>
* <span data-ttu-id="68bc5-245">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="68bc5-245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="68bc5-246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="68bc5-246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="68bc5-247">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="68bc5-248">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="68bc5-248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="68bc5-249">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="68bc5-250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68bc5-250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="68bc5-251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68bc5-251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="68bc5-252">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="68bc5-253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="68bc5-253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="68bc5-254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="68bc5-254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="68bc5-255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="68bc5-255">Az.StorageSync</span></span>
* <span data-ttu-id="68bc5-256">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="68bc5-256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="68bc5-257">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="68bc5-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="68bc5-258">Az.Accounts</span></span>
* <span data-ttu-id="68bc5-259">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="68bc5-260">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="68bc5-260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="68bc5-261">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="68bc5-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="68bc5-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="68bc5-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="68bc5-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-264">Az.Compute</span></span>
* <span data-ttu-id="68bc5-265">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="68bc5-265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="68bc5-266">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="68bc5-267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="68bc5-267">Az.Dns</span></span>
* <span data-ttu-id="68bc5-268">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="68bc5-269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="68bc5-269">Az.EventGrid</span></span>
* <span data-ttu-id="68bc5-270">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="68bc5-271">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="68bc5-271">New cmdlets:</span></span>
    - <span data-ttu-id="68bc5-272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="68bc5-272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="68bc5-273">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="68bc5-273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="68bc5-274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="68bc5-274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="68bc5-275">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="68bc5-275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="68bc5-276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="68bc5-276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="68bc5-277">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68bc5-277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="68bc5-278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="68bc5-278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="68bc5-279">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="68bc5-279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="68bc5-280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="68bc5-280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="68bc5-281">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="68bc5-281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="68bc5-282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="68bc5-282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="68bc5-283">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="68bc5-283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="68bc5-284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="68bc5-284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="68bc5-285">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="68bc5-285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="68bc5-286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="68bc5-286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="68bc5-287">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68bc5-287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="68bc5-288">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="68bc5-288">Updated cmdlets:</span></span>
    - <span data-ttu-id="68bc5-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="68bc5-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="68bc5-290">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="68bc5-290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="68bc5-291">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="68bc5-291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="68bc5-292">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="68bc5-292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="68bc5-293">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="68bc5-293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="68bc5-294">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="68bc5-294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="68bc5-295">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="68bc5-295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="68bc5-296">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="68bc5-296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="68bc5-297">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="68bc5-297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="68bc5-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="68bc5-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="68bc5-299">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="68bc5-299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="68bc5-300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="68bc5-300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="68bc5-301">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="68bc5-301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="68bc5-302">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="68bc5-302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="68bc5-303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="68bc5-303">Az.FrontDoor</span></span>
* <span data-ttu-id="68bc5-304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="68bc5-304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="68bc5-305">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="68bc5-305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="68bc5-306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="68bc5-306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="68bc5-307">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="68bc5-307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-308">Az.Network</span></span>
* <span data-ttu-id="68bc5-309">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="68bc5-309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="68bc5-310">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-310">New cmdlets</span></span>
        - <span data-ttu-id="68bc5-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="68bc5-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="68bc5-312">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="68bc5-312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="68bc5-313">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-313">New cmdlets</span></span> 
        - <span data-ttu-id="68bc5-314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="68bc5-314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="68bc5-315">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="68bc5-315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="68bc5-316">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-316">New cmdlets</span></span> 
        - <span data-ttu-id="68bc5-317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="68bc5-317">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="68bc5-318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="68bc5-318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="68bc5-319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="68bc5-319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="68bc5-320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="68bc5-320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="68bc5-321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="68bc5-321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="68bc5-322">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="68bc5-322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="68bc5-323">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-323">New cmdlets</span></span>
        - <span data-ttu-id="68bc5-324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="68bc5-324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="68bc5-325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="68bc5-325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="68bc5-326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="68bc5-326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="68bc5-327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="68bc5-327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="68bc5-328">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="68bc5-328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="68bc5-329">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="68bc5-330">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="68bc5-331">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="68bc5-332">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="68bc5-333">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="68bc5-334">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="68bc5-335">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="68bc5-336">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="68bc5-337">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="68bc5-338">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="68bc5-339">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="68bc5-340">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="68bc5-341">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="68bc5-342">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="68bc5-342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="68bc5-343">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="68bc5-344">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="68bc5-345">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="68bc5-345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="68bc5-346">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="68bc5-346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="68bc5-347">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="68bc5-348">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="68bc5-349">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="68bc5-350">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="68bc5-351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="68bc5-351">Az.OperationalInsights</span></span>
* <span data-ttu-id="68bc5-352">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-353">Az.Resources</span></span>
* <span data-ttu-id="68bc5-354">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="68bc5-354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="68bc5-355">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="68bc5-356">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="68bc5-357">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="68bc5-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="68bc5-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="68bc5-359">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-360">Az.Sql</span></span>
* <span data-ttu-id="68bc5-361">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="68bc5-362">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="68bc5-363">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="68bc5-364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="68bc5-364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="68bc5-365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="68bc5-365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="68bc5-366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="68bc5-366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="68bc5-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="68bc5-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="68bc5-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="68bc5-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="68bc5-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="68bc5-369">Az.Storage</span></span>
* <span data-ttu-id="68bc5-370">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="68bc5-370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="68bc5-371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68bc5-371">New-AzStorageAccount</span></span>
* <span data-ttu-id="68bc5-372">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="68bc5-373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="68bc5-373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="68bc5-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="68bc5-374">Az.Websites</span></span>
* <span data-ttu-id="68bc5-375">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="68bc5-375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="68bc5-376">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="68bc5-376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="68bc5-377">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="68bc5-378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="68bc5-378">Az.Cdn</span></span>
* <span data-ttu-id="68bc5-379">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-380">Az.Compute</span></span>
* <span data-ttu-id="68bc5-381">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="68bc5-382">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="68bc5-382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="68bc5-383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="68bc5-383">Az.EventHub</span></span>
* <span data-ttu-id="68bc5-384">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="68bc5-384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="68bc5-385">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="68bc5-385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-386">Az.Network</span></span>
* <span data-ttu-id="68bc5-387">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="68bc5-388">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="68bc5-389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="68bc5-389">Az.PolicyInsights</span></span>
* <span data-ttu-id="68bc5-390">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="68bc5-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="68bc5-392">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="68bc5-393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="68bc5-393">Az.ServiceBus</span></span>
* <span data-ttu-id="68bc5-394">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="68bc5-394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="68bc5-395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="68bc5-395">Az.ServiceFabric</span></span>
* <span data-ttu-id="68bc5-396">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="68bc5-397">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-398">Az.Sql</span></span>
* <span data-ttu-id="68bc5-399">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="68bc5-400">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="68bc5-400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="68bc5-401">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="68bc5-401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="68bc5-402">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="68bc5-403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="68bc5-403">Az.Websites</span></span>
* <span data-ttu-id="68bc5-404">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="68bc5-405">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="68bc5-406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="68bc5-406">Az.ApiManagement</span></span>
* <span data-ttu-id="68bc5-407">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="68bc5-407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="68bc5-408">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="68bc5-408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="68bc5-409">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="68bc5-409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="68bc5-410">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="68bc5-410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="68bc5-411">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="68bc5-411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="68bc5-412">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="68bc5-412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="68bc5-413">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="68bc5-413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="68bc5-414">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="68bc5-414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="68bc5-415">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="68bc5-415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="68bc5-416">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="68bc5-416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="68bc5-417">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="68bc5-417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="68bc5-418">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="68bc5-418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="68bc5-419">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="68bc5-419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="68bc5-420">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="68bc5-420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="68bc5-421">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="68bc5-421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="68bc5-422">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="68bc5-422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="68bc5-423">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="68bc5-423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="68bc5-424">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="68bc5-424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="68bc5-425">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="68bc5-425">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="68bc5-426">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="68bc5-426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="68bc5-427">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="68bc5-427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="68bc5-428">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="68bc5-428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="68bc5-429">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="68bc5-429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="68bc5-430">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="68bc5-431">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="68bc5-432">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="68bc5-433">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="68bc5-433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="68bc5-434">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="68bc5-434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="68bc5-435">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="68bc5-436">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="68bc5-437">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-437">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="68bc5-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="68bc5-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="68bc5-439">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="68bc5-440">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="68bc5-441">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="68bc5-441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="68bc5-442">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="68bc5-442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="68bc5-443">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="68bc5-443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="68bc5-444">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="68bc5-445">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="68bc5-446">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-446">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="68bc5-447">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="68bc5-447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="68bc5-448">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="68bc5-448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="68bc5-449">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="68bc5-449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="68bc5-450">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="68bc5-450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="68bc5-451">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="68bc5-452">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="68bc5-452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="68bc5-453">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="68bc5-453">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="68bc5-454">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="68bc5-454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="68bc5-455">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="68bc5-456">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="68bc5-456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="68bc5-457">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="68bc5-457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="68bc5-458">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="68bc5-458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="68bc5-459">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="68bc5-459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="68bc5-460">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="68bc5-461">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="68bc5-461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="68bc5-462">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="68bc5-462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="68bc5-463">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="68bc5-464">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="68bc5-464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="68bc5-465">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="68bc5-465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="68bc5-466">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="68bc5-467">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="68bc5-468">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="68bc5-468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="68bc5-469">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="68bc5-469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="68bc5-470">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="68bc5-471">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="68bc5-472">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="68bc5-472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="68bc5-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="68bc5-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="68bc5-474">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="68bc5-474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="68bc5-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="68bc5-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="68bc5-476">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="68bc5-476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="68bc5-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="68bc5-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="68bc5-478">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="68bc5-478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="68bc5-479">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="68bc5-479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="68bc5-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="68bc5-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="68bc5-481">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="68bc5-481">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="68bc5-482">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="68bc5-482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="68bc5-483">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="68bc5-483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="68bc5-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="68bc5-484">Az.Automation</span></span>
* <span data-ttu-id="68bc5-485">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="68bc5-486">https://github.com/Azure/azure-powershell/issues/7977 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="68bc5-487">https://github.com/Azure/azure-powershell/issues/8600 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="68bc5-488">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="68bc5-489">https://github.com/Azure/azure-powershell/issues/8347 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="68bc5-490">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="68bc5-491">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="68bc5-491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-492">Az.Compute</span></span>
* <span data-ttu-id="68bc5-493">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="68bc5-494">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="68bc5-494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="68bc5-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="68bc5-495">Az.DataLakeStore</span></span>
* <span data-ttu-id="68bc5-496">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="68bc5-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="68bc5-497">Az.Monitor</span></span>
* <span data-ttu-id="68bc5-498">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-499">Az.Network</span></span>
* <span data-ttu-id="68bc5-500">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="68bc5-501">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="68bc5-501">Updated cmdlet:</span></span>
        - <span data-ttu-id="68bc5-502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="68bc5-502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="68bc5-503">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-504">Az.Resources</span></span>
* <span data-ttu-id="68bc5-505">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-506">Az.Sql</span></span>
* <span data-ttu-id="68bc5-507">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="68bc5-507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="68bc5-508">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="68bc5-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="68bc5-509">Az.Accounts</span></span>
* <span data-ttu-id="68bc5-510">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="68bc5-510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="68bc5-511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-511">Az.CognitiveServices</span></span>
* <span data-ttu-id="68bc5-512">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="68bc5-512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="68bc5-513">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="68bc5-513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-514">Az.Compute</span></span>
* <span data-ttu-id="68bc5-515">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="68bc5-515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="68bc5-516">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="68bc5-516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="68bc5-517">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="68bc5-517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="68bc5-518">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="68bc5-519">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="68bc5-519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="68bc5-520">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="68bc5-521">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="68bc5-521">Breaking changes</span></span>
    - <span data-ttu-id="68bc5-522">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="68bc5-523">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="68bc5-524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="68bc5-524">Az.DeploymentManager</span></span>
* <span data-ttu-id="68bc5-525">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="68bc5-525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="68bc5-526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="68bc5-526">Az.Dns</span></span>
* <span data-ttu-id="68bc5-527">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="68bc5-527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="68bc5-528">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="68bc5-528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="68bc5-529">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="68bc5-529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="68bc5-530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="68bc5-530">Az.FrontDoor</span></span>
* <span data-ttu-id="68bc5-531">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="68bc5-531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="68bc5-532">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="68bc5-532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="68bc5-533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="68bc5-533">Az.HDInsight</span></span>
* <span data-ttu-id="68bc5-534">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="68bc5-534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="68bc5-535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="68bc5-535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="68bc5-536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="68bc5-536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="68bc5-537">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="68bc5-538">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="68bc5-538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="68bc5-539">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="68bc5-539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="68bc5-540">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="68bc5-540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="68bc5-541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="68bc5-541">Az.Monitor</span></span>
* <span data-ttu-id="68bc5-542">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="68bc5-543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="68bc5-543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="68bc5-544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="68bc5-544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="68bc5-545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="68bc5-545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="68bc5-546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="68bc5-546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="68bc5-547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="68bc5-547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="68bc5-548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="68bc5-548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="68bc5-549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="68bc5-549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="68bc5-550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="68bc5-550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="68bc5-551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="68bc5-551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="68bc5-552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="68bc5-552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="68bc5-553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="68bc5-553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="68bc5-554">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="68bc5-554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="68bc5-555">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-556">Az.Network</span></span>
* <span data-ttu-id="68bc5-557">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="68bc5-557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="68bc5-558">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-558">New cmdlets</span></span>
        - <span data-ttu-id="68bc5-559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="68bc5-559">New-AzNatGateway</span></span>
        - <span data-ttu-id="68bc5-560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="68bc5-560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="68bc5-561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="68bc5-561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="68bc5-562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="68bc5-562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="68bc5-563">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-563">Updated cmdlets</span></span>
        - <span data-ttu-id="68bc5-564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="68bc5-564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="68bc5-565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="68bc5-565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="68bc5-566">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="68bc5-566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="68bc5-567">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="68bc5-568">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="68bc5-569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="68bc5-569">Az.PolicyInsights</span></span>
* <span data-ttu-id="68bc5-570">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="68bc5-570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="68bc5-571">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="68bc5-571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="68bc5-572">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="68bc5-572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="68bc5-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="68bc5-574">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="68bc5-574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="68bc5-575">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="68bc5-575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="68bc5-576">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="68bc5-576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="68bc5-577">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="68bc5-577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="68bc5-578">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="68bc5-578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="68bc5-579">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="68bc5-579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="68bc5-580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="68bc5-580">Az.Relay</span></span>
* <span data-ttu-id="68bc5-581">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="68bc5-581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="68bc5-582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="68bc5-582">Az.ServiceBus</span></span>
* <span data-ttu-id="68bc5-583">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="68bc5-584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="68bc5-584">Az.Storage</span></span>
* <span data-ttu-id="68bc5-585">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="68bc5-585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="68bc5-586">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="68bc5-586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="68bc5-587">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="68bc5-587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="68bc5-588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68bc5-588">New-AzStorageAccount</span></span>
* <span data-ttu-id="68bc5-589">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="68bc5-589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="68bc5-590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68bc5-590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="68bc5-591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68bc5-591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="68bc5-592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68bc5-592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="68bc5-593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="68bc5-593">Az.Websites</span></span>
* <span data-ttu-id="68bc5-594">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="68bc5-594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="68bc5-595">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="68bc5-596">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="68bc5-597">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="68bc5-597">Highlights since the last major release</span></span>
* <span data-ttu-id="68bc5-598">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="68bc5-598">General availability of `Az` module</span></span>
* <span data-ttu-id="68bc5-599">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="68bc5-599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="68bc5-600">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="68bc5-600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="68bc5-601">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="68bc5-602">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="68bc5-603">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="68bc5-604">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="68bc5-605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="68bc5-605">Az.Accounts</span></span>
* <span data-ttu-id="68bc5-606">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="68bc5-607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="68bc5-607">Az.Batch</span></span>
* <span data-ttu-id="68bc5-608">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="68bc5-609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="68bc5-609">Az.Cdn</span></span>
* <span data-ttu-id="68bc5-610">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="68bc5-611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-611">Az.CognitiveServices</span></span>
* <span data-ttu-id="68bc5-612">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-613">Az.Compute</span></span>
* <span data-ttu-id="68bc5-614">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="68bc5-615">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="68bc5-616">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="68bc5-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="68bc5-617">Az.DataFactory</span></span>
* <span data-ttu-id="68bc5-618">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="68bc5-619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="68bc5-619">Az.DataLakeStore</span></span>
* <span data-ttu-id="68bc5-620">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="68bc5-621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="68bc5-621">Az.EventGrid</span></span>
* <span data-ttu-id="68bc5-622">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="68bc5-623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="68bc5-623">Az.EventHub</span></span>
* <span data-ttu-id="68bc5-624">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-624">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="68bc5-625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="68bc5-625">Az.HDInsight</span></span>
* <span data-ttu-id="68bc5-626">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="68bc5-627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="68bc5-627">Az.IotHub</span></span>
* <span data-ttu-id="68bc5-628">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="68bc5-629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="68bc5-629">Az.KeyVault</span></span>
* <span data-ttu-id="68bc5-630">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="68bc5-631">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="68bc5-632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="68bc5-632">Az.MachineLearning</span></span>
* <span data-ttu-id="68bc5-633">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="68bc5-634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="68bc5-634">Az.Media</span></span>
* <span data-ttu-id="68bc5-635">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="68bc5-636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="68bc5-636">Az.Monitor</span></span>
  * <span data-ttu-id="68bc5-637">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="68bc5-638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="68bc5-638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="68bc5-639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="68bc5-639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="68bc5-640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="68bc5-640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="68bc5-641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="68bc5-641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="68bc5-642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="68bc5-642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="68bc5-643">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-644">Az.Network</span></span>
* <span data-ttu-id="68bc5-645">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="68bc5-646">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="68bc5-647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="68bc5-647">Az.NotificationHubs</span></span>
* <span data-ttu-id="68bc5-648">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="68bc5-649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="68bc5-649">Az.OperationalInsights</span></span>
* <span data-ttu-id="68bc5-650">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="68bc5-651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="68bc5-651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="68bc5-652">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="68bc5-653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-653">Az.RecoveryServices</span></span>
* <span data-ttu-id="68bc5-654">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="68bc5-655">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="68bc5-655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="68bc5-656">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="68bc5-657">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="68bc5-658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="68bc5-658">Az.RedisCache</span></span>
* <span data-ttu-id="68bc5-659">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-660">Az.Resources</span></span>
* <span data-ttu-id="68bc5-661">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-662">Az.Sql</span></span>
* <span data-ttu-id="68bc5-663">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="68bc5-664">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="68bc5-665">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="68bc5-666">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="68bc5-667">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="68bc5-668">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="68bc5-668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="68bc5-669">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="68bc5-670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="68bc5-670">Az.Websites</span></span>
* <span data-ttu-id="68bc5-671">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="68bc5-672">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="68bc5-673">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="68bc5-674">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="68bc5-675">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="68bc5-676">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="68bc5-676">Highlights since the last major release</span></span>
* <span data-ttu-id="68bc5-677">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="68bc5-677">General availability of `Az` module</span></span>
* <span data-ttu-id="68bc5-678">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="68bc5-678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="68bc5-679">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="68bc5-679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="68bc5-680">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="68bc5-681">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="68bc5-682">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="68bc5-683">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="68bc5-684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="68bc5-684">Az.Accounts</span></span>
* <span data-ttu-id="68bc5-685">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="68bc5-686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-686">Az.AnalysisServices</span></span>
* <span data-ttu-id="68bc5-687">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="68bc5-687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="68bc5-688">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="68bc5-688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="68bc5-689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="68bc5-689">Az.Automation</span></span>
* <span data-ttu-id="68bc5-690">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="68bc5-691">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="68bc5-691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="68bc5-692">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="68bc5-692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-693">Az.Compute</span></span>
* <span data-ttu-id="68bc5-694">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="68bc5-695">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-695">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="68bc5-696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="68bc5-696">Az.ContainerInstance</span></span>
* <span data-ttu-id="68bc5-697">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="68bc5-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="68bc5-698">Az.DataFactory</span></span>
* <span data-ttu-id="68bc5-699">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="68bc5-700">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-701">Az.Resources</span></span>
* <span data-ttu-id="68bc5-702">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="68bc5-703">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="68bc5-704">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="68bc5-705">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="68bc5-705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="68bc5-706">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="68bc5-707">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="68bc5-707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-708">Az.Sql</span></span>
* <span data-ttu-id="68bc5-709">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="68bc5-709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="68bc5-710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="68bc5-710">Az.Storage</span></span>
* <span data-ttu-id="68bc5-711">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="68bc5-711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="68bc5-712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="68bc5-712">New-AzStorageContext</span></span>
* <span data-ttu-id="68bc5-713">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="68bc5-713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="68bc5-714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="68bc5-714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="68bc5-715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="68bc5-715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="68bc5-716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="68bc5-716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="68bc5-717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="68bc5-717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="68bc5-718">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="68bc5-718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="68bc5-719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="68bc5-719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="68bc5-720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="68bc5-720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="68bc5-721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="68bc5-721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="68bc5-722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="68bc5-722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="68bc5-723">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="68bc5-724">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="68bc5-724">Highlights since the last major release</span></span>
* <span data-ttu-id="68bc5-725">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="68bc5-725">General availability of `Az` module</span></span>
* <span data-ttu-id="68bc5-726">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="68bc5-726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="68bc5-727">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="68bc5-727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="68bc5-728">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="68bc5-729">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="68bc5-730">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="68bc5-731">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="68bc5-732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="68bc5-732">Az.Automation</span></span>
* <span data-ttu-id="68bc5-733">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="68bc5-733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="68bc5-734">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="68bc5-734">Dynamic grouping</span></span>
    * <span data-ttu-id="68bc5-735">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="68bc5-735">Pre-Post script</span></span>
    * <span data-ttu-id="68bc5-736">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="68bc5-736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-737">Az.Compute</span></span>
* <span data-ttu-id="68bc5-738">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="68bc5-738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="68bc5-739">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="68bc5-740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="68bc5-740">Az.KeyVault</span></span>
* <span data-ttu-id="68bc5-741">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-742">Az.Network</span></span>
* <span data-ttu-id="68bc5-743">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="68bc5-744">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="68bc5-745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-745">Az.RecoveryServices</span></span>
* <span data-ttu-id="68bc5-746">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="68bc5-747">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-748">Az.Resources</span></span>
* <span data-ttu-id="68bc5-749">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="68bc5-750">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-751">Az.Sql</span></span>
* <span data-ttu-id="68bc5-752">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="68bc5-753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="68bc5-753">Az.Storage</span></span>
* <span data-ttu-id="68bc5-754">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="68bc5-754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="68bc5-755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="68bc5-755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="68bc5-756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="68bc5-756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="68bc5-757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="68bc5-757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="68bc5-758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="68bc5-758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="68bc5-759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="68bc5-759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="68bc5-760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="68bc5-760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="68bc5-761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="68bc5-761">Az.Websites</span></span>
* <span data-ttu-id="68bc5-762">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="68bc5-763">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="68bc5-764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="68bc5-764">Az.Accounts</span></span>
* <span data-ttu-id="68bc5-765">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="68bc5-766">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="68bc5-767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="68bc5-767">Az.Automation</span></span>
* <span data-ttu-id="68bc5-768">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="68bc5-769">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="68bc5-770">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="68bc5-770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="68bc5-771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="68bc5-771">Az.Cdn</span></span>
* <span data-ttu-id="68bc5-772">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="68bc5-772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-773">Az.Compute</span></span>
* <span data-ttu-id="68bc5-774">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="68bc5-775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="68bc5-775">Az.DataFactory</span></span>
* <span data-ttu-id="68bc5-776">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="68bc5-777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="68bc5-777">Az.LogicApp</span></span>
* <span data-ttu-id="68bc5-778">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="68bc5-778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-779">Az.Network</span></span>
* <span data-ttu-id="68bc5-780">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="68bc5-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="68bc5-782">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="68bc5-783">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="68bc5-783">SDK Update</span></span>
* <span data-ttu-id="68bc5-784">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="68bc5-784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="68bc5-785">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-786">Az.Resources</span></span>
* <span data-ttu-id="68bc5-787">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="68bc5-788">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="68bc5-788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="68bc5-789">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="68bc5-790">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="68bc5-790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="68bc5-791">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="68bc5-792">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="68bc5-792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-793">Az.Sql</span></span>
* <span data-ttu-id="68bc5-794">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="68bc5-794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="68bc5-795">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="68bc5-795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="68bc5-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="68bc5-796">Az.Storage</span></span>
* <span data-ttu-id="68bc5-797">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68bc5-797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="68bc5-798">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="68bc5-799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-799">Az.AnalysisServices</span></span>
* <span data-ttu-id="68bc5-800">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="68bc5-800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="68bc5-801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="68bc5-801">Az.Automation</span></span>
* <span data-ttu-id="68bc5-802">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="68bc5-803">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="68bc5-804">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="68bc5-805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-805">Az.CognitiveServices</span></span>
* <span data-ttu-id="68bc5-806">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-807">Az.Compute</span></span>
* <span data-ttu-id="68bc5-808">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="68bc5-809">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="68bc5-810">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="68bc5-811">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="68bc5-811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="68bc5-812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="68bc5-812">Az.DataLakeStore</span></span>
* <span data-ttu-id="68bc5-813">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="68bc5-814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="68bc5-814">Az.EventHub</span></span>
* <span data-ttu-id="68bc5-815">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="68bc5-816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="68bc5-816">Az.KeyVault</span></span>
* <span data-ttu-id="68bc5-817">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="68bc5-818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="68bc5-818">Az.LogicApp</span></span>
* <span data-ttu-id="68bc5-819">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="68bc5-820">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="68bc5-821">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="68bc5-822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="68bc5-822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="68bc5-823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="68bc5-823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="68bc5-824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="68bc5-824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="68bc5-825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="68bc5-825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="68bc5-826">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="68bc5-826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="68bc5-827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="68bc5-827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="68bc5-828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="68bc5-828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="68bc5-829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="68bc5-829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="68bc5-830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="68bc5-830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="68bc5-831">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="68bc5-832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="68bc5-832">Az.Monitor</span></span>
* <span data-ttu-id="68bc5-833">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-834">Az.Network</span></span>
* <span data-ttu-id="68bc5-835">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="68bc5-836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="68bc5-836">Az.OperationalInsights</span></span>
* <span data-ttu-id="68bc5-837">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="68bc5-837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="68bc5-838">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="68bc5-839">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="68bc5-840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-840">Az.Resources</span></span>
* <span data-ttu-id="68bc5-841">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="68bc5-842">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="68bc5-843">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="68bc5-844">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-845">Az.Sql</span></span>
* <span data-ttu-id="68bc5-846">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="68bc5-847">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="68bc5-848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="68bc5-848">Az.Websites</span></span>
* <span data-ttu-id="68bc5-849">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="68bc5-850">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="68bc5-851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="68bc5-851">Az.Accounts</span></span>
* <span data-ttu-id="68bc5-852">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="68bc5-852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="68bc5-853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-853">Az.AnalysisServices</span></span>
<span data-ttu-id="68bc5-854">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="68bc5-854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-855">Az.Compute</span></span>
* <span data-ttu-id="68bc5-856">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="68bc5-857">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="68bc5-858">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="68bc5-859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-859">Az.RecoveryServices</span></span>
<span data-ttu-id="68bc5-860">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="68bc5-860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-861">Az.Resources</span></span>
* <span data-ttu-id="68bc5-862">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-862">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="68bc5-863">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="68bc5-863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="68bc5-864">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="68bc5-865">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="68bc5-865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-866">Az.Sql</span></span>
* <span data-ttu-id="68bc5-867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="68bc5-867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="68bc5-868">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="68bc5-869">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="68bc5-870">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="68bc5-871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="68bc5-871">Az.Accounts</span></span>
* <span data-ttu-id="68bc5-872">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="68bc5-872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="68bc5-873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-873">Az.AnalysisServices</span></span>
* <span data-ttu-id="68bc5-874">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="68bc5-874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="68bc5-875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-875">Az.RecoveryServices</span></span>
* <span data-ttu-id="68bc5-876">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="68bc5-876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="68bc5-877">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="68bc5-878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="68bc5-878">Az.Accounts</span></span>
* <span data-ttu-id="68bc5-879">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="68bc5-880">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="68bc5-881">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="68bc5-882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="68bc5-882">Az.Aks</span></span>
* <span data-ttu-id="68bc5-883">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="68bc5-884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="68bc5-884">Az.Automation</span></span>
* <span data-ttu-id="68bc5-885">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="68bc5-886">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="68bc5-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="68bc5-887">Az.Cdn</span></span>
* <span data-ttu-id="68bc5-888">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-889">Az.Compute</span></span>
* <span data-ttu-id="68bc5-890">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="68bc5-891">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="68bc5-892">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="68bc5-893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="68bc5-893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="68bc5-894">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="68bc5-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="68bc5-895">Az.DataFactory</span></span>
* <span data-ttu-id="68bc5-896">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="68bc5-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="68bc5-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="68bc5-898">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="68bc5-899">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="68bc5-899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="68bc5-900">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="68bc5-901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="68bc5-901">Az.IotHub</span></span>
* <span data-ttu-id="68bc5-902">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="68bc5-903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="68bc5-903">Az.KeyVault</span></span>
* <span data-ttu-id="68bc5-904">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-905">Az.Network</span></span>
* <span data-ttu-id="68bc5-906">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-907">Az.Resources</span></span>
* <span data-ttu-id="68bc5-908">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="68bc5-909">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="68bc5-910">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="68bc5-911">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="68bc5-912">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="68bc5-913">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="68bc5-914">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="68bc5-914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="68bc5-915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="68bc5-915">Az.ServiceFabric</span></span>
* <span data-ttu-id="68bc5-916">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="68bc5-916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="68bc5-917">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-917">Fix some error messages.</span></span>
* <span data-ttu-id="68bc5-918">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="68bc5-919">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="68bc5-920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="68bc5-920">Az.SignalR</span></span>
* <span data-ttu-id="68bc5-921">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-922">Az.Sql</span></span>
* <span data-ttu-id="68bc5-923">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="68bc5-924">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="68bc5-925">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="68bc5-926">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="68bc5-926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="68bc5-927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="68bc5-927">Az.Storage</span></span>
* <span data-ttu-id="68bc5-928">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="68bc5-929">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="68bc5-929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="68bc5-930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="68bc5-930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="68bc5-931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="68bc5-931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="68bc5-932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="68bc5-932">Az.TrafficManager</span></span>
* <span data-ttu-id="68bc5-933">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="68bc5-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="68bc5-934">Az.Websites</span></span>
* <span data-ttu-id="68bc5-935">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="68bc5-936">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="68bc5-937">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="68bc5-938">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="68bc5-938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="68bc5-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="68bc5-939">Az.Accounts</span></span>
* <span data-ttu-id="68bc5-940">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-941">Az.Compute</span></span>
* <span data-ttu-id="68bc5-942">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="68bc5-942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="68bc5-943">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="68bc5-944">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="68bc5-944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="68bc5-945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="68bc5-945">Az.DataLakeStore</span></span>
* <span data-ttu-id="68bc5-946">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="68bc5-947">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="68bc5-948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="68bc5-948">Az.EventGrid</span></span>
* <span data-ttu-id="68bc5-949">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="68bc5-950">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="68bc5-951">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="68bc5-951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="68bc5-952">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="68bc5-952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="68bc5-953">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="68bc5-953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="68bc5-954">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="68bc5-954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="68bc5-955">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="68bc5-955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="68bc5-956">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="68bc5-956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="68bc5-957">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="68bc5-957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="68bc5-958">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="68bc5-958">Dead letter endpoint.</span></span>
* <span data-ttu-id="68bc5-959">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="68bc5-960">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="68bc5-960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="68bc5-961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="68bc5-961">Az.IotHub</span></span>
* <span data-ttu-id="68bc5-962">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="68bc5-963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="68bc5-963">Az.LogicApp</span></span>
* <span data-ttu-id="68bc5-964">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="68bc5-964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-965">Az.Resources</span></span>
* <span data-ttu-id="68bc5-966">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="68bc5-967">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="68bc5-967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="68bc5-968">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="68bc5-969">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="68bc5-970">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="68bc5-971">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="68bc5-971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="68bc5-972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="68bc5-972">Az.SignalR</span></span>
* <span data-ttu-id="68bc5-973">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="68bc5-973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-974">Az.Sql</span></span>
* <span data-ttu-id="68bc5-975">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="68bc5-975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="68bc5-976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="68bc5-976">Az.Storage</span></span>
* <span data-ttu-id="68bc5-977">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="68bc5-977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="68bc5-978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="68bc5-978">New-AzStorageContext</span></span>
* <span data-ttu-id="68bc5-979">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="68bc5-980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="68bc5-980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="68bc5-981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="68bc5-981">Az.Websites</span></span>
* <span data-ttu-id="68bc5-982">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="68bc5-983">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="68bc5-983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="68bc5-984">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="68bc5-984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="68bc5-985">Genel</span><span class="sxs-lookup"><span data-stu-id="68bc5-985">General</span></span>

- <span data-ttu-id="68bc5-986">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="68bc5-986">General Availability of Az Module</span></span>
- <span data-ttu-id="68bc5-987">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="68bc5-987">Online help for each module</span></span>
- <span data-ttu-id="68bc5-988">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="68bc5-988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="68bc5-989">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="68bc5-990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="68bc5-990">Az.Accounts</span></span>
- <span data-ttu-id="68bc5-991">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="68bc5-991">Changed from Az.Profile</span></span>
- <span data-ttu-id="68bc5-992">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="68bc5-993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="68bc5-993">Az.ApiManagement</span></span>
- <span data-ttu-id="68bc5-994">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="68bc5-994">Fixes for #7002</span></span>
- <span data-ttu-id="68bc5-995">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="68bc5-996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="68bc5-996">Az.Batch</span></span>
- <span data-ttu-id="68bc5-997">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="68bc5-998">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="68bc5-998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="68bc5-999">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="68bc5-1000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="68bc5-1000">Az.Billing</span></span>
- <span data-ttu-id="68bc5-1001">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-1001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="68bc5-1002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-1002">Az.CognitivServices</span></span>
- <span data-ttu-id="68bc5-1003">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="68bc5-1004">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="68bc5-1004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="68bc5-1005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="68bc5-1005">Az.ContainerInstance</span></span>
- <span data-ttu-id="68bc5-1006">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="68bc5-1007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="68bc5-1007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="68bc5-1008">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-1008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="68bc5-1009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="68bc5-1009">Az.DataLakeStore</span></span>
- <span data-ttu-id="68bc5-1010">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-1010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="68bc5-1011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="68bc5-1011">Az.Monitor</span></span>
- <span data-ttu-id="68bc5-1012">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-1012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="68bc5-1013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="68bc5-1013">Az.KeyVault</span></span>
- <span data-ttu-id="68bc5-1014">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="68bc5-1014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="68bc5-1015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="68bc5-1015">Az.MachineLearning</span></span>
- <span data-ttu-id="68bc5-1016">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="68bc5-1017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="68bc5-1017">Az.Media</span></span>
- <span data-ttu-id="68bc5-1018">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="68bc5-1018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="68bc5-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-1019">Az.Network</span></span>
<span data-ttu-id="68bc5-1020">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="68bc5-1021">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="68bc5-1021">New cmdlets added:</span></span>
        - <span data-ttu-id="68bc5-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="68bc5-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="68bc5-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="68bc5-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="68bc5-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="68bc5-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="68bc5-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="68bc5-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="68bc5-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="68bc5-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="68bc5-1027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="68bc5-1027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="68bc5-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="68bc5-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="68bc5-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="68bc5-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="68bc5-1030">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="68bc5-1031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68bc5-1031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="68bc5-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="68bc5-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="68bc5-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="68bc5-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="68bc5-1034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="68bc5-1034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="68bc5-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="68bc5-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="68bc5-1036">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="68bc5-1037">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="68bc5-1038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="68bc5-1038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="68bc5-1039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="68bc5-1039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="68bc5-1040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="68bc5-1040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="68bc5-1041">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="68bc5-1042">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-1042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="68bc5-1043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="68bc5-1043">Az.OperationalInsights</span></span>
- <span data-ttu-id="68bc5-1044">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-1044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="68bc5-1045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="68bc5-1045">Az.Profile</span></span>
- <span data-ttu-id="68bc5-1046">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="68bc5-1047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-1047">Az.RecoveryServices</span></span>
- <span data-ttu-id="68bc5-1048">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-1048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="68bc5-1049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-1049">Az.Resources</span></span>
- <span data-ttu-id="68bc5-1050">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-1050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="68bc5-1051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="68bc5-1051">Az.ServiceFabric</span></span>
- <span data-ttu-id="68bc5-1052">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="68bc5-1052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="68bc5-1053">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-1053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="68bc5-1054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="68bc5-1054">Az.SIgnalR</span></span>
- <span data-ttu-id="68bc5-1055">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="68bc5-1055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="68bc5-1056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-1056">Az.Sql</span></span>
- <span data-ttu-id="68bc5-1057">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="68bc5-1058">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="68bc5-1059">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-1059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="68bc5-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="68bc5-1060">Az.Storage</span></span>
- <span data-ttu-id="68bc5-1061">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-1061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="68bc5-1062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="68bc5-1062">Az.Websites</span></span>
- <span data-ttu-id="68bc5-1063">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="68bc5-1063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="68bc5-1064">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="68bc5-1064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="68bc5-1065">Genel</span><span class="sxs-lookup"><span data-stu-id="68bc5-1065">General</span></span>

* <span data-ttu-id="68bc5-1066">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="68bc5-1066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="68bc5-1067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-1067">Az.Compute</span></span>

* <span data-ttu-id="68bc5-1068">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="68bc5-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="68bc5-1069">Az.DataLakeStore</span></span>

* <span data-ttu-id="68bc5-1070">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="68bc5-1071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="68bc5-1071">Az.FrontDoor</span></span>

* <span data-ttu-id="68bc5-1072">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1072">Fixed some broken links</span></span>
    - <span data-ttu-id="68bc5-1073">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="68bc5-1074">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="68bc5-1075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-1075">Az.RecoveryServices</span></span>

* <span data-ttu-id="68bc5-1076">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="68bc5-1077">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="68bc5-1078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-1078">Az.Resources</span></span>

* <span data-ttu-id="68bc5-1079">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="68bc5-1080">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="68bc5-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-1081">Az.Sql</span></span>

* <span data-ttu-id="68bc5-1082">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="68bc5-1082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="68bc5-1083">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="68bc5-1084">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="68bc5-1085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="68bc5-1085">Az.Storage</span></span>

* <span data-ttu-id="68bc5-1086">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="68bc5-1087">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="68bc5-1088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="68bc5-1088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="68bc5-1089">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1089">Support Static Website configuration</span></span>
    - <span data-ttu-id="68bc5-1090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="68bc5-1090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="68bc5-1091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="68bc5-1091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="68bc5-1092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="68bc5-1092">Az.Websites</span></span>

* <span data-ttu-id="68bc5-1093">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="68bc5-1093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="68bc5-1094">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="68bc5-1095">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="68bc5-1096">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="68bc5-1096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="68bc5-1097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="68bc5-1097">Az.ApiManagement</span></span>
* <span data-ttu-id="68bc5-1098">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="68bc5-1098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="68bc5-1099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="68bc5-1099">Az.Automation</span></span>
* <span data-ttu-id="68bc5-1100">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="68bc5-1100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="68bc5-1101">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="68bc5-1102">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="68bc5-1103">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="68bc5-1104">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="68bc5-1105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-1105">Az.Compute</span></span>
* <span data-ttu-id="68bc5-1106">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="68bc5-1107">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="68bc5-1107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="68bc5-1108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="68bc5-1108">Az.ContainerInstance</span></span>
* <span data-ttu-id="68bc5-1109">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="68bc5-1109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="68bc5-1110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="68bc5-1110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="68bc5-1111">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="68bc5-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-1112">Az.Network</span></span>
* <span data-ttu-id="68bc5-1113">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="68bc5-1114">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="68bc5-1115">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="68bc5-1116">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="68bc5-1117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="68bc5-1117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="68bc5-1118">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="68bc5-1119">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="68bc5-1120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="68bc5-1120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="68bc5-1121">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="68bc5-1122">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="68bc5-1122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="68bc5-1123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="68bc5-1123">Az.Relay</span></span>
* <span data-ttu-id="68bc5-1124">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="68bc5-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-1125">Az.Resources</span></span>
* <span data-ttu-id="68bc5-1126">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="68bc5-1127">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="68bc5-1128">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="68bc5-1128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="68bc5-1129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="68bc5-1129">Az.ServiceFabric</span></span>
* <span data-ttu-id="68bc5-1130">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="68bc5-1131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-1131">Az.Sql</span></span>
* <span data-ttu-id="68bc5-1132">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="68bc5-1133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="68bc5-1133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="68bc5-1134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="68bc5-1134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="68bc5-1135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="68bc5-1135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="68bc5-1136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="68bc5-1136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="68bc5-1137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="68bc5-1137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="68bc5-1138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="68bc5-1138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="68bc5-1139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="68bc5-1139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="68bc5-1140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="68bc5-1140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="68bc5-1141">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="68bc5-1142">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="68bc5-1143">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="68bc5-1144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="68bc5-1145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="68bc5-1146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="68bc5-1147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="68bc5-1148">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="68bc5-1149">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="68bc5-1149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="68bc5-1150">Genel</span><span class="sxs-lookup"><span data-stu-id="68bc5-1150">General</span></span>
* <span data-ttu-id="68bc5-1151">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="68bc5-1151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="68bc5-1152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="68bc5-1152">Az.Profile</span></span>
* <span data-ttu-id="68bc5-1153">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="68bc5-1154">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="68bc5-1155">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="68bc5-1156">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="68bc5-1157">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="68bc5-1158">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="68bc5-1159">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="68bc5-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="68bc5-1161">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-1162">Az.Compute</span></span>
* <span data-ttu-id="68bc5-1163">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="68bc5-1164">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="68bc5-1164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="68bc5-1165">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="68bc5-1166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="68bc5-1166">Az.DataLakeStore</span></span>
* <span data-ttu-id="68bc5-1167">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="68bc5-1168">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="68bc5-1169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="68bc5-1169">Az.Insights</span></span>
* <span data-ttu-id="68bc5-1170">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="68bc5-1171">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="68bc5-1171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="68bc5-1172">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="68bc5-1173">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="68bc5-1173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-1174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-1174">Az.Network</span></span>
* <span data-ttu-id="68bc5-1175">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="68bc5-1175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="68bc5-1176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="68bc5-1176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="68bc5-1177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="68bc5-1177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="68bc5-1178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="68bc5-1178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="68bc5-1179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="68bc5-1179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="68bc5-1180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="68bc5-1180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="68bc5-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="68bc5-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="68bc5-1182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="68bc5-1182">Az.PolicyInsights</span></span>
* <span data-ttu-id="68bc5-1183">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-1184">Az.Resources</span></span>
* <span data-ttu-id="68bc5-1185">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="68bc5-1186">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="68bc5-1186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="68bc5-1187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="68bc5-1187">Az.ServiceBus</span></span>
* <span data-ttu-id="68bc5-1188">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="68bc5-1189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="68bc5-1189">Az.ServiceFabric</span></span>
* <span data-ttu-id="68bc5-1190">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="68bc5-1191">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="68bc5-1192">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="68bc5-1192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="68bc5-1193">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="68bc5-1193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="68bc5-1194">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="68bc5-1195">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="68bc5-1195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="68bc5-1196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="68bc5-1196">Az.Profile</span></span>
* <span data-ttu-id="68bc5-1197">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="68bc5-1197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="68bc5-1198">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-1199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-1199">Az.Compute</span></span>
* <span data-ttu-id="68bc5-1200">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="68bc5-1201">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="68bc5-1202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="68bc5-1202">Az.DataLakeStore</span></span>
* <span data-ttu-id="68bc5-1203">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="68bc5-1203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="68bc5-1204">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="68bc5-1205">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="68bc5-1206">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="68bc5-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-1208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-1208">Az.Network</span></span>
* <span data-ttu-id="68bc5-1209">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="68bc5-1210">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-1211">Az.Resources</span></span>
* <span data-ttu-id="68bc5-1212">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="68bc5-1213">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="68bc5-1214">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="68bc5-1214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="68bc5-1215">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="68bc5-1215">Azure.Storage</span></span>
* <span data-ttu-id="68bc5-1216">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="68bc5-1216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="68bc5-1217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="68bc5-1217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="68bc5-1218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="68bc5-1218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="68bc5-1219">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="68bc5-1220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="68bc5-1220">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="68bc5-1221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="68bc5-1221">Az.CognitiveServices</span></span>
* <span data-ttu-id="68bc5-1222">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="68bc5-1223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="68bc5-1223">Az.Compute</span></span>
* <span data-ttu-id="68bc5-1224">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="68bc5-1225">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="68bc5-1226">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="68bc5-1227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="68bc5-1227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="68bc5-1228">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="68bc5-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="68bc5-1229">Az.Network</span></span>
* <span data-ttu-id="68bc5-1230">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="68bc5-1231">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1231">new cmdlets added</span></span>
    - <span data-ttu-id="68bc5-1232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="68bc5-1232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="68bc5-1233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="68bc5-1233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="68bc5-1234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="68bc5-1234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="68bc5-1235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="68bc5-1235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="68bc5-1236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="68bc5-1236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="68bc5-1237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="68bc5-1237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="68bc5-1238">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="68bc5-1239">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="68bc5-1240">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="68bc5-1241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="68bc5-1241">Az.RedisCache</span></span>
* <span data-ttu-id="68bc5-1242">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="68bc5-1242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="68bc5-1243">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="68bc5-1244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="68bc5-1244">Az.Resources</span></span>
* <span data-ttu-id="68bc5-1245">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="68bc5-1246">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="68bc5-1247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="68bc5-1247">Az.Sql</span></span>
* <span data-ttu-id="68bc5-1248">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="68bc5-1248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="68bc5-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="68bc5-1249">Az.Websites</span></span>
* <span data-ttu-id="68bc5-1250">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="68bc5-1250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="68bc5-1251">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="68bc5-1251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="68bc5-1252">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="68bc5-1252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="68bc5-1253">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="68bc5-1253">Initial Release</span></span>