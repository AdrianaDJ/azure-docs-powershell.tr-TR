---
ms.openlocfilehash: 96e6d7bc0cc29adc1c0e49ba344d27349454c214
ms.sourcegitcommit: 92722d603b60dc769660e7517da60110133d9959
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71226448"
---
## <a name="270---september-2019"></a><span data-ttu-id="75345-101">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="75345-101">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="75345-102">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="75345-102">Az.ApiManagement</span></span>
* <span data-ttu-id="75345-103">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-103">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="75345-104">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-104">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="75345-105">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="75345-105">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="75345-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="75345-106">Az.Automation</span></span>
* <span data-ttu-id="75345-107">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-107">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="75345-108">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-108">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="75345-109">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-109">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-110">Az.Compute</span></span>
* <span data-ttu-id="75345-111">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-111">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="75345-112">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-112">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="75345-113">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="75345-113">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="75345-114">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-114">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="75345-115">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-115">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="75345-116">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-116">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="75345-117">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-117">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="75345-118">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-118">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="75345-119">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-119">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="75345-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="75345-120">Az.DataFactory</span></span>
* <span data-ttu-id="75345-121">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="75345-121">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="75345-122">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-122">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="75345-123">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="75345-123">Az.HDInsight</span></span>
* <span data-ttu-id="75345-124">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="75345-124">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="75345-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="75345-125">Az.IotHub</span></span>
* <span data-ttu-id="75345-126">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-126">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="75345-127">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-127">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="75345-128">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="75345-128">New cmdlets are:</span></span>
    - <span data-ttu-id="75345-129">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="75345-129">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="75345-130">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="75345-130">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="75345-131">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="75345-131">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="75345-132">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="75345-132">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="75345-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="75345-133">Az.Monitor</span></span>
* <span data-ttu-id="75345-134">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="75345-134">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="75345-135">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="75345-135">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="75345-136">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="75345-136">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="75345-137">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="75345-137">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="75345-138">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-138">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="75345-139">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-139">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="75345-140">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="75345-140">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="75345-141">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="75345-141">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="75345-142">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-142">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="75345-143">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="75345-143">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="75345-144">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-144">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="75345-145">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="75345-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="75345-146">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-146">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="75345-147">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="75345-147">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="75345-148">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="75345-148">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="75345-149">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="75345-149">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="75345-150">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="75345-150">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="75345-151">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="75345-151">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="75345-152">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-152">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="75345-153">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-153">Overall improved help files</span></span>
* <span data-ttu-id="75345-154">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-154">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-155">Az.Network</span></span>
* <span data-ttu-id="75345-156">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-156">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="75345-157">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-157">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="75345-158">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-158">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="75345-159">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-159">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="75345-160">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-160">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="75345-161">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-161">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="75345-162">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-162">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="75345-163">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-163">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="75345-164">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-164">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="75345-165">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-165">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="75345-166">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-166">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="75345-167">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="75345-167">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="75345-168">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-168">New cmdlets</span></span>
        - <span data-ttu-id="75345-169">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="75345-169">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="75345-170">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="75345-170">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="75345-171">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="75345-171">Updated cmdlet:</span></span>
        - <span data-ttu-id="75345-172">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="75345-172">New-VpnSite</span></span>
        - <span data-ttu-id="75345-173">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="75345-173">Update-VpnSite</span></span>
        - <span data-ttu-id="75345-174">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="75345-174">New-VpnConnection</span></span>
        - <span data-ttu-id="75345-175">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="75345-175">Update-VpnConnection</span></span>
* <span data-ttu-id="75345-176">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-176">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="75345-177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-177">Az.RecoveryServices</span></span>
* <span data-ttu-id="75345-178">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-178">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="75345-179">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-179">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-180">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-180">Az.Resources</span></span>
* <span data-ttu-id="75345-181">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-181">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="75345-182">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="75345-182">Az.ServiceFabric</span></span>
* <span data-ttu-id="75345-183">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-183">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="75345-184">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="75345-184">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="75345-185">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="75345-185">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="75345-186">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="75345-186">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="75345-187">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="75345-187">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="75345-188">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="75345-188">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="75345-189">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="75345-189">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="75345-190">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="75345-190">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="75345-191">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="75345-191">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="75345-192">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="75345-192">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="75345-193">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="75345-193">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="75345-194">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="75345-194">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="75345-195">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="75345-195">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="75345-196">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="75345-196">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="75345-197">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="75345-197">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="75345-198">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-198">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="75345-199">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="75345-199">Az.SignalR</span></span>
* <span data-ttu-id="75345-200">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-200">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-201">Az.Sql</span></span>
* <span data-ttu-id="75345-202">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-202">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="75345-203">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-203">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="75345-204">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="75345-204">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="75345-205">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-205">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="75345-206">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-206">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="75345-207">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-207">Az.Storage</span></span>
* <span data-ttu-id="75345-208">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-208">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="75345-209">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-209">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="75345-210">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="75345-210">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="75345-211">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="75345-211">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="75345-212">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-212">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="75345-213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="75345-213">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="75345-214">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-214">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="75345-215">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="75345-215">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="75345-216">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="75345-216">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="75345-217">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="75345-217">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="75345-218">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="75345-218">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="75345-219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-219">Az.Websites</span></span>
* <span data-ttu-id="75345-220">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="75345-220">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="75345-221">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="75345-221">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="75345-222">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-222">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="75345-223">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="75345-223">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="75345-224">Genel</span><span class="sxs-lookup"><span data-stu-id="75345-224">General</span></span>
* <span data-ttu-id="75345-225">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-225">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="75345-226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-226">Az.Accounts</span></span>
* <span data-ttu-id="75345-227">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="75345-227">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="75345-228">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="75345-228">Az.Aks</span></span>
* <span data-ttu-id="75345-229">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-229">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="75345-230">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="75345-230">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="75345-231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="75345-231">Az.ApiManagement</span></span>
* <span data-ttu-id="75345-232">https://github.com/Azure/azure-powershell/issues/9351 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-232">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="75345-233">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-233">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="75345-234">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-234">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="75345-235">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="75345-235">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="75345-236">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-236">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="75345-237">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="75345-237">Az.Batch</span></span>
* <span data-ttu-id="75345-238">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-238">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="75345-239">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="75345-239">Az.Cdn</span></span>
* <span data-ttu-id="75345-240">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-240">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-241">Az.Compute</span></span>
* <span data-ttu-id="75345-242">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-242">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="75345-243">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-243">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="75345-244">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-244">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="75345-245">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-245">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="75345-246">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="75345-246">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="75345-247">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-247">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="75345-248">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-248">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="75345-249">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-249">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="75345-250">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="75345-250">Az.DataFactory</span></span>
* <span data-ttu-id="75345-251">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-251">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="75345-252">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-252">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="75345-253">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-253">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="75345-254">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-254">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="75345-255">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="75345-255">Az.DataLakeStore</span></span>
* <span data-ttu-id="75345-256">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-256">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="75345-257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="75345-257">Az.EventHub</span></span>
* <span data-ttu-id="75345-258">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="75345-258">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="75345-259">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="75345-259">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="75345-260">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-260">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="75345-261">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="75345-261">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="75345-262">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="75345-262">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="75345-263">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-263">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="75345-264">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="75345-264">Az.Monitor</span></span>
* <span data-ttu-id="75345-265">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-265">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-266">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-266">Az.Network</span></span>
* <span data-ttu-id="75345-267">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-267">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="75345-268">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-268">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="75345-269">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-269">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="75345-270">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="75345-270">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="75345-271">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="75345-271">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="75345-272">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-272">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="75345-273">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-273">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="75345-274">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="75345-274">Az.OperationalInsights</span></span>
* <span data-ttu-id="75345-275">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-275">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="75345-276">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-276">Added example</span></span>
    - <span data-ttu-id="75345-277">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-277">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="75345-278">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-278">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="75345-279">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-279">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="75345-280">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-280">Az.RecoveryServices</span></span>
* <span data-ttu-id="75345-281">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-281">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-282">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-282">Az.Resources</span></span>
* <span data-ttu-id="75345-283">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-283">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="75345-284">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-284">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="75345-285">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="75345-285">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="75345-286">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-286">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="75345-287">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="75345-287">Az.ServiceBus</span></span>
* <span data-ttu-id="75345-288">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="75345-288">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="75345-289">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="75345-289">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="75345-290">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-290">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="75345-291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="75345-291">Az.ServiceFabric</span></span>
* <span data-ttu-id="75345-292">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="75345-292">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="75345-293">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="75345-293">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="75345-294">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="75345-294">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="75345-295">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-295">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="75345-296">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="75345-296">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="75345-297">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="75345-297">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-298">Az.Sql</span></span>
* <span data-ttu-id="75345-299">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-299">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="75345-300">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-300">Az.Storage</span></span>
* <span data-ttu-id="75345-301">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-301">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="75345-302">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="75345-302">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="75345-303">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="75345-303">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="75345-304">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="75345-304">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="75345-305">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="75345-305">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="75345-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="75345-306">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="75345-307">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-307">Az.Websites</span></span>
* <span data-ttu-id="75345-308">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-308">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="75345-309">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="75345-309">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="75345-310">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-310">Az.Accounts</span></span>
* <span data-ttu-id="75345-311">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-311">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="75345-312">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="75345-312">Az.ApplicationInsights</span></span>
* <span data-ttu-id="75345-313">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-313">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="75345-314">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="75345-314">Az.Automation</span></span>
* <span data-ttu-id="75345-315">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-315">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="75345-316">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="75345-316">Az.CognitiveServices</span></span>
* <span data-ttu-id="75345-317">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-317">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-318">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-318">Az.Compute</span></span>
* <span data-ttu-id="75345-319">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-319">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="75345-320">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="75345-320">Az.ContainerRegistry</span></span>
* <span data-ttu-id="75345-321">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-321">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="75345-322">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="75345-322">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="75345-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="75345-323">Az.DataFactory</span></span>
* <span data-ttu-id="75345-324">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-324">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="75345-325">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-325">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="75345-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="75345-326">Az.EventHub</span></span>
* <span data-ttu-id="75345-327">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="75345-327">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="75345-328">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-328">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="75345-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="75345-329">Az.KeyVault</span></span>
* <span data-ttu-id="75345-330">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-330">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="75345-331">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="75345-331">Az.LogicApp</span></span>
* <span data-ttu-id="75345-332">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="75345-332">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="75345-333">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-333">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="75345-334">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="75345-334">Az.ManagedServices</span></span>
* <span data-ttu-id="75345-335">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="75345-335">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-336">Az.Network</span></span>
* <span data-ttu-id="75345-337">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-337">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="75345-338">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-338">New cmdlets</span></span>
        - <span data-ttu-id="75345-339">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="75345-339">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="75345-340">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="75345-340">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="75345-341">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="75345-341">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="75345-342">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="75345-342">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="75345-343">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="75345-343">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="75345-344">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="75345-344">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="75345-345">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="75345-345">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="75345-346">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="75345-346">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="75345-347">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="75345-347">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="75345-348">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-348">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="75345-349">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-349">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="75345-350">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-350">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="75345-351">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="75345-351">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="75345-352">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-352">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="75345-353">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-353">Updated cmdlets</span></span>
        - <span data-ttu-id="75345-354">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75345-354">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="75345-355">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75345-355">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="75345-356">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75345-356">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="75345-357">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-357">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="75345-358">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-358">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="75345-359">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="75345-359">Updated cmdlet:</span></span>
        - <span data-ttu-id="75345-360">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="75345-360">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="75345-361">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="75345-361">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="75345-362">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="75345-362">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="75345-363">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-363">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="75345-364">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-364">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="75345-365">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="75345-365">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="75345-366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="75345-366">Az.OperationalInsights</span></span>
* <span data-ttu-id="75345-367">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-367">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="75345-368">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-368">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="75345-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="75345-370">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-370">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="75345-371">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-371">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="75345-372">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-372">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="75345-373">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-373">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="75345-374">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-374">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="75345-375">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-375">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="75345-376">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-376">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="75345-377">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-377">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="75345-378">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-378">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="75345-379">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-379">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-380">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-380">Az.Resources</span></span>
- <span data-ttu-id="75345-381">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="75345-381">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="75345-382">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-382">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="75345-383">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="75345-383">Az.ServiceBus</span></span>
* <span data-ttu-id="75345-384">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="75345-384">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="75345-385">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-385">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-386">Az.Sql</span></span>
* <span data-ttu-id="75345-387">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-387">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="75345-388">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-388">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="75345-389">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-389">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="75345-390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-390">Az.Storage</span></span>
* <span data-ttu-id="75345-391">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-391">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="75345-392">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="75345-392">Az.StorageSync</span></span>
* <span data-ttu-id="75345-393">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="75345-393">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="75345-394">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-394">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="75345-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-395">Az.Websites</span></span>
* <span data-ttu-id="75345-396">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-396">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="75345-397">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-397">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="75345-398">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-398">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="75345-399">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="75345-399">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="75345-400">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-400">Az.Accounts</span></span>
* <span data-ttu-id="75345-401">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-401">Add support for profile cmdlets</span></span>
* <span data-ttu-id="75345-402">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-402">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="75345-403">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-403">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="75345-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="75345-404">Az.Advisor</span></span>
* <span data-ttu-id="75345-405">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="75345-405">GA release of Az.Advisor</span></span>
* <span data-ttu-id="75345-406">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="75345-406">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="75345-407">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="75345-407">Az.ApiManagement</span></span>
* <span data-ttu-id="75345-408">https://github.com/Azure/azure-powershell/issues/8671 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-408">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="75345-409">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="75345-409">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="75345-410">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-410">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="75345-411">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="75345-411">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="75345-412">https://github.com/Azure/azure-powershell/issues/9307 ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="75345-412">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="75345-413">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="75345-413">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="75345-414">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-414">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="75345-415">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="75345-415">Az.Automation</span></span>
* <span data-ttu-id="75345-416">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-416">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-417">Az.Compute</span></span>
* <span data-ttu-id="75345-418">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-418">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="75345-419">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="75345-419">Az.DataFactory</span></span>
* <span data-ttu-id="75345-420">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="75345-420">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="75345-421">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="75345-421">Az.EventGrid</span></span>
* <span data-ttu-id="75345-422">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-422">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="75345-423">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="75345-423">Az.IotHub</span></span>
* <span data-ttu-id="75345-424">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-424">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-425">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-425">Az.Network</span></span>
* <span data-ttu-id="75345-426">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-426">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="75345-427">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-427">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="75345-428">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="75345-428">Az.PolicyInsights</span></span>
* <span data-ttu-id="75345-429">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-429">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="75345-430">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="75345-430">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="75345-431">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="75345-431">Az.OperationalInsights</span></span>
* <span data-ttu-id="75345-432">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-432">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="75345-433">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-433">Az.RecoveryServices</span></span>
* <span data-ttu-id="75345-434">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="75345-434">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-435">Az.Resources</span></span>
    - <span data-ttu-id="75345-436">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="75345-436">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="75345-437">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-437">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="75345-438">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-438">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="75345-439">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-439">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="75345-440">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="75345-440">Az.ServiceBus</span></span>
* <span data-ttu-id="75345-441">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-441">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-442">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-442">Az.Sql</span></span>
* <span data-ttu-id="75345-443">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-443">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="75345-444">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="75345-444">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="75345-445">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="75345-445">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="75345-446">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="75345-446">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="75345-447">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="75345-447">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="75345-448">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="75345-448">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="75345-449">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="75345-449">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="75345-450">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="75345-450">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="75345-451">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="75345-451">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="75345-452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-452">Az.Storage</span></span>
* <span data-ttu-id="75345-453">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="75345-453">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="75345-454">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="75345-454">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="75345-455">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-455">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="75345-456">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="75345-456">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="75345-457">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-457">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="75345-458">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75345-458">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="75345-459">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75345-459">Set-AzStorageAccount</span></span>
* <span data-ttu-id="75345-460">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-460">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="75345-461">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="75345-461">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="75345-462">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="75345-462">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="75345-463">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="75345-463">Az.StorageSync</span></span>
* <span data-ttu-id="75345-464">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="75345-464">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="75345-465">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="75345-465">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="75345-466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-466">Az.Accounts</span></span>
* <span data-ttu-id="75345-467">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-467">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="75345-468">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="75345-468">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="75345-469">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-469">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="75345-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="75345-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="75345-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="75345-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-472">Az.Compute</span></span>
* <span data-ttu-id="75345-473">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="75345-473">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="75345-474">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-474">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="75345-475">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="75345-475">Az.Dns</span></span>
* <span data-ttu-id="75345-476">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-476">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="75345-477">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="75345-477">Az.EventGrid</span></span>
* <span data-ttu-id="75345-478">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-478">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="75345-479">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="75345-479">New cmdlets:</span></span>
    - <span data-ttu-id="75345-480">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="75345-480">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="75345-481">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="75345-481">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="75345-482">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="75345-482">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="75345-483">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="75345-483">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="75345-484">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="75345-484">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="75345-485">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="75345-485">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="75345-486">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="75345-486">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="75345-487">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="75345-487">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="75345-488">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="75345-488">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="75345-489">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="75345-489">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="75345-490">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="75345-490">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="75345-491">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="75345-491">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="75345-492">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="75345-492">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="75345-493">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="75345-493">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="75345-494">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="75345-494">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="75345-495">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="75345-495">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="75345-496">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="75345-496">Updated cmdlets:</span></span>
    - <span data-ttu-id="75345-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="75345-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="75345-498">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="75345-498">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="75345-499">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="75345-499">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="75345-500">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="75345-500">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="75345-501">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="75345-501">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="75345-502">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="75345-502">Event subscription expiration date,</span></span>
            - <span data-ttu-id="75345-503">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="75345-503">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="75345-504">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="75345-504">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="75345-505">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="75345-505">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="75345-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="75345-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="75345-507">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="75345-507">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="75345-508">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="75345-508">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="75345-509">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="75345-509">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="75345-510">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="75345-510">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="75345-511">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="75345-511">Az.FrontDoor</span></span>
* <span data-ttu-id="75345-512">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="75345-512">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="75345-513">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="75345-513">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="75345-514">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="75345-514">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="75345-515">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="75345-515">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-516">Az.Network</span></span>
* <span data-ttu-id="75345-517">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="75345-517">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="75345-518">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-518">New cmdlets</span></span>
        - <span data-ttu-id="75345-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="75345-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="75345-520">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="75345-520">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="75345-521">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-521">New cmdlets</span></span> 
        - <span data-ttu-id="75345-522">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="75345-522">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="75345-523">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="75345-523">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="75345-524">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-524">New cmdlets</span></span> 
        - <span data-ttu-id="75345-525">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="75345-525">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="75345-526">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="75345-526">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="75345-527">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="75345-527">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="75345-528">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="75345-528">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="75345-529">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="75345-529">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="75345-530">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="75345-530">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="75345-531">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-531">New cmdlets</span></span>
        - <span data-ttu-id="75345-532">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="75345-532">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="75345-533">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="75345-533">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="75345-534">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="75345-534">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="75345-535">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="75345-535">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="75345-536">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="75345-536">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="75345-537">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-537">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="75345-538">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-538">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="75345-539">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-539">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="75345-540">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-540">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="75345-541">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-541">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="75345-542">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-542">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="75345-543">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-543">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="75345-544">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-544">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="75345-545">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-545">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="75345-546">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-546">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="75345-547">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-547">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="75345-548">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-548">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="75345-549">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-549">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="75345-550">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="75345-550">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="75345-551">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-551">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="75345-552">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-552">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="75345-553">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="75345-553">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="75345-554">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="75345-554">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="75345-555">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="75345-555">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="75345-556">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-556">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="75345-557">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-557">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="75345-558">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-558">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="75345-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="75345-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="75345-560">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-560">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-561">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-561">Az.Resources</span></span>
* <span data-ttu-id="75345-562">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="75345-562">Support for additional Template Export options</span></span>
    - <span data-ttu-id="75345-563">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-563">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="75345-564">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-564">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="75345-565">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-565">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="75345-566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="75345-566">Az.ServiceFabric</span></span>
* <span data-ttu-id="75345-567">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-567">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-568">Az.Sql</span></span>
* <span data-ttu-id="75345-569">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-569">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="75345-570">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-570">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="75345-571">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-571">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="75345-572">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75345-572">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="75345-573">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75345-573">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="75345-574">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75345-574">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="75345-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="75345-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="75345-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="75345-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="75345-577">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-577">Az.Storage</span></span>
* <span data-ttu-id="75345-578">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="75345-578">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="75345-579">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75345-579">New-AzStorageAccount</span></span>
* <span data-ttu-id="75345-580">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-580">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="75345-581">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="75345-581">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="75345-582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-582">Az.Websites</span></span>
* <span data-ttu-id="75345-583">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="75345-583">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="75345-584">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="75345-584">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="75345-585">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="75345-585">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="75345-586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="75345-586">Az.Cdn</span></span>
* <span data-ttu-id="75345-587">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-587">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-588">Az.Compute</span></span>
* <span data-ttu-id="75345-589">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-589">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="75345-590">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="75345-590">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="75345-591">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="75345-591">Az.EventHub</span></span>
* <span data-ttu-id="75345-592">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="75345-592">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="75345-593">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="75345-593">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-594">Az.Network</span></span>
* <span data-ttu-id="75345-595">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-595">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="75345-596">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-596">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="75345-597">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="75345-597">Az.PolicyInsights</span></span>
* <span data-ttu-id="75345-598">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-598">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="75345-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="75345-600">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-600">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="75345-601">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="75345-601">Az.ServiceBus</span></span>
* <span data-ttu-id="75345-602">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="75345-602">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="75345-603">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="75345-603">Az.ServiceFabric</span></span>
* <span data-ttu-id="75345-604">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-604">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="75345-605">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-605">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-606">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-606">Az.Sql</span></span>
* <span data-ttu-id="75345-607">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-607">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="75345-608">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="75345-608">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="75345-609">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="75345-609">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="75345-610">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="75345-610">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="75345-611">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-611">Az.Websites</span></span>
* <span data-ttu-id="75345-612">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="75345-612">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="75345-613">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="75345-613">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="75345-614">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="75345-614">Az.ApiManagement</span></span>
* <span data-ttu-id="75345-615">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="75345-615">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="75345-616">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="75345-616">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="75345-617">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="75345-617">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="75345-618">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="75345-618">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="75345-619">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="75345-619">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="75345-620">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="75345-620">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="75345-621">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="75345-621">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="75345-622">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="75345-622">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="75345-623">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="75345-623">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="75345-624">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="75345-624">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="75345-625">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="75345-625">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="75345-626">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="75345-626">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="75345-627">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="75345-627">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="75345-628">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="75345-628">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="75345-629">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="75345-629">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="75345-630">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="75345-630">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="75345-631">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="75345-631">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="75345-632">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="75345-632">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="75345-633">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="75345-633">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="75345-634">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="75345-634">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="75345-635">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="75345-635">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="75345-636">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="75345-636">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="75345-637">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="75345-637">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="75345-638">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-638">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="75345-639">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-639">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="75345-640">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-640">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="75345-641">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="75345-641">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="75345-642">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="75345-642">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="75345-643">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-643">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="75345-644">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-644">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="75345-645">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-645">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="75345-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="75345-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="75345-647">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-647">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="75345-648">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-648">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="75345-649">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="75345-649">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="75345-650">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="75345-650">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="75345-651">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="75345-651">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="75345-652">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-652">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="75345-653">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-653">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="75345-654">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-654">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="75345-655">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="75345-655">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="75345-656">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="75345-656">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="75345-657">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="75345-657">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="75345-658">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="75345-658">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="75345-659">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-659">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="75345-660">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="75345-660">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="75345-661">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="75345-661">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="75345-662">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="75345-662">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="75345-663">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-663">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="75345-664">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="75345-664">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="75345-665">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="75345-665">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="75345-666">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="75345-666">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="75345-667">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="75345-667">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="75345-668">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-668">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="75345-669">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="75345-669">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="75345-670">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="75345-670">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="75345-671">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-671">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="75345-672">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="75345-672">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="75345-673">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="75345-673">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="75345-674">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-674">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="75345-675">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-675">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="75345-676">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="75345-676">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="75345-677">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="75345-677">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="75345-678">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-678">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="75345-679">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-679">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="75345-680">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="75345-680">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="75345-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="75345-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="75345-682">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="75345-682">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="75345-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="75345-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="75345-684">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="75345-684">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="75345-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="75345-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="75345-686">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="75345-686">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="75345-687">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="75345-687">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="75345-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="75345-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="75345-689">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="75345-689">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="75345-690">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="75345-690">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="75345-691">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="75345-691">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="75345-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="75345-692">Az.Automation</span></span>
* <span data-ttu-id="75345-693">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-693">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="75345-694">https://github.com/Azure/azure-powershell/issues/7977 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-694">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="75345-695">https://github.com/Azure/azure-powershell/issues/8600 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-695">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="75345-696">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-696">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="75345-697">https://github.com/Azure/azure-powershell/issues/8347 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="75345-698">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-698">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="75345-699">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="75345-699">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-700">Az.Compute</span></span>
* <span data-ttu-id="75345-701">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-701">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="75345-702">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="75345-702">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="75345-703">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="75345-703">Az.DataLakeStore</span></span>
* <span data-ttu-id="75345-704">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-704">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="75345-705">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="75345-705">Az.Monitor</span></span>
* <span data-ttu-id="75345-706">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-706">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-707">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-707">Az.Network</span></span>
* <span data-ttu-id="75345-708">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-708">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="75345-709">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="75345-709">Updated cmdlet:</span></span>
        - <span data-ttu-id="75345-710">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="75345-710">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="75345-711">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-711">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-712">Az.Resources</span></span>
* <span data-ttu-id="75345-713">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-713">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-714">Az.Sql</span></span>
* <span data-ttu-id="75345-715">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="75345-715">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="75345-716">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="75345-716">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="75345-717">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-717">Az.Accounts</span></span>
* <span data-ttu-id="75345-718">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="75345-718">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="75345-719">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="75345-719">Az.CognitiveServices</span></span>
* <span data-ttu-id="75345-720">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="75345-720">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="75345-721">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="75345-721">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-722">Az.Compute</span></span>
* <span data-ttu-id="75345-723">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="75345-723">Proximity placement group feature.</span></span>
    - <span data-ttu-id="75345-724">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="75345-724">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="75345-725">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="75345-725">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="75345-726">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-726">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="75345-727">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="75345-727">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="75345-728">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-728">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="75345-729">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="75345-729">Breaking changes</span></span>
    - <span data-ttu-id="75345-730">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-730">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="75345-731">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-731">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="75345-732">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="75345-732">Az.DeploymentManager</span></span>
* <span data-ttu-id="75345-733">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="75345-733">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="75345-734">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="75345-734">Az.Dns</span></span>
* <span data-ttu-id="75345-735">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="75345-735">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="75345-736">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="75345-736">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="75345-737">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="75345-737">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="75345-738">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="75345-738">Az.FrontDoor</span></span>
* <span data-ttu-id="75345-739">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="75345-739">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="75345-740">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="75345-740">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="75345-741">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="75345-741">Az.HDInsight</span></span>
* <span data-ttu-id="75345-742">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="75345-742">Removed two cmdlets:</span></span>
    - <span data-ttu-id="75345-743">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="75345-743">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="75345-744">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="75345-744">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="75345-745">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-745">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="75345-746">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="75345-746">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="75345-747">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="75345-747">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="75345-748">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="75345-748">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="75345-749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="75345-749">Az.Monitor</span></span>
* <span data-ttu-id="75345-750">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="75345-750">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="75345-751">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="75345-751">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="75345-752">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="75345-752">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="75345-753">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="75345-753">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="75345-754">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="75345-754">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="75345-755">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="75345-755">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="75345-756">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="75345-756">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="75345-757">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="75345-757">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="75345-758">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="75345-758">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="75345-759">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="75345-759">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="75345-760">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="75345-760">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="75345-761">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="75345-761">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="75345-762">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="75345-762">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="75345-763">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-763">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-764">Az.Network</span></span>
* <span data-ttu-id="75345-765">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="75345-765">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="75345-766">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-766">New cmdlets</span></span>
        - <span data-ttu-id="75345-767">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="75345-767">New-AzNatGateway</span></span>
        - <span data-ttu-id="75345-768">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="75345-768">Get-AzNatGateway</span></span>
        - <span data-ttu-id="75345-769">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="75345-769">Set-AzNatGateway</span></span>
        - <span data-ttu-id="75345-770">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="75345-770">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="75345-771">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-771">Updated cmdlets</span></span>
        - <span data-ttu-id="75345-772">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="75345-772">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="75345-773">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="75345-773">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="75345-774">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="75345-774">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="75345-775">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-775">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="75345-776">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-776">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="75345-777">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="75345-777">Az.PolicyInsights</span></span>
* <span data-ttu-id="75345-778">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="75345-778">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="75345-779">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="75345-779">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="75345-780">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="75345-780">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="75345-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="75345-782">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="75345-782">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="75345-783">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="75345-783">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="75345-784">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="75345-784">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="75345-785">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="75345-785">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="75345-786">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="75345-786">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="75345-787">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="75345-787">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="75345-788">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="75345-788">Az.Relay</span></span>
* <span data-ttu-id="75345-789">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="75345-789">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="75345-790">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="75345-790">Az.ServiceBus</span></span>
* <span data-ttu-id="75345-791">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-791">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="75345-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-792">Az.Storage</span></span>
* <span data-ttu-id="75345-793">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="75345-793">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="75345-794">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="75345-794">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="75345-795">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="75345-795">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="75345-796">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75345-796">New-AzStorageAccount</span></span>
* <span data-ttu-id="75345-797">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="75345-797">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="75345-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75345-798">New-AzStorageAccount</span></span>
    - <span data-ttu-id="75345-799">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75345-799">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="75345-800">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75345-800">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="75345-801">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-801">Az.Websites</span></span>
* <span data-ttu-id="75345-802">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="75345-802">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="75345-803">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="75345-803">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="75345-804">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="75345-804">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="75345-805">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="75345-805">Highlights since the last major release</span></span>
* <span data-ttu-id="75345-806">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="75345-806">General availability of `Az` module</span></span>
* <span data-ttu-id="75345-807">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="75345-807">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="75345-808">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="75345-808">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="75345-809">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-809">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="75345-810">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-810">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="75345-811">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-811">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="75345-812">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-812">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="75345-813">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-813">Az.Accounts</span></span>
* <span data-ttu-id="75345-814">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-814">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="75345-815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="75345-815">Az.Batch</span></span>
* <span data-ttu-id="75345-816">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-816">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="75345-817">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="75345-817">Az.Cdn</span></span>
* <span data-ttu-id="75345-818">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="75345-819">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="75345-819">Az.CognitiveServices</span></span>
* <span data-ttu-id="75345-820">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-821">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-821">Az.Compute</span></span>
* <span data-ttu-id="75345-822">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-822">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="75345-823">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-823">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="75345-824">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-824">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="75345-825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="75345-825">Az.DataFactory</span></span>
* <span data-ttu-id="75345-826">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-826">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="75345-827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="75345-827">Az.DataLakeStore</span></span>
* <span data-ttu-id="75345-828">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-828">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="75345-829">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="75345-829">Az.EventGrid</span></span>
* <span data-ttu-id="75345-830">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-830">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="75345-831">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="75345-831">Az.EventHub</span></span>
* <span data-ttu-id="75345-832">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-832">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="75345-833">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="75345-833">Az.HDInsight</span></span>
* <span data-ttu-id="75345-834">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-834">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="75345-835">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="75345-835">Az.IotHub</span></span>
* <span data-ttu-id="75345-836">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="75345-837">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="75345-837">Az.KeyVault</span></span>
* <span data-ttu-id="75345-838">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="75345-839">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-839">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="75345-840">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="75345-840">Az.MachineLearning</span></span>
* <span data-ttu-id="75345-841">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-841">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="75345-842">Az.Media</span><span class="sxs-lookup"><span data-stu-id="75345-842">Az.Media</span></span>
* <span data-ttu-id="75345-843">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="75345-844">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="75345-844">Az.Monitor</span></span>
  * <span data-ttu-id="75345-845">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="75345-845">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="75345-846">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="75345-846">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="75345-847">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="75345-847">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="75345-848">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="75345-848">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="75345-849">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="75345-849">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="75345-850">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="75345-850">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="75345-851">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-851">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-852">Az.Network</span></span>
* <span data-ttu-id="75345-853">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="75345-854">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-854">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="75345-855">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="75345-855">Az.NotificationHubs</span></span>
* <span data-ttu-id="75345-856">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-856">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="75345-857">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="75345-857">Az.OperationalInsights</span></span>
* <span data-ttu-id="75345-858">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="75345-859">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="75345-859">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="75345-860">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="75345-861">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-861">Az.RecoveryServices</span></span>
* <span data-ttu-id="75345-862">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="75345-863">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="75345-863">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="75345-864">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-864">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="75345-865">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-865">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="75345-866">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="75345-866">Az.RedisCache</span></span>
* <span data-ttu-id="75345-867">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-867">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-868">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-868">Az.Resources</span></span>
* <span data-ttu-id="75345-869">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-869">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-870">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-870">Az.Sql</span></span>
* <span data-ttu-id="75345-871">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-871">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="75345-872">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-872">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="75345-873">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-873">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="75345-874">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-874">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="75345-875">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-875">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="75345-876">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="75345-876">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="75345-877">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-877">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="75345-878">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-878">Az.Websites</span></span>
* <span data-ttu-id="75345-879">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-879">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="75345-880">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-880">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="75345-881">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-881">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="75345-882">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="75345-882">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="75345-883">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="75345-883">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="75345-884">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="75345-884">Highlights since the last major release</span></span>
* <span data-ttu-id="75345-885">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="75345-885">General availability of `Az` module</span></span>
* <span data-ttu-id="75345-886">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="75345-886">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="75345-887">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="75345-887">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="75345-888">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-888">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="75345-889">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-889">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="75345-890">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-890">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="75345-891">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-891">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="75345-892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-892">Az.Accounts</span></span>
* <span data-ttu-id="75345-893">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-893">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="75345-894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="75345-894">Az.AnalysisServices</span></span>
* <span data-ttu-id="75345-895">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="75345-895">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="75345-896">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="75345-896">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="75345-897">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="75345-897">Az.Automation</span></span>
* <span data-ttu-id="75345-898">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-898">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="75345-899">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="75345-899">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="75345-900">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="75345-900">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-901">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-901">Az.Compute</span></span>
* <span data-ttu-id="75345-902">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-902">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="75345-903">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="75345-903">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="75345-904">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="75345-904">Az.ContainerInstance</span></span>
* <span data-ttu-id="75345-905">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-905">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="75345-906">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="75345-906">Az.DataFactory</span></span>
* <span data-ttu-id="75345-907">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-907">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="75345-908">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-908">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-909">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-909">Az.Resources</span></span>
* <span data-ttu-id="75345-910">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-910">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="75345-911">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-911">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="75345-912">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="75345-912">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="75345-913">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="75345-913">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="75345-914">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-914">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="75345-915">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="75345-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-916">Az.Sql</span></span>
* <span data-ttu-id="75345-917">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="75345-917">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="75345-918">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-918">Az.Storage</span></span>
* <span data-ttu-id="75345-919">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="75345-919">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="75345-920">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="75345-920">New-AzStorageContext</span></span>
* <span data-ttu-id="75345-921">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="75345-921">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="75345-922">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="75345-922">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="75345-923">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="75345-923">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="75345-924">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="75345-924">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="75345-925">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="75345-925">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="75345-926">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="75345-926">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="75345-927">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="75345-927">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="75345-928">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="75345-928">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="75345-929">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="75345-929">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="75345-930">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="75345-930">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="75345-931">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="75345-931">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="75345-932">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="75345-932">Highlights since the last major release</span></span>
* <span data-ttu-id="75345-933">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="75345-933">General availability of `Az` module</span></span>
* <span data-ttu-id="75345-934">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="75345-934">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="75345-935">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="75345-935">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="75345-936">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-936">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="75345-937">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-937">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="75345-938">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-938">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="75345-939">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-939">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="75345-940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="75345-940">Az.Automation</span></span>
* <span data-ttu-id="75345-941">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="75345-941">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="75345-942">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="75345-942">Dynamic grouping</span></span>
    * <span data-ttu-id="75345-943">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="75345-943">Pre-Post script</span></span>
    * <span data-ttu-id="75345-944">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="75345-944">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-945">Az.Compute</span></span>
* <span data-ttu-id="75345-946">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="75345-946">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="75345-947">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-947">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="75345-948">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="75345-948">Az.KeyVault</span></span>
* <span data-ttu-id="75345-949">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-949">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-950">Az.Network</span></span>
* <span data-ttu-id="75345-951">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-951">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="75345-952">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-952">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="75345-953">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-953">Az.RecoveryServices</span></span>
* <span data-ttu-id="75345-954">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-954">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="75345-955">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-955">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-956">Az.Resources</span></span>
* <span data-ttu-id="75345-957">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-957">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="75345-958">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-958">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-959">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-959">Az.Sql</span></span>
* <span data-ttu-id="75345-960">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-960">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="75345-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-961">Az.Storage</span></span>
* <span data-ttu-id="75345-962">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="75345-962">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="75345-963">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="75345-963">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="75345-964">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="75345-964">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="75345-965">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="75345-965">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="75345-966">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="75345-966">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="75345-967">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="75345-967">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="75345-968">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="75345-968">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="75345-969">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-969">Az.Websites</span></span>
* <span data-ttu-id="75345-970">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-970">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="75345-971">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="75345-971">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="75345-972">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-972">Az.Accounts</span></span>
* <span data-ttu-id="75345-973">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-973">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="75345-974">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-974">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="75345-975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="75345-975">Az.Automation</span></span>
* <span data-ttu-id="75345-976">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-976">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="75345-977">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-977">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="75345-978">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="75345-978">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="75345-979">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="75345-979">Az.Cdn</span></span>
* <span data-ttu-id="75345-980">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="75345-980">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-981">Az.Compute</span></span>
* <span data-ttu-id="75345-982">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-982">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="75345-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="75345-983">Az.DataFactory</span></span>
* <span data-ttu-id="75345-984">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-984">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="75345-985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="75345-985">Az.LogicApp</span></span>
* <span data-ttu-id="75345-986">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="75345-986">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-987">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-987">Az.Network</span></span>
* <span data-ttu-id="75345-988">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-988">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="75345-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="75345-990">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-990">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="75345-991">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="75345-991">SDK Update</span></span>
* <span data-ttu-id="75345-992">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="75345-992">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="75345-993">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-993">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-994">Az.Resources</span></span>
* <span data-ttu-id="75345-995">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-995">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="75345-996">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="75345-996">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="75345-997">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-997">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="75345-998">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="75345-998">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="75345-999">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-999">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="75345-1000">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="75345-1000">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-1001">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-1001">Az.Sql</span></span>
* <span data-ttu-id="75345-1002">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="75345-1002">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="75345-1003">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="75345-1003">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="75345-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-1004">Az.Storage</span></span>
* <span data-ttu-id="75345-1005">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75345-1005">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="75345-1006">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="75345-1006">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="75345-1007">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="75345-1007">Az.AnalysisServices</span></span>
* <span data-ttu-id="75345-1008">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="75345-1008">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="75345-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="75345-1009">Az.Automation</span></span>
* <span data-ttu-id="75345-1010">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1010">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="75345-1011">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1011">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="75345-1012">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1012">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="75345-1013">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="75345-1013">Az.CognitiveServices</span></span>
* <span data-ttu-id="75345-1014">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1014">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-1015">Az.Compute</span></span>
* <span data-ttu-id="75345-1016">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1016">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="75345-1017">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1017">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="75345-1018">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1018">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="75345-1019">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="75345-1019">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="75345-1020">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="75345-1020">Az.DataLakeStore</span></span>
* <span data-ttu-id="75345-1021">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1021">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="75345-1022">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="75345-1022">Az.EventHub</span></span>
* <span data-ttu-id="75345-1023">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1023">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="75345-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="75345-1024">Az.KeyVault</span></span>
* <span data-ttu-id="75345-1025">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1025">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="75345-1026">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="75345-1026">Az.LogicApp</span></span>
* <span data-ttu-id="75345-1027">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1027">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="75345-1028">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1028">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="75345-1029">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-1029">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="75345-1030">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="75345-1030">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="75345-1031">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="75345-1031">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="75345-1032">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="75345-1032">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="75345-1033">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="75345-1033">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="75345-1034">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="75345-1034">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="75345-1035">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="75345-1035">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="75345-1036">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="75345-1036">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="75345-1037">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="75345-1037">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="75345-1038">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="75345-1038">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="75345-1039">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1039">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="75345-1040">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="75345-1040">Az.Monitor</span></span>
* <span data-ttu-id="75345-1041">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1041">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-1042">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-1042">Az.Network</span></span>
* <span data-ttu-id="75345-1043">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1043">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="75345-1044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="75345-1044">Az.OperationalInsights</span></span>
* <span data-ttu-id="75345-1045">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="75345-1045">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="75345-1046">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1046">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="75345-1047">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1047">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="75345-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-1048">Az.Resources</span></span>
* <span data-ttu-id="75345-1049">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1049">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="75345-1050">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1050">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="75345-1051">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="75345-1052">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1052">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-1053">Az.Sql</span></span>
* <span data-ttu-id="75345-1054">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1054">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="75345-1055">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1055">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="75345-1056">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-1056">Az.Websites</span></span>
* <span data-ttu-id="75345-1057">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1057">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="75345-1058">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="75345-1058">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="75345-1059">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-1059">Az.Accounts</span></span>
* <span data-ttu-id="75345-1060">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="75345-1060">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="75345-1061">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="75345-1061">Az.AnalysisServices</span></span>
<span data-ttu-id="75345-1062">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="75345-1062">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-1063">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-1063">Az.Compute</span></span>
* <span data-ttu-id="75345-1064">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1064">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="75345-1065">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1065">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="75345-1066">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1066">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="75345-1067">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-1067">Az.RecoveryServices</span></span>
<span data-ttu-id="75345-1068">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="75345-1068">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-1069">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-1069">Az.Resources</span></span>
* <span data-ttu-id="75345-1070">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1070">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="75345-1071">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="75345-1071">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="75345-1072">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1072">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="75345-1073">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="75345-1073">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-1074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-1074">Az.Sql</span></span>
* <span data-ttu-id="75345-1075">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="75345-1075">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="75345-1076">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1076">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="75345-1077">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1077">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="75345-1078">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="75345-1078">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="75345-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-1079">Az.Accounts</span></span>
* <span data-ttu-id="75345-1080">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="75345-1080">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="75345-1081">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="75345-1081">Az.AnalysisServices</span></span>
* <span data-ttu-id="75345-1082">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="75345-1082">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="75345-1083">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-1083">Az.RecoveryServices</span></span>
* <span data-ttu-id="75345-1084">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="75345-1084">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="75345-1085">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="75345-1085">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="75345-1086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-1086">Az.Accounts</span></span>
* <span data-ttu-id="75345-1087">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1087">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="75345-1088">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1088">Update incorrect online help URLs</span></span>
* <span data-ttu-id="75345-1089">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1089">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="75345-1090">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="75345-1090">Az.Aks</span></span>
* <span data-ttu-id="75345-1091">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1091">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="75345-1092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="75345-1092">Az.Automation</span></span>
* <span data-ttu-id="75345-1093">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1093">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="75345-1094">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1094">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="75345-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="75345-1095">Az.Cdn</span></span>
* <span data-ttu-id="75345-1096">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1096">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-1097">Az.Compute</span></span>
* <span data-ttu-id="75345-1098">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1098">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="75345-1099">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1099">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="75345-1100">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1100">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="75345-1101">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="75345-1101">Az.ContainerRegistry</span></span>
* <span data-ttu-id="75345-1102">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1102">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="75345-1103">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="75345-1103">Az.DataFactory</span></span>
* <span data-ttu-id="75345-1104">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1104">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="75345-1105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="75345-1105">Az.DataLakeStore</span></span>
* <span data-ttu-id="75345-1106">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1106">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="75345-1107">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="75345-1107">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="75345-1108">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1108">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="75345-1109">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="75345-1109">Az.IotHub</span></span>
* <span data-ttu-id="75345-1110">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1110">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="75345-1111">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="75345-1111">Az.KeyVault</span></span>
* <span data-ttu-id="75345-1112">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1112">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-1113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-1113">Az.Network</span></span>
* <span data-ttu-id="75345-1114">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1114">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-1115">Az.Resources</span></span>
* <span data-ttu-id="75345-1116">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1116">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="75345-1117">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1117">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="75345-1118">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1118">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="75345-1119">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1119">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="75345-1120">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1120">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="75345-1121">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1121">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="75345-1122">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="75345-1122">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="75345-1123">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="75345-1123">Az.ServiceFabric</span></span>
* <span data-ttu-id="75345-1124">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="75345-1124">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="75345-1125">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1125">Fix some error messages.</span></span>
* <span data-ttu-id="75345-1126">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1126">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="75345-1127">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1127">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="75345-1128">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="75345-1128">Az.SignalR</span></span>
* <span data-ttu-id="75345-1129">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1129">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-1130">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-1130">Az.Sql</span></span>
* <span data-ttu-id="75345-1131">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1131">Update incorrect online help URLs</span></span>
* <span data-ttu-id="75345-1132">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1132">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="75345-1133">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1133">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="75345-1134">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="75345-1134">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="75345-1135">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-1135">Az.Storage</span></span>
* <span data-ttu-id="75345-1136">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1136">Update incorrect online help URLs</span></span>
* <span data-ttu-id="75345-1137">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="75345-1137">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="75345-1138">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="75345-1138">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="75345-1139">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="75345-1139">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="75345-1140">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="75345-1140">Az.TrafficManager</span></span>
* <span data-ttu-id="75345-1141">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1141">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="75345-1142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-1142">Az.Websites</span></span>
* <span data-ttu-id="75345-1143">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1143">Update incorrect online help URLs</span></span>
* <span data-ttu-id="75345-1144">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1144">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="75345-1145">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1145">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="75345-1146">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="75345-1146">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="75345-1147">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-1147">Az.Accounts</span></span>
* <span data-ttu-id="75345-1148">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1148">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-1149">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-1149">Az.Compute</span></span>
* <span data-ttu-id="75345-1150">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="75345-1150">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="75345-1151">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1151">Updated the description of ID in help files</span></span>
* <span data-ttu-id="75345-1152">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="75345-1152">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="75345-1153">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="75345-1153">Az.DataLakeStore</span></span>
* <span data-ttu-id="75345-1154">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1154">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="75345-1155">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1155">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="75345-1156">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="75345-1156">Az.EventGrid</span></span>
* <span data-ttu-id="75345-1157">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1157">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="75345-1158">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1158">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="75345-1159">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="75345-1159">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="75345-1160">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="75345-1160">Event Time-To-Live,</span></span>
        - <span data-ttu-id="75345-1161">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="75345-1161">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="75345-1162">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="75345-1162">Dead letter endpoint.</span></span>
    - <span data-ttu-id="75345-1163">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="75345-1163">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="75345-1164">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="75345-1164">Event Time-To-Live,</span></span>
        - <span data-ttu-id="75345-1165">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="75345-1165">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="75345-1166">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="75345-1166">Dead letter endpoint.</span></span>
* <span data-ttu-id="75345-1167">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1167">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="75345-1168">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="75345-1168">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="75345-1169">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="75345-1169">Az.IotHub</span></span>
* <span data-ttu-id="75345-1170">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1170">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="75345-1171">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="75345-1171">Az.LogicApp</span></span>
* <span data-ttu-id="75345-1172">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="75345-1172">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-1173">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-1173">Az.Resources</span></span>
* <span data-ttu-id="75345-1174">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1174">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="75345-1175">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="75345-1175">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="75345-1176">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1176">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="75345-1177">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1177">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="75345-1178">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1178">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="75345-1179">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="75345-1179">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="75345-1180">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="75345-1180">Az.SignalR</span></span>
* <span data-ttu-id="75345-1181">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="75345-1181">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-1182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-1182">Az.Sql</span></span>
* <span data-ttu-id="75345-1183">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="75345-1183">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="75345-1184">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-1184">Az.Storage</span></span>
* <span data-ttu-id="75345-1185">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="75345-1185">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="75345-1186">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="75345-1186">New-AzStorageContext</span></span>
* <span data-ttu-id="75345-1187">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1187">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="75345-1188">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="75345-1188">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="75345-1189">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-1189">Az.Websites</span></span>
* <span data-ttu-id="75345-1190">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1190">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="75345-1191">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="75345-1191">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="75345-1192">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="75345-1192">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="75345-1193">Genel</span><span class="sxs-lookup"><span data-stu-id="75345-1193">General</span></span>

- <span data-ttu-id="75345-1194">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="75345-1194">General Availability of Az Module</span></span>
- <span data-ttu-id="75345-1195">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="75345-1195">Online help for each module</span></span>
- <span data-ttu-id="75345-1196">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="75345-1196">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="75345-1197">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1197">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="75345-1198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="75345-1198">Az.Accounts</span></span>
- <span data-ttu-id="75345-1199">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="75345-1199">Changed from Az.Profile</span></span>
- <span data-ttu-id="75345-1200">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1200">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="75345-1201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="75345-1201">Az.ApiManagement</span></span>
- <span data-ttu-id="75345-1202">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="75345-1202">Fixes for #7002</span></span>
- <span data-ttu-id="75345-1203">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1203">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="75345-1204">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="75345-1204">Az.Batch</span></span>
- <span data-ttu-id="75345-1205">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1205">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="75345-1206">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="75345-1206">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="75345-1207">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="75345-1208">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="75345-1208">Az.Billing</span></span>
- <span data-ttu-id="75345-1209">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1209">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="75345-1210">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="75345-1210">Az.CognitivServices</span></span>
- <span data-ttu-id="75345-1211">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1211">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="75345-1212">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="75345-1212">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="75345-1213">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="75345-1213">Az.ContainerInstance</span></span>
- <span data-ttu-id="75345-1214">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1214">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="75345-1215">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="75345-1215">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="75345-1216">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1216">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="75345-1217">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="75345-1217">Az.DataLakeStore</span></span>
- <span data-ttu-id="75345-1218">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="75345-1219">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="75345-1219">Az.Monitor</span></span>
- <span data-ttu-id="75345-1220">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1220">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="75345-1221">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="75345-1221">Az.KeyVault</span></span>
- <span data-ttu-id="75345-1222">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="75345-1222">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="75345-1223">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="75345-1223">Az.MachineLearning</span></span>
- <span data-ttu-id="75345-1224">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1224">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="75345-1225">Az.Media</span><span class="sxs-lookup"><span data-stu-id="75345-1225">Az.Media</span></span>
- <span data-ttu-id="75345-1226">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="75345-1226">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="75345-1227">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-1227">Az.Network</span></span>
<span data-ttu-id="75345-1228">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1228">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="75345-1229">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="75345-1229">New cmdlets added:</span></span>
        - <span data-ttu-id="75345-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="75345-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="75345-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="75345-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="75345-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="75345-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="75345-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="75345-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="75345-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="75345-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="75345-1235">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="75345-1235">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="75345-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="75345-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="75345-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="75345-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="75345-1238">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1238">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="75345-1239">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75345-1239">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="75345-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="75345-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="75345-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="75345-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="75345-1242">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75345-1242">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="75345-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="75345-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="75345-1244">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="75345-1244">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="75345-1245">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1245">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="75345-1246">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="75345-1246">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="75345-1247">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="75345-1247">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="75345-1248">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="75345-1248">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="75345-1249">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1249">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="75345-1250">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1250">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="75345-1251">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="75345-1251">Az.OperationalInsights</span></span>
- <span data-ttu-id="75345-1252">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="75345-1253">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="75345-1253">Az.Profile</span></span>
- <span data-ttu-id="75345-1254">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1254">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="75345-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-1255">Az.RecoveryServices</span></span>
- <span data-ttu-id="75345-1256">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1256">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="75345-1257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-1257">Az.Resources</span></span>
- <span data-ttu-id="75345-1258">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="75345-1259">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="75345-1259">Az.ServiceFabric</span></span>
- <span data-ttu-id="75345-1260">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="75345-1260">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="75345-1261">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1261">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="75345-1262">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="75345-1262">Az.SIgnalR</span></span>
- <span data-ttu-id="75345-1263">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="75345-1263">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="75345-1264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-1264">Az.Sql</span></span>
- <span data-ttu-id="75345-1265">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1265">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="75345-1266">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1266">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="75345-1267">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1267">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="75345-1268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-1268">Az.Storage</span></span>
- <span data-ttu-id="75345-1269">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="75345-1270">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-1270">Az.Websites</span></span>
- <span data-ttu-id="75345-1271">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="75345-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="75345-1272">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="75345-1272">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="75345-1273">Genel</span><span class="sxs-lookup"><span data-stu-id="75345-1273">General</span></span>

* <span data-ttu-id="75345-1274">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="75345-1274">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="75345-1275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-1275">Az.Compute</span></span>

* <span data-ttu-id="75345-1276">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1276">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="75345-1277">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="75345-1277">Az.DataLakeStore</span></span>

* <span data-ttu-id="75345-1278">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1278">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="75345-1279">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="75345-1279">Az.FrontDoor</span></span>

* <span data-ttu-id="75345-1280">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1280">Fixed some broken links</span></span>
    - <span data-ttu-id="75345-1281">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1281">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="75345-1282">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1282">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="75345-1283">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="75345-1283">Az.RecoveryServices</span></span>

* <span data-ttu-id="75345-1284">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1284">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="75345-1285">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1285">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="75345-1286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-1286">Az.Resources</span></span>

* <span data-ttu-id="75345-1287">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="75345-1287">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="75345-1288">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1288">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="75345-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-1289">Az.Sql</span></span>

* <span data-ttu-id="75345-1290">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="75345-1290">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="75345-1291">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1291">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="75345-1292">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1292">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="75345-1293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="75345-1293">Az.Storage</span></span>

* <span data-ttu-id="75345-1294">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1294">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="75345-1295">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1295">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="75345-1296">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="75345-1296">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="75345-1297">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1297">Support Static Website configuration</span></span>
    - <span data-ttu-id="75345-1298">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="75345-1298">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="75345-1299">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="75345-1299">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="75345-1300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-1300">Az.Websites</span></span>

* <span data-ttu-id="75345-1301">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="75345-1301">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="75345-1302">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1302">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="75345-1303">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="75345-1303">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="75345-1304">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="75345-1304">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="75345-1305">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="75345-1305">Az.ApiManagement</span></span>
* <span data-ttu-id="75345-1306">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="75345-1306">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="75345-1307">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="75345-1307">Az.Automation</span></span>
* <span data-ttu-id="75345-1308">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="75345-1308">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="75345-1309">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1309">Added Update Management cmdlets</span></span>
* <span data-ttu-id="75345-1310">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1310">Added Source Control cmdlets</span></span>
* <span data-ttu-id="75345-1311">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1311">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="75345-1312">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1312">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="75345-1313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-1313">Az.Compute</span></span>
* <span data-ttu-id="75345-1314">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1314">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="75345-1315">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="75345-1315">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="75345-1316">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="75345-1316">Az.ContainerInstance</span></span>
* <span data-ttu-id="75345-1317">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="75345-1317">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="75345-1318">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="75345-1318">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="75345-1319">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1319">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="75345-1320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-1320">Az.Network</span></span>
* <span data-ttu-id="75345-1321">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1321">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="75345-1322">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1322">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="75345-1323">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1323">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="75345-1324">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1324">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="75345-1325">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="75345-1325">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="75345-1326">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1326">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="75345-1327">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="75345-1327">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="75345-1328">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="75345-1328">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="75345-1329">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1329">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="75345-1330">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="75345-1330">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="75345-1331">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="75345-1331">Az.Relay</span></span>
* <span data-ttu-id="75345-1332">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1332">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="75345-1333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-1333">Az.Resources</span></span>
* <span data-ttu-id="75345-1334">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1334">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="75345-1335">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1335">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="75345-1336">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="75345-1336">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="75345-1337">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="75345-1337">Az.ServiceFabric</span></span>
* <span data-ttu-id="75345-1338">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1338">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="75345-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-1339">Az.Sql</span></span>
* <span data-ttu-id="75345-1340">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1340">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="75345-1341">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="75345-1341">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="75345-1342">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="75345-1342">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="75345-1343">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="75345-1343">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="75345-1344">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="75345-1344">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="75345-1345">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="75345-1345">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="75345-1346">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="75345-1346">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="75345-1347">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="75345-1347">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="75345-1348">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="75345-1348">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="75345-1349">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1349">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="75345-1350">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1350">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="75345-1351">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1351">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="75345-1352">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="75345-1352">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="75345-1353">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="75345-1353">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="75345-1354">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="75345-1354">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="75345-1355">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="75345-1355">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="75345-1356">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1356">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="75345-1357">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="75345-1357">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="75345-1358">Genel</span><span class="sxs-lookup"><span data-stu-id="75345-1358">General</span></span>
* <span data-ttu-id="75345-1359">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="75345-1359">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="75345-1360">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="75345-1360">Az.Profile</span></span>
* <span data-ttu-id="75345-1361">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1361">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="75345-1362">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1362">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="75345-1363">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1363">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="75345-1364">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1364">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="75345-1365">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1365">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="75345-1366">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1366">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="75345-1367">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1367">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="75345-1368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="75345-1368">Az.CognitiveServices</span></span>
* <span data-ttu-id="75345-1369">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1369">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-1370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-1370">Az.Compute</span></span>
* <span data-ttu-id="75345-1371">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1371">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="75345-1372">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="75345-1372">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="75345-1373">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1373">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="75345-1374">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="75345-1374">Az.DataLakeStore</span></span>
* <span data-ttu-id="75345-1375">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1375">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="75345-1376">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1376">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="75345-1377">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="75345-1377">Az.Insights</span></span>
* <span data-ttu-id="75345-1378">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1378">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="75345-1379">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="75345-1379">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="75345-1380">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1380">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="75345-1381">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="75345-1381">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-1382">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-1382">Az.Network</span></span>
* <span data-ttu-id="75345-1383">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="75345-1383">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="75345-1384">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="75345-1384">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="75345-1385">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="75345-1385">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="75345-1386">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="75345-1386">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="75345-1387">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="75345-1387">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="75345-1388">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="75345-1388">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="75345-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="75345-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="75345-1390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="75345-1390">Az.PolicyInsights</span></span>
* <span data-ttu-id="75345-1391">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1391">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-1392">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-1392">Az.Resources</span></span>
* <span data-ttu-id="75345-1393">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="75345-1393">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="75345-1394">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="75345-1394">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="75345-1395">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="75345-1395">Az.ServiceBus</span></span>
* <span data-ttu-id="75345-1396">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1396">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="75345-1397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="75345-1397">Az.ServiceFabric</span></span>
* <span data-ttu-id="75345-1398">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1398">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="75345-1399">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1399">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="75345-1400">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="75345-1400">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="75345-1401">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="75345-1401">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="75345-1402">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1402">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="75345-1403">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="75345-1403">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="75345-1404">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="75345-1404">Az.Profile</span></span>
* <span data-ttu-id="75345-1405">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="75345-1405">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="75345-1406">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="75345-1406">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-1407">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-1407">Az.Compute</span></span>
* <span data-ttu-id="75345-1408">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1408">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="75345-1409">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1409">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="75345-1410">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="75345-1410">Az.DataLakeStore</span></span>
* <span data-ttu-id="75345-1411">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="75345-1411">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="75345-1412">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="75345-1412">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="75345-1413">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="75345-1413">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="75345-1414">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="75345-1414">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="75345-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="75345-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-1416">Az.Network</span></span>
* <span data-ttu-id="75345-1417">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="75345-1417">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="75345-1418">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1418">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-1419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-1419">Az.Resources</span></span>
* <span data-ttu-id="75345-1420">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1420">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="75345-1421">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="75345-1421">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="75345-1422">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="75345-1422">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="75345-1423">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="75345-1423">Azure.Storage</span></span>
* <span data-ttu-id="75345-1424">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="75345-1424">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="75345-1425">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="75345-1425">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="75345-1426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="75345-1426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="75345-1427">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="75345-1427">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="75345-1428">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="75345-1428">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="75345-1429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="75345-1429">Az.CognitiveServices</span></span>
* <span data-ttu-id="75345-1430">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="75345-1430">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="75345-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="75345-1431">Az.Compute</span></span>
* <span data-ttu-id="75345-1432">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1432">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="75345-1433">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1433">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="75345-1434">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1434">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="75345-1435">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="75345-1435">Az.DataFactoryV2</span></span>
* <span data-ttu-id="75345-1436">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="75345-1436">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="75345-1437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="75345-1437">Az.Network</span></span>
* <span data-ttu-id="75345-1438">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="75345-1438">Added NetworkProfile functionality.</span></span> <span data-ttu-id="75345-1439">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1439">new cmdlets added</span></span>
    - <span data-ttu-id="75345-1440">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="75345-1440">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="75345-1441">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="75345-1441">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="75345-1442">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="75345-1442">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="75345-1443">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="75345-1443">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="75345-1444">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="75345-1444">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="75345-1445">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="75345-1445">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="75345-1446">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1446">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="75345-1447">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1447">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="75345-1448">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1448">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="75345-1449">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="75345-1449">Az.RedisCache</span></span>
* <span data-ttu-id="75345-1450">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="75345-1450">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="75345-1451">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1451">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="75345-1452">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="75345-1452">Az.Resources</span></span>
* <span data-ttu-id="75345-1453">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="75345-1453">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="75345-1454">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1454">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="75345-1455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="75345-1455">Az.Sql</span></span>
* <span data-ttu-id="75345-1456">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="75345-1456">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="75345-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="75345-1457">Az.Websites</span></span>
* <span data-ttu-id="75345-1458">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="75345-1458">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="75345-1459">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="75345-1459">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="75345-1460">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="75345-1460">0.2.0 - September 2018</span></span>
 <span data-ttu-id="75345-1461">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="75345-1461">Initial Release</span></span>