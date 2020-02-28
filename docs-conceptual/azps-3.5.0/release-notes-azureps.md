---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 81afcd63e5ca7a776965849de9090b833f49acc7
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477242"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="01289-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="01289-103">Azure PowerShell release notes</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="01289-104">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="01289-104">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="01289-105">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="01289-105">Highlights since the last major release</span></span>
* <span data-ttu-id="01289-106">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-106">Updated client side telemetry.</span></span>
* <span data-ttu-id="01289-107">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-107">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="01289-108">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-108">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="01289-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-109">Az.Accounts</span></span>
* <span data-ttu-id="01289-110">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-110">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="01289-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="01289-111">Az.Automation</span></span>
* <span data-ttu-id="01289-112">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-112">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="01289-113">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="01289-113">Az.CognitiveServices</span></span>
* <span data-ttu-id="01289-114">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-114">Updated SDK to 7.0</span></span>
* <span data-ttu-id="01289-115">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-115">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-116">Az.Compute</span></span>
* <span data-ttu-id="01289-117">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="01289-117">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="01289-118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="01289-118">Az.FrontDoor</span></span>
* <span data-ttu-id="01289-119">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-119">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="01289-120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="01289-120">Az.IotHub</span></span>
* <span data-ttu-id="01289-121">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-121">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="01289-122">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="01289-122">New Cmdlets are:</span></span>
    - <span data-ttu-id="01289-123">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="01289-123">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="01289-124">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="01289-124">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="01289-125">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="01289-125">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="01289-126">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="01289-126">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="01289-127">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="01289-127">Az.KeyVault</span></span>
* <span data-ttu-id="01289-128">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-128">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="01289-129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="01289-129">Az.Monitor</span></span>
* <span data-ttu-id="01289-130">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-130">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="01289-131">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-131">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="01289-132">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="01289-132">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-133">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-133">Az.Network</span></span>
* <span data-ttu-id="01289-134">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-134">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="01289-135">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-135">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="01289-136">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-136">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="01289-137">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="01289-137">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="01289-138">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="01289-138">No new cmdlets are added.</span></span> <span data-ttu-id="01289-139">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="01289-139">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-140">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-141">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-141">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-142">Az.Resources</span></span>
* <span data-ttu-id="01289-143">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="01289-143">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="01289-144">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="01289-144">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="01289-145">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="01289-145">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="01289-146">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="01289-146">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="01289-147">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="01289-147">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="01289-148">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-148">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="01289-149">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-149">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="01289-150">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="01289-150">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-151">Az.Sql</span></span>
* <span data-ttu-id="01289-152">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-152">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="01289-153">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-153">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="01289-154">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="01289-154">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="01289-155">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="01289-155">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="01289-156">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-156">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="01289-157">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="01289-157">Az.StorageSync</span></span>
* <span data-ttu-id="01289-158">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-158">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="01289-159">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="01289-159">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="01289-160">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="01289-160">Highlights since the last major release</span></span>
* <span data-ttu-id="01289-161">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="01289-161">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="01289-162">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-162">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="01289-163">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-163">Az.Accounts</span></span>
* <span data-ttu-id="01289-164">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="01289-164">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="01289-165">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-165">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="01289-166">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="01289-166">Az.ApiManagement</span></span>
* <span data-ttu-id="01289-167">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="01289-167">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="01289-168">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="01289-168">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="01289-169">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-169">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="01289-170">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-170">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-171">Az.Compute</span></span>
* <span data-ttu-id="01289-172">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="01289-172">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="01289-173">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-173">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="01289-174">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-174">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="01289-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="01289-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="01289-176">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-176">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-177">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-177">Az.DataFactory</span></span>
* <span data-ttu-id="01289-178">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-178">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="01289-179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="01289-179">Az.DeploymentManager</span></span>
* <span data-ttu-id="01289-180">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="01289-180">Adds LIST operations for resources</span></span>
* <span data-ttu-id="01289-181">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="01289-181">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="01289-182">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="01289-182">Az.HDInsight</span></span>
* <span data-ttu-id="01289-183">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-183">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="01289-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="01289-184">Az.KeyVault</span></span>
* <span data-ttu-id="01289-185">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-185">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-186">Az.Network</span></span>
* <span data-ttu-id="01289-187">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-187">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="01289-188">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="01289-188">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="01289-189">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="01289-190">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-190">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="01289-191">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="01289-191">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="01289-192">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-192">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="01289-193">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-193">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="01289-194">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-194">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="01289-195">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-195">New cmdlets added:</span></span>
        - <span data-ttu-id="01289-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="01289-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="01289-197">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-197">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="01289-198">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="01289-198">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="01289-199">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-199">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="01289-200">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="01289-200">Az.PolicyInsights</span></span>
* <span data-ttu-id="01289-201">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="01289-201">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="01289-202">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-202">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="01289-203">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-203">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="01289-204">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-204">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-206">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-206">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="01289-207">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="01289-207">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-208">Az.Resources</span></span>
* <span data-ttu-id="01289-209">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="01289-209">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="01289-210">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-210">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-211">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-211">Az.Sql</span></span>
<span data-ttu-id="01289-212">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-212">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-213">Az.Storage</span></span>
* <span data-ttu-id="01289-214">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="01289-214">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="01289-215">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-215">New-AzStorageAccount</span></span>
* <span data-ttu-id="01289-216">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="01289-216">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="01289-217">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-217">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-218">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-218">Az.Websites</span></span>
* <span data-ttu-id="01289-219">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="01289-219">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="01289-220">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-220">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="01289-221">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="01289-221">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="01289-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-222">Az.Accounts</span></span>
* <span data-ttu-id="01289-223">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-223">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="01289-224">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="01289-224">Az.Cdn</span></span>
* <span data-ttu-id="01289-225">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="01289-225">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-226">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-226">Az.Compute</span></span>
* <span data-ttu-id="01289-227">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-227">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="01289-228">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="01289-228">Az.ContainerInstance</span></span>
* <span data-ttu-id="01289-229">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-229">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="01289-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="01289-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="01289-231">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-231">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="01289-232">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="01289-232">Get the Edge Storage Container</span></span>
* <span data-ttu-id="01289-233">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-233">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="01289-234">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="01289-234">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="01289-235">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-235">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="01289-236">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="01289-236">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="01289-237">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-237">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="01289-238">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="01289-238">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="01289-239">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-239">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="01289-240">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="01289-240">Get the Edge Storage Account</span></span>
* <span data-ttu-id="01289-241">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-241">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="01289-242">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="01289-242">Create new Edge Storage Account</span></span>
* <span data-ttu-id="01289-243">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-243">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="01289-244">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="01289-244">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="01289-245">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="01289-245">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="01289-246">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="01289-246">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="01289-247">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-247">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="01289-248">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="01289-248">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-249">Az.DataFactory</span></span>
* <span data-ttu-id="01289-250">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-250">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="01289-251">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-251">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="01289-252">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-252">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="01289-253">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="01289-253">Az.DevTestLabs</span></span>
* <span data-ttu-id="01289-254">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-254">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="01289-255">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="01289-255">Az.EventHub</span></span>
* <span data-ttu-id="01289-256">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-256">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="01289-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="01289-257">Az.HDInsight</span></span>
* <span data-ttu-id="01289-258">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-258">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="01289-259">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="01289-259">Az.MachineLearning</span></span>
* <span data-ttu-id="01289-260">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-260">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="01289-261">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="01289-261">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="01289-262">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="01289-262">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="01289-263">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="01289-263">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="01289-264">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="01289-264">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="01289-265">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="01289-265">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="01289-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="01289-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="01289-267">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="01289-267">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-268">Az.Network</span></span>
* <span data-ttu-id="01289-269">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="01289-269">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-270">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-270">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-271">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-271">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="01289-272">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-272">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="01289-273">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-273">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="01289-274">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-274">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-275">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-275">Az.Resources</span></span>
* <span data-ttu-id="01289-276">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-276">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-277">Az.Sql</span></span>
* <span data-ttu-id="01289-278">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-278">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="01289-279">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-279">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="01289-280">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="01289-280">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="01289-281">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-281">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-282">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-282">Az.Storage</span></span>
* <span data-ttu-id="01289-283">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-283">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="01289-284">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="01289-284">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="01289-285">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="01289-285">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="01289-286">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-286">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="01289-287">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="01289-287">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="01289-288">Genel</span><span class="sxs-lookup"><span data-stu-id="01289-288">General</span></span>
* <span data-ttu-id="01289-289">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-289">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="01289-290">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-290">Az.Accounts</span></span>
* <span data-ttu-id="01289-291">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="01289-291">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="01289-292">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="01289-292">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="01289-293">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="01289-293">Az.Batch</span></span>
* <span data-ttu-id="01289-294">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-294">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-295">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-295">Az.DataFactory</span></span>
* <span data-ttu-id="01289-296">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-296">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="01289-297">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="01289-297">Az.FrontDoor</span></span>
* <span data-ttu-id="01289-298">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-298">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="01289-299">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-299">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="01289-300">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="01289-300">Az.HealthcareApis</span></span>
* <span data-ttu-id="01289-301">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="01289-301">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="01289-302">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="01289-302">Az.KeyVault</span></span>
* <span data-ttu-id="01289-303">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-303">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="01289-304">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="01289-304">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="01289-305">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-305">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="01289-306">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="01289-306">Az.Monitor</span></span>
* <span data-ttu-id="01289-307">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-307">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="01289-308">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="01289-308">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="01289-309">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="01289-309">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-310">Az.Network</span></span>
* <span data-ttu-id="01289-311">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-311">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-312">Az.Resources</span></span>
* <span data-ttu-id="01289-313">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-313">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="01289-314">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-314">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-315">Az.Sql</span></span>
* <span data-ttu-id="01289-316">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="01289-316">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-317">Az.Storage</span></span>
* <span data-ttu-id="01289-318">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="01289-318">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="01289-319">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="01289-319">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="01289-320">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="01289-320">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="01289-321">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="01289-321">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="01289-322">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="01289-322">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="01289-323">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-323">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="01289-324">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-324">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="01289-325">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="01289-325">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="01289-326">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="01289-326">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="01289-327">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-327">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="01289-328">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="01289-328">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="01289-329">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-329">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="01289-330">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="01289-330">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="01289-331">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="01289-331">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="01289-332">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="01289-332">Highlights since the last major release</span></span>
* <span data-ttu-id="01289-333">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="01289-333">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="01289-334">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="01289-334">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-335">Az.Compute</span></span>
* <span data-ttu-id="01289-336">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="01289-336">VM Reapply feature</span></span>
    - <span data-ttu-id="01289-337">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="01289-337">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="01289-338">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="01289-338">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="01289-339">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="01289-339">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="01289-340">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="01289-340">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="01289-341">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-341">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="01289-342">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-342">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="01289-343">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-343">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="01289-344">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-344">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="01289-345">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-345">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="01289-346">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-346">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="01289-347">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="01289-347">Az.DataBoxEdge</span></span>
* <span data-ttu-id="01289-348">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-348">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="01289-349">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="01289-349">Get the Order</span></span>
* <span data-ttu-id="01289-350">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-350">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="01289-351">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="01289-351">Create new Order</span></span>
* <span data-ttu-id="01289-352">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-352">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="01289-353">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="01289-353">Remove the Order</span></span>
* <span data-ttu-id="01289-354">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="01289-354">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="01289-355">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="01289-355">Now creates Local Share</span></span>
* <span data-ttu-id="01289-356">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-356">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="01289-357">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="01289-357">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="01289-358">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-358">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="01289-359">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="01289-359">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="01289-360">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-360">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="01289-361">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="01289-361">Gets the information about Triggers</span></span>
* <span data-ttu-id="01289-362">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-362">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="01289-363">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="01289-363">Create new Triggers</span></span>
* <span data-ttu-id="01289-364">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-364">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="01289-365">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="01289-365">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-366">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-366">Az.DataFactory</span></span>
* <span data-ttu-id="01289-367">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-367">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="01289-368">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-368">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="01289-369">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-369">Az.DataLakeStore</span></span>
* <span data-ttu-id="01289-370">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-370">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="01289-371">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="01289-371">Az.EventHub</span></span>
* <span data-ttu-id="01289-372">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-372">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="01289-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="01289-373">Az.FrontDoor</span></span>
* <span data-ttu-id="01289-374">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-374">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="01289-375">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-375">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="01289-376">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-376">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="01289-377">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="01289-377">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-378">Az.Network</span></span>
* <span data-ttu-id="01289-379">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-379">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="01289-380">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="01289-380">Az.PrivateDns</span></span>
* <span data-ttu-id="01289-381">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-381">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-383">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-383">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="01289-384">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="01289-384">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="01289-385">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-385">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="01289-386">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="01289-386">Az.RedisCache</span></span>
* <span data-ttu-id="01289-387">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-387">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="01289-388">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-388">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="01289-389">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-389">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-390">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-390">Az.Resources</span></span>
- <span data-ttu-id="01289-391">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-391">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="01289-392">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-392">Updated create policy definition help example</span></span>
- <span data-ttu-id="01289-393">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-393">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="01289-394">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-394">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="01289-395">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-395">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-396">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-396">Az.Sql</span></span>
* <span data-ttu-id="01289-397">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-397">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="01289-398">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-398">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="01289-399">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="01289-399">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="01289-400">Genel</span><span class="sxs-lookup"><span data-stu-id="01289-400">General</span></span>
* <span data-ttu-id="01289-401">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="01289-401">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="01289-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-402">Az.Accounts</span></span>
* <span data-ttu-id="01289-403">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="01289-403">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="01289-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="01289-404">Az.Advisor</span></span>
* <span data-ttu-id="01289-405">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-405">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="01289-406">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="01289-406">Az.Batch</span></span>
* <span data-ttu-id="01289-407">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-407">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="01289-408">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="01289-408">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="01289-409">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="01289-409">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="01289-410">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="01289-410">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="01289-411">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="01289-411">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="01289-412">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="01289-412">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="01289-413">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="01289-413">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="01289-414">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="01289-414">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="01289-415">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="01289-415">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="01289-416">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-416">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="01289-417">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="01289-417">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="01289-418">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="01289-418">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="01289-419">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-419">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="01289-420">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="01289-420">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="01289-421">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-421">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="01289-422">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-422">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="01289-423">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-423">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="01289-424">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-424">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="01289-425">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-425">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="01289-426">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="01289-426">This operation is no longer supported.</span></span>
* <span data-ttu-id="01289-427">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-427">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="01289-428">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-428">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="01289-429">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-429">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="01289-430">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="01289-430">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="01289-431">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="01289-431">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="01289-432">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="01289-432">New non-verified images are also now returned.</span></span> <span data-ttu-id="01289-433">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="01289-433">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="01289-434">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-434">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="01289-435">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="01289-435">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="01289-436">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="01289-436">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="01289-437">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="01289-437">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="01289-438">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="01289-438">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="01289-439">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-439">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="01289-440">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="01289-440">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="01289-441">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="01289-441">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="01289-442">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="01289-442">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="01289-443">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="01289-443">Az.Cdn</span></span>
* <span data-ttu-id="01289-444">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-444">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="01289-445">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-445">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-446">Az.Compute</span></span>
* <span data-ttu-id="01289-447">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="01289-447">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="01289-448">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="01289-448">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="01289-449">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="01289-449">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="01289-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="01289-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="01289-451">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="01289-451">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="01289-452">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-452">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="01289-453">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="01289-453">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="01289-454">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-454">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="01289-455">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="01289-455">Breaking changes</span></span>
    - <span data-ttu-id="01289-456">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="01289-456">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="01289-457">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="01289-457">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-458">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-458">Az.DataFactory</span></span>
* <span data-ttu-id="01289-459">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-459">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="01289-460">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-460">Az.DataLakeStore</span></span>
* <span data-ttu-id="01289-461">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="01289-461">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="01289-462">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="01289-462">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="01289-463">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="01289-463">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="01289-464">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="01289-464">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="01289-465">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="01289-465">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="01289-466">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="01289-466">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="01289-467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="01289-467">Az.FrontDoor</span></span>
* <span data-ttu-id="01289-468">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-468">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="01289-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="01289-469">Az.HDInsight</span></span>
* <span data-ttu-id="01289-470">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-470">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="01289-471">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-471">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="01289-472">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="01289-472">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="01289-473">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="01289-473">Removed five cmdlets:</span></span>
    - <span data-ttu-id="01289-474">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="01289-474">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="01289-475">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="01289-475">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="01289-476">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="01289-476">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="01289-477">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="01289-477">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="01289-478">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="01289-478">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="01289-479">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-479">Added three cmdlets:</span></span>
    - <span data-ttu-id="01289-480">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="01289-480">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="01289-481">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="01289-481">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="01289-482">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="01289-482">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="01289-483">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-483">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="01289-484">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-484">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="01289-485">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-485">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="01289-486">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-486">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="01289-487">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-487">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="01289-488">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-488">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="01289-489">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-489">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="01289-490">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-490">Added some scenario test cases.</span></span>
* <span data-ttu-id="01289-491">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="01289-491">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="01289-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="01289-492">Az.IotHub</span></span>
* <span data-ttu-id="01289-493">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="01289-493">Breaking changes:</span></span>
    - <span data-ttu-id="01289-494">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="01289-494">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="01289-495">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-495">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="01289-496">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="01289-496">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="01289-497">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-497">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="01289-498">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-498">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="01289-499">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-499">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="01289-500">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="01289-500">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="01289-501">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="01289-501">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="01289-502">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="01289-502">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="01289-503">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-503">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="01289-504">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="01289-504">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="01289-505">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-505">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-506">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-506">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-507">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-507">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="01289-508">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-508">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="01289-509">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-509">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="01289-510">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-510">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="01289-511">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-511">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="01289-512">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-512">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="01289-513">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-513">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="01289-514">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-514">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="01289-515">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-515">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-516">Az.Resources</span></span>
* <span data-ttu-id="01289-517">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-517">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-518">Az.Network</span></span>
* <span data-ttu-id="01289-519">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-519">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="01289-520">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-520">Updated cmdlet:</span></span>
        - <span data-ttu-id="01289-521">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="01289-521">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="01289-522">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="01289-522">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="01289-523">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="01289-523">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="01289-524">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="01289-524">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="01289-525">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="01289-525">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="01289-526">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="01289-526">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="01289-527">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="01289-527">New cmdlet:</span></span>
        - <span data-ttu-id="01289-528">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="01289-528">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="01289-529">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-529">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="01289-530">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-530">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="01289-531">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-531">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="01289-532">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-532">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="01289-533">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-533">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="01289-534">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-534">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="01289-535">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-535">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="01289-536">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-536">New cmdlets added:</span></span>
        - <span data-ttu-id="01289-537">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="01289-537">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="01289-538">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="01289-538">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="01289-539">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="01289-539">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="01289-540">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="01289-540">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="01289-541">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="01289-541">Set-AzVirtualHub</span></span>
* <span data-ttu-id="01289-542">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-542">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="01289-543">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-543">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="01289-544">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-544">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="01289-545">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-545">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="01289-546">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-546">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="01289-547">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-547">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="01289-548">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-548">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="01289-549">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-549">New cmdlets added:</span></span>
        - <span data-ttu-id="01289-550">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="01289-550">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="01289-551">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-551">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="01289-552">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-552">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="01289-553">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-553">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="01289-554">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-554">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="01289-555">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-555">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="01289-556">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-556">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="01289-557">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-557">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="01289-558">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-558">New cmdlets added:</span></span>
        - <span data-ttu-id="01289-559">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="01289-559">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="01289-560">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="01289-560">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="01289-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="01289-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="01289-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="01289-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="01289-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="01289-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="01289-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="01289-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="01289-565">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-565">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="01289-566">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-566">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="01289-567">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-567">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="01289-568">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-568">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="01289-569">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-569">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="01289-570">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-570">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="01289-571">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-571">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="01289-572">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-572">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="01289-573">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-573">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="01289-574">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="01289-574">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="01289-575">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-575">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="01289-576">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-576">New cmdlets added:</span></span>
        - <span data-ttu-id="01289-577">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="01289-577">New-AzIpGroup</span></span>
        - <span data-ttu-id="01289-578">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="01289-578">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="01289-579">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="01289-579">Get-AzIpGroup</span></span>
        - <span data-ttu-id="01289-580">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="01289-580">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="01289-581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="01289-581">Az.ServiceFabric</span></span>
* <span data-ttu-id="01289-582">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-582">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-583">Az.Sql</span></span>
* <span data-ttu-id="01289-584">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-584">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="01289-585">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-585">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="01289-586">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="01289-586">Removed deprecated aliases:</span></span>
* <span data-ttu-id="01289-587">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="01289-587">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="01289-588">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="01289-588">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="01289-589">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-589">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="01289-590">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-590">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="01289-591">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="01289-591">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="01289-592">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-592">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-593">Az.Storage</span></span>
* <span data-ttu-id="01289-594">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="01289-594">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="01289-595">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-595">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="01289-596">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-596">Set-AzStorageAccount</span></span>
* <span data-ttu-id="01289-597">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="01289-597">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="01289-598">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="01289-598">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="01289-599">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="01289-599">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="01289-600">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="01289-600">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="01289-601">Genel</span><span class="sxs-lookup"><span data-stu-id="01289-601">General</span></span>
* <span data-ttu-id="01289-602">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="01289-602">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="01289-603">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-603">Az.Accounts</span></span>
* <span data-ttu-id="01289-604">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-604">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="01289-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="01289-605">Az.ApiManagement</span></span>
* <span data-ttu-id="01289-606">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-606">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="01289-607">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-607">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="01289-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="01289-608">Az.Automation</span></span>
* <span data-ttu-id="01289-609">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-609">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="01289-610">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="01289-610">Az.Batch</span></span>
* <span data-ttu-id="01289-611">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="01289-611">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-612">Az.Compute</span></span>
* <span data-ttu-id="01289-613">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-613">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="01289-614">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-614">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="01289-615">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-615">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="01289-616">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-616">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-617">Az.DataFactory</span></span>
* <span data-ttu-id="01289-618">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="01289-618">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="01289-619">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="01289-619">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="01289-620">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-620">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="01289-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="01289-622">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-622">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="01289-623">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="01289-623">Az.HealthcareApis</span></span>
* <span data-ttu-id="01289-624">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-624">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="01289-625">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-625">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="01289-626">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-626">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="01289-627">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-627">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="01289-628">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="01289-628">Az.IotHub</span></span>
* <span data-ttu-id="01289-629">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="01289-629">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="01289-630">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="01289-630">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="01289-631">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="01289-631">Az.Monitor</span></span>
* <span data-ttu-id="01289-632">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-632">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="01289-633">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="01289-633">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="01289-634">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="01289-634">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="01289-635">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="01289-635">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-636">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-636">Az.Network</span></span>
* <span data-ttu-id="01289-637">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-637">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="01289-638">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-638">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="01289-639">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-639">New cmdlets added:</span></span>
        - <span data-ttu-id="01289-640">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="01289-640">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="01289-641">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="01289-641">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="01289-642">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-642">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="01289-643">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-643">Updated cmdlets:</span></span>
        - <span data-ttu-id="01289-644">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01289-644">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="01289-645">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01289-645">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="01289-646">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01289-646">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="01289-647">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-647">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="01289-648">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="01289-648">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="01289-649">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="01289-649">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="01289-650">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="01289-650">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="01289-651">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="01289-651">Az.RedisCache</span></span>
* <span data-ttu-id="01289-652">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-652">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-653">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-653">Az.Sql</span></span>
* <span data-ttu-id="01289-654">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-654">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-655">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-655">Az.Storage</span></span>
* <span data-ttu-id="01289-656">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="01289-656">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="01289-657">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="01289-657">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="01289-658">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="01289-658">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="01289-659">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="01289-659">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="01289-660">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-660">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="01289-661">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="01289-661">Az.StorageSync</span></span>
* <span data-ttu-id="01289-662">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-662">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-663">Az.Websites</span></span>
* <span data-ttu-id="01289-664">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="01289-664">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="01289-665">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="01289-665">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="01289-666">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="01289-666">Az.ApiManagement</span></span>
* <span data-ttu-id="01289-667">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-667">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="01289-668">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-668">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="01289-669">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="01289-669">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="01289-670">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="01289-670">Az.Automation</span></span>
* <span data-ttu-id="01289-671">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-671">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="01289-672">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-672">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="01289-673">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-673">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-674">Az.Compute</span></span>
* <span data-ttu-id="01289-675">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-675">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="01289-676">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-676">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="01289-677">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-677">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="01289-678">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-678">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="01289-679">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-679">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="01289-680">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-680">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="01289-681">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-681">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="01289-682">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-682">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="01289-683">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-683">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-684">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-684">Az.DataFactory</span></span>
* <span data-ttu-id="01289-685">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="01289-685">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="01289-686">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-686">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="01289-687">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="01289-687">Az.HDInsight</span></span>
* <span data-ttu-id="01289-688">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="01289-688">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="01289-689">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="01289-689">Az.IotHub</span></span>
* <span data-ttu-id="01289-690">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-690">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="01289-691">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-691">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="01289-692">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="01289-692">New cmdlets are:</span></span>
    - <span data-ttu-id="01289-693">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="01289-693">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="01289-694">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="01289-694">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="01289-695">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="01289-695">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="01289-696">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="01289-696">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="01289-697">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="01289-697">Az.Monitor</span></span>
* <span data-ttu-id="01289-698">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="01289-698">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="01289-699">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="01289-699">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="01289-700">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="01289-700">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="01289-701">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="01289-701">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="01289-702">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-702">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="01289-703">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-703">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="01289-704">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="01289-704">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="01289-705">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="01289-705">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="01289-706">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-706">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="01289-707">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="01289-707">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="01289-708">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-708">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="01289-709">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="01289-709">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="01289-710">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-710">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="01289-711">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="01289-711">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="01289-712">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="01289-712">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="01289-713">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="01289-713">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="01289-714">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="01289-714">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="01289-715">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="01289-715">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="01289-716">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-716">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="01289-717">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-717">Overall improved help files</span></span>
* <span data-ttu-id="01289-718">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-718">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-719">Az.Network</span></span>
* <span data-ttu-id="01289-720">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-720">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="01289-721">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-721">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="01289-722">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-722">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="01289-723">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-723">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="01289-724">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-724">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="01289-725">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-725">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="01289-726">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-726">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="01289-727">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-727">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="01289-728">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-728">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="01289-729">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-729">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="01289-730">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-730">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="01289-731">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="01289-731">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="01289-732">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-732">New cmdlets</span></span>
        - <span data-ttu-id="01289-733">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="01289-733">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="01289-734">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="01289-734">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="01289-735">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-735">Updated cmdlet:</span></span>
        - <span data-ttu-id="01289-736">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="01289-736">New-VpnSite</span></span>
        - <span data-ttu-id="01289-737">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="01289-737">Update-VpnSite</span></span>
        - <span data-ttu-id="01289-738">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="01289-738">New-VpnConnection</span></span>
        - <span data-ttu-id="01289-739">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="01289-739">Update-VpnConnection</span></span>
* <span data-ttu-id="01289-740">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-740">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-741">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-741">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-742">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-742">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="01289-743">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-743">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-744">Az.Resources</span></span>
* <span data-ttu-id="01289-745">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-745">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="01289-746">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="01289-746">Az.ServiceFabric</span></span>
* <span data-ttu-id="01289-747">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-747">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="01289-748">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="01289-748">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="01289-749">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="01289-749">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="01289-750">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="01289-750">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="01289-751">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="01289-751">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="01289-752">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="01289-752">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="01289-753">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="01289-753">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="01289-754">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="01289-754">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="01289-755">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="01289-755">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="01289-756">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="01289-756">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="01289-757">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="01289-757">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="01289-758">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="01289-758">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="01289-759">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="01289-759">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="01289-760">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="01289-760">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="01289-761">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="01289-761">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="01289-762">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-762">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="01289-763">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="01289-763">Az.SignalR</span></span>
* <span data-ttu-id="01289-764">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-764">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-765">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-765">Az.Sql</span></span>
* <span data-ttu-id="01289-766">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-766">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="01289-767">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-767">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="01289-768">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-768">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="01289-769">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-769">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="01289-770">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-770">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-771">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-771">Az.Storage</span></span>
* <span data-ttu-id="01289-772">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-772">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="01289-773">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-773">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="01289-774">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="01289-774">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="01289-775">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="01289-775">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="01289-776">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-776">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="01289-777">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="01289-777">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="01289-778">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-778">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="01289-779">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="01289-779">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="01289-780">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="01289-780">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="01289-781">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="01289-781">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="01289-782">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="01289-782">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-783">Az.Websites</span></span>
* <span data-ttu-id="01289-784">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="01289-784">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="01289-785">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="01289-785">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="01289-786">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-786">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="01289-787">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="01289-787">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="01289-788">Genel</span><span class="sxs-lookup"><span data-stu-id="01289-788">General</span></span>
* <span data-ttu-id="01289-789">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-789">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="01289-790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-790">Az.Accounts</span></span>
* <span data-ttu-id="01289-791">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="01289-791">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="01289-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="01289-792">Az.Aks</span></span>
* <span data-ttu-id="01289-793">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-793">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="01289-794">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="01289-794">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="01289-795">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="01289-795">Az.ApiManagement</span></span>
* <span data-ttu-id="01289-796">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-796">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="01289-797">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-797">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="01289-798">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-798">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="01289-799">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="01289-799">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="01289-800">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-800">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="01289-801">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="01289-801">Az.Batch</span></span>
* <span data-ttu-id="01289-802">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-802">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="01289-803">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="01289-803">Az.Cdn</span></span>
* <span data-ttu-id="01289-804">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-804">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-805">Az.Compute</span></span>
* <span data-ttu-id="01289-806">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-806">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="01289-807">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-807">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="01289-808">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-808">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="01289-809">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-809">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="01289-810">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="01289-810">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="01289-811">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-811">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="01289-812">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-812">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="01289-813">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-813">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-814">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-814">Az.DataFactory</span></span>
* <span data-ttu-id="01289-815">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-815">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="01289-816">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-816">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="01289-817">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-817">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="01289-818">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-818">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="01289-819">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-819">Az.DataLakeStore</span></span>
* <span data-ttu-id="01289-820">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-820">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="01289-821">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="01289-821">Az.EventHub</span></span>
* <span data-ttu-id="01289-822">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="01289-822">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="01289-823">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="01289-823">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="01289-824">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-824">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="01289-825">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="01289-825">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="01289-826">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="01289-826">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="01289-827">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-827">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="01289-828">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="01289-828">Az.Monitor</span></span>
* <span data-ttu-id="01289-829">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-829">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-830">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-830">Az.Network</span></span>
* <span data-ttu-id="01289-831">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-831">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="01289-832">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-832">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="01289-833">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-833">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="01289-834">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="01289-834">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="01289-835">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="01289-835">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="01289-836">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-836">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="01289-837">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-837">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="01289-838">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="01289-838">Az.OperationalInsights</span></span>
* <span data-ttu-id="01289-839">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-839">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="01289-840">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-840">Added example</span></span>
    - <span data-ttu-id="01289-841">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-841">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="01289-842">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-842">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="01289-843">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-843">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-844">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-844">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-845">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-845">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-846">Az.Resources</span></span>
* <span data-ttu-id="01289-847">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-847">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="01289-848">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-848">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="01289-849">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="01289-849">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="01289-850">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-850">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="01289-851">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="01289-851">Az.ServiceBus</span></span>
* <span data-ttu-id="01289-852">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="01289-852">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="01289-853">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="01289-853">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="01289-854">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-854">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="01289-855">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="01289-855">Az.ServiceFabric</span></span>
* <span data-ttu-id="01289-856">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="01289-856">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="01289-857">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="01289-857">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="01289-858">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="01289-858">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="01289-859">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-859">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="01289-860">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="01289-860">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="01289-861">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-861">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-862">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-862">Az.Sql</span></span>
* <span data-ttu-id="01289-863">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-863">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-864">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-864">Az.Storage</span></span>
* <span data-ttu-id="01289-865">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-865">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="01289-866">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="01289-866">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="01289-867">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="01289-867">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="01289-868">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="01289-868">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="01289-869">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="01289-869">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="01289-870">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="01289-870">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-871">Az.Websites</span></span>
* <span data-ttu-id="01289-872">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-872">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="01289-873">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="01289-873">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="01289-874">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-874">Az.Accounts</span></span>
* <span data-ttu-id="01289-875">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-875">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="01289-876">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="01289-876">Az.ApplicationInsights</span></span>
* <span data-ttu-id="01289-877">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-877">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="01289-878">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="01289-878">Az.Automation</span></span>
* <span data-ttu-id="01289-879">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-879">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="01289-880">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="01289-880">Az.CognitiveServices</span></span>
* <span data-ttu-id="01289-881">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-881">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-882">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-882">Az.Compute</span></span>
* <span data-ttu-id="01289-883">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-883">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="01289-884">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="01289-884">Az.ContainerRegistry</span></span>
* <span data-ttu-id="01289-885">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-885">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="01289-886">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="01289-886">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-887">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-887">Az.DataFactory</span></span>
* <span data-ttu-id="01289-888">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-888">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="01289-889">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-889">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="01289-890">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="01289-890">Az.EventHub</span></span>
* <span data-ttu-id="01289-891">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="01289-891">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="01289-892">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-892">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="01289-893">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="01289-893">Az.KeyVault</span></span>
* <span data-ttu-id="01289-894">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-894">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="01289-895">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="01289-895">Az.LogicApp</span></span>
* <span data-ttu-id="01289-896">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="01289-896">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="01289-897">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-897">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="01289-898">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="01289-898">Az.ManagedServices</span></span>
* <span data-ttu-id="01289-899">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="01289-899">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-900">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-900">Az.Network</span></span>
* <span data-ttu-id="01289-901">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-901">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="01289-902">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-902">New cmdlets</span></span>
        - <span data-ttu-id="01289-903">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="01289-903">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="01289-904">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="01289-904">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="01289-905">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="01289-905">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="01289-906">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="01289-906">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="01289-907">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="01289-907">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="01289-908">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="01289-908">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="01289-909">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="01289-909">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="01289-910">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="01289-910">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="01289-911">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="01289-911">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="01289-912">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-912">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="01289-913">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-913">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="01289-914">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-914">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="01289-915">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-915">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="01289-916">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-916">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="01289-917">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-917">Updated cmdlets</span></span>
        - <span data-ttu-id="01289-918">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01289-918">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="01289-919">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01289-919">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="01289-920">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01289-920">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="01289-921">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-921">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="01289-922">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-922">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="01289-923">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-923">Updated cmdlet:</span></span>
        - <span data-ttu-id="01289-924">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="01289-924">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="01289-925">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="01289-925">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="01289-926">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="01289-926">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="01289-927">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-927">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="01289-928">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-928">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="01289-929">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="01289-929">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="01289-930">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="01289-930">Az.OperationalInsights</span></span>
* <span data-ttu-id="01289-931">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-931">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="01289-932">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-932">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-933">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-933">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-934">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-934">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="01289-935">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-935">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="01289-936">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-936">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="01289-937">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-937">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="01289-938">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-938">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="01289-939">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-939">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="01289-940">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-940">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="01289-941">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-941">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="01289-942">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-942">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="01289-943">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-943">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-944">Az.Resources</span></span>
- <span data-ttu-id="01289-945">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-945">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="01289-946">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-946">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="01289-947">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="01289-947">Az.ServiceBus</span></span>
* <span data-ttu-id="01289-948">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="01289-948">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="01289-949">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-949">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-950">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-950">Az.Sql</span></span>
* <span data-ttu-id="01289-951">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-951">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="01289-952">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-952">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="01289-953">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-953">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-954">Az.Storage</span></span>
* <span data-ttu-id="01289-955">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-955">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="01289-956">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="01289-956">Az.StorageSync</span></span>
* <span data-ttu-id="01289-957">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="01289-957">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="01289-958">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-958">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-959">Az.Websites</span></span>
* <span data-ttu-id="01289-960">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-960">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="01289-961">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-961">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="01289-962">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-962">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="01289-963">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="01289-963">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="01289-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-964">Az.Accounts</span></span>
* <span data-ttu-id="01289-965">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-965">Add support for profile cmdlets</span></span>
* <span data-ttu-id="01289-966">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-966">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="01289-967">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-967">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="01289-968">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="01289-968">Az.Advisor</span></span>
* <span data-ttu-id="01289-969">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="01289-969">GA release of Az.Advisor</span></span>
* <span data-ttu-id="01289-970">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="01289-970">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="01289-971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="01289-971">Az.ApiManagement</span></span>
* <span data-ttu-id="01289-972">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-972">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="01289-973">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="01289-973">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="01289-974">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-974">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="01289-975">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="01289-975">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="01289-976">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="01289-976">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="01289-977">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="01289-977">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="01289-978">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-978">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="01289-979">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="01289-979">Az.Automation</span></span>
* <span data-ttu-id="01289-980">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-980">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-981">Az.Compute</span></span>
* <span data-ttu-id="01289-982">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-982">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-983">Az.DataFactory</span></span>
* <span data-ttu-id="01289-984">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="01289-984">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="01289-985">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="01289-985">Az.EventGrid</span></span>
* <span data-ttu-id="01289-986">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-986">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="01289-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="01289-987">Az.IotHub</span></span>
* <span data-ttu-id="01289-988">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-988">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-989">Az.Network</span></span>
* <span data-ttu-id="01289-990">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-990">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="01289-991">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-991">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="01289-992">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="01289-992">Az.PolicyInsights</span></span>
* <span data-ttu-id="01289-993">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-993">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="01289-994">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="01289-994">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="01289-995">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="01289-995">Az.OperationalInsights</span></span>
* <span data-ttu-id="01289-996">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-996">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-997">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-997">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-998">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="01289-998">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-999">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-999">Az.Resources</span></span>
    - <span data-ttu-id="01289-1000">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="01289-1000">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="01289-1001">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1001">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="01289-1002">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1002">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="01289-1003">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1003">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="01289-1004">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="01289-1004">Az.ServiceBus</span></span>
* <span data-ttu-id="01289-1005">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1005">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-1006">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1006">Az.Sql</span></span>
* <span data-ttu-id="01289-1007">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1007">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="01289-1008">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-1008">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="01289-1009">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="01289-1009">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="01289-1010">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="01289-1010">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="01289-1011">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="01289-1011">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="01289-1012">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="01289-1012">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="01289-1013">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="01289-1013">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="01289-1014">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="01289-1014">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="01289-1015">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-1015">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-1016">Az.Storage</span></span>
* <span data-ttu-id="01289-1017">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-1017">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="01289-1018">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="01289-1018">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="01289-1019">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1019">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="01289-1020">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="01289-1020">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="01289-1021">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1021">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="01289-1022">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-1022">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="01289-1023">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-1023">Set-AzStorageAccount</span></span>
* <span data-ttu-id="01289-1024">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1024">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="01289-1025">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="01289-1025">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="01289-1026">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="01289-1026">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="01289-1027">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="01289-1027">Az.StorageSync</span></span>
* <span data-ttu-id="01289-1028">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="01289-1028">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="01289-1029">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1029">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="01289-1030">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-1030">Az.Accounts</span></span>
* <span data-ttu-id="01289-1031">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1031">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="01289-1032">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="01289-1032">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="01289-1033">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1033">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="01289-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="01289-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="01289-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="01289-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1036">Az.Compute</span></span>
* <span data-ttu-id="01289-1037">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="01289-1037">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="01289-1038">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1038">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="01289-1039">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="01289-1039">Az.Dns</span></span>
* <span data-ttu-id="01289-1040">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1040">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="01289-1041">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="01289-1041">Az.EventGrid</span></span>
* <span data-ttu-id="01289-1042">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1042">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="01289-1043">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="01289-1043">New cmdlets:</span></span>
    - <span data-ttu-id="01289-1044">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="01289-1044">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="01289-1045">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01289-1045">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="01289-1046">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="01289-1046">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="01289-1047">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="01289-1047">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="01289-1048">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="01289-1048">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="01289-1049">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="01289-1049">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="01289-1050">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="01289-1050">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="01289-1051">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="01289-1051">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="01289-1052">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="01289-1052">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="01289-1053">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="01289-1053">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="01289-1054">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="01289-1054">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="01289-1055">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01289-1055">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="01289-1056">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="01289-1056">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="01289-1057">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="01289-1057">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="01289-1058">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="01289-1058">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="01289-1059">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="01289-1059">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="01289-1060">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-1060">Updated cmdlets:</span></span>
    - <span data-ttu-id="01289-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="01289-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="01289-1062">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="01289-1062">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="01289-1063">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="01289-1063">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="01289-1064">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="01289-1064">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="01289-1065">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-1065">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="01289-1066">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="01289-1066">Event subscription expiration date,</span></span>
            - <span data-ttu-id="01289-1067">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="01289-1067">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="01289-1068">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="01289-1068">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="01289-1069">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="01289-1069">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="01289-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="01289-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="01289-1071">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="01289-1071">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="01289-1072">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="01289-1072">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="01289-1073">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="01289-1073">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="01289-1074">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="01289-1074">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="01289-1075">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="01289-1075">Az.FrontDoor</span></span>
* <span data-ttu-id="01289-1076">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="01289-1076">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="01289-1077">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="01289-1077">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="01289-1078">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="01289-1078">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="01289-1079">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="01289-1079">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1080">Az.Network</span></span>
* <span data-ttu-id="01289-1081">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="01289-1081">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="01289-1082">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-1082">New cmdlets</span></span>
        - <span data-ttu-id="01289-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="01289-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="01289-1084">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="01289-1084">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="01289-1085">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-1085">New cmdlets</span></span> 
        - <span data-ttu-id="01289-1086">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="01289-1086">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="01289-1087">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="01289-1087">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="01289-1088">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-1088">New cmdlets</span></span> 
        - <span data-ttu-id="01289-1089">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="01289-1089">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="01289-1090">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="01289-1090">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="01289-1091">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="01289-1091">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="01289-1092">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="01289-1092">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="01289-1093">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="01289-1093">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="01289-1094">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="01289-1094">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="01289-1095">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-1095">New cmdlets</span></span>
        - <span data-ttu-id="01289-1096">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="01289-1096">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="01289-1097">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="01289-1097">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="01289-1098">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="01289-1098">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="01289-1099">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="01289-1099">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="01289-1100">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="01289-1100">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="01289-1101">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1101">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="01289-1102">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1102">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="01289-1103">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1103">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="01289-1104">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1104">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="01289-1105">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1105">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="01289-1106">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1106">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="01289-1107">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1107">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="01289-1108">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1108">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="01289-1109">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1109">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="01289-1110">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1110">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="01289-1111">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1111">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="01289-1112">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1112">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="01289-1113">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1113">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="01289-1114">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-1114">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="01289-1115">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1115">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="01289-1116">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1116">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="01289-1117">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="01289-1117">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="01289-1118">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="01289-1118">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="01289-1119">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="01289-1119">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="01289-1120">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1120">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="01289-1121">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1121">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="01289-1122">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1122">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="01289-1123">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="01289-1123">Az.OperationalInsights</span></span>
* <span data-ttu-id="01289-1124">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1124">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1125">Az.Resources</span></span>
* <span data-ttu-id="01289-1126">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="01289-1126">Support for additional Template Export options</span></span>
    - <span data-ttu-id="01289-1127">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1127">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="01289-1128">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1128">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="01289-1129">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1129">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="01289-1130">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="01289-1130">Az.ServiceFabric</span></span>
* <span data-ttu-id="01289-1131">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1131">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1132">Az.Sql</span></span>
* <span data-ttu-id="01289-1133">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1133">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="01289-1134">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1134">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="01289-1135">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-1135">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="01289-1136">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="01289-1136">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="01289-1137">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="01289-1137">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="01289-1138">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="01289-1138">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="01289-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="01289-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="01289-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="01289-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-1141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-1141">Az.Storage</span></span>
* <span data-ttu-id="01289-1142">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="01289-1142">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="01289-1143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-1143">New-AzStorageAccount</span></span>
* <span data-ttu-id="01289-1144">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1144">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="01289-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="01289-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-1146">Az.Websites</span></span>
* <span data-ttu-id="01289-1147">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="01289-1147">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="01289-1148">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="01289-1148">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="01289-1149">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1149">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="01289-1150">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="01289-1150">Az.Cdn</span></span>
* <span data-ttu-id="01289-1151">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1151">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1152">Az.Compute</span></span>
* <span data-ttu-id="01289-1153">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1153">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="01289-1154">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="01289-1154">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="01289-1155">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="01289-1155">Az.EventHub</span></span>
* <span data-ttu-id="01289-1156">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="01289-1156">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="01289-1157">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="01289-1157">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1158">Az.Network</span></span>
* <span data-ttu-id="01289-1159">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1159">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="01289-1160">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1160">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="01289-1161">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="01289-1161">Az.PolicyInsights</span></span>
* <span data-ttu-id="01289-1162">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1162">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-1163">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-1163">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-1164">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1164">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="01289-1165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="01289-1165">Az.ServiceBus</span></span>
* <span data-ttu-id="01289-1166">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="01289-1166">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="01289-1167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="01289-1167">Az.ServiceFabric</span></span>
* <span data-ttu-id="01289-1168">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1168">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="01289-1169">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1169">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-1170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1170">Az.Sql</span></span>
* <span data-ttu-id="01289-1171">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1171">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="01289-1172">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="01289-1172">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="01289-1173">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-1173">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="01289-1174">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="01289-1174">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-1175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-1175">Az.Websites</span></span>
* <span data-ttu-id="01289-1176">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="01289-1176">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="01289-1177">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1177">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="01289-1178">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="01289-1178">Az.ApiManagement</span></span>
* <span data-ttu-id="01289-1179">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="01289-1179">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="01289-1180">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="01289-1180">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="01289-1181">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="01289-1181">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="01289-1182">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="01289-1182">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="01289-1183">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01289-1183">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="01289-1184">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="01289-1184">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="01289-1185">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="01289-1185">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="01289-1186">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="01289-1186">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="01289-1187">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="01289-1187">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="01289-1188">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="01289-1188">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="01289-1189">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="01289-1189">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="01289-1190">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="01289-1190">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="01289-1191">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="01289-1191">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="01289-1192">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="01289-1192">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="01289-1193">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="01289-1193">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="01289-1194">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="01289-1194">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="01289-1195">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="01289-1195">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="01289-1196">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="01289-1196">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="01289-1197">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="01289-1197">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="01289-1198">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="01289-1198">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="01289-1199">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="01289-1199">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="01289-1200">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="01289-1200">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="01289-1201">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="01289-1201">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="01289-1202">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1202">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="01289-1203">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1203">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="01289-1204">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1204">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="01289-1205">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="01289-1205">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="01289-1206">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="01289-1206">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="01289-1207">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1207">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="01289-1208">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1208">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="01289-1209">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1209">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="01289-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="01289-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="01289-1211">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1211">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="01289-1212">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1212">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="01289-1213">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="01289-1213">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="01289-1214">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="01289-1214">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="01289-1215">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="01289-1215">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="01289-1216">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1216">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="01289-1217">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1217">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="01289-1218">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1218">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="01289-1219">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="01289-1219">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="01289-1220">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="01289-1220">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="01289-1221">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="01289-1221">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="01289-1222">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="01289-1222">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="01289-1223">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1223">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="01289-1224">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="01289-1224">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="01289-1225">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="01289-1225">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="01289-1226">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="01289-1226">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="01289-1227">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1227">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="01289-1228">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="01289-1228">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="01289-1229">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="01289-1229">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="01289-1230">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="01289-1230">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="01289-1231">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="01289-1231">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="01289-1232">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1232">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="01289-1233">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="01289-1233">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="01289-1234">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="01289-1234">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="01289-1235">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1235">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="01289-1236">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="01289-1236">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="01289-1237">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="01289-1237">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="01289-1238">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1238">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="01289-1239">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1239">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="01289-1240">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="01289-1240">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="01289-1241">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="01289-1241">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="01289-1242">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1242">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="01289-1243">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1243">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="01289-1244">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="01289-1244">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="01289-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="01289-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="01289-1246">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="01289-1246">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="01289-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="01289-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="01289-1248">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="01289-1248">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="01289-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="01289-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="01289-1250">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="01289-1250">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="01289-1251">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="01289-1251">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="01289-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="01289-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="01289-1253">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="01289-1253">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="01289-1254">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="01289-1254">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="01289-1255">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="01289-1255">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="01289-1256">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="01289-1256">Az.Automation</span></span>
* <span data-ttu-id="01289-1257">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1257">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="01289-1258">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1258">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="01289-1259">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1259">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="01289-1260">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1260">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="01289-1261">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1261">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="01289-1262">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1262">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="01289-1263">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="01289-1263">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1264">Az.Compute</span></span>
* <span data-ttu-id="01289-1265">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1265">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="01289-1266">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="01289-1266">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="01289-1267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-1267">Az.DataLakeStore</span></span>
* <span data-ttu-id="01289-1268">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1268">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="01289-1269">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="01289-1269">Az.Monitor</span></span>
* <span data-ttu-id="01289-1270">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1270">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-1271">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1271">Az.Network</span></span>
* <span data-ttu-id="01289-1272">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1272">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="01289-1273">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="01289-1273">Updated cmdlet:</span></span>
        - <span data-ttu-id="01289-1274">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="01289-1274">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="01289-1275">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1275">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-1276">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1276">Az.Resources</span></span>
* <span data-ttu-id="01289-1277">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1277">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-1278">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1278">Az.Sql</span></span>
* <span data-ttu-id="01289-1279">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="01289-1279">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="01289-1280">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1280">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="01289-1281">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-1281">Az.Accounts</span></span>
* <span data-ttu-id="01289-1282">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="01289-1282">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="01289-1283">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="01289-1283">Az.CognitiveServices</span></span>
* <span data-ttu-id="01289-1284">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="01289-1284">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="01289-1285">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="01289-1285">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1286">Az.Compute</span></span>
* <span data-ttu-id="01289-1287">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="01289-1287">Proximity placement group feature.</span></span>
    - <span data-ttu-id="01289-1288">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="01289-1288">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="01289-1289">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="01289-1289">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="01289-1290">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1290">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="01289-1291">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="01289-1291">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="01289-1292">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1292">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="01289-1293">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="01289-1293">Breaking changes</span></span>
    - <span data-ttu-id="01289-1294">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1294">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="01289-1295">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1295">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="01289-1296">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="01289-1296">Az.DeploymentManager</span></span>
* <span data-ttu-id="01289-1297">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="01289-1297">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="01289-1298">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="01289-1298">Az.Dns</span></span>
* <span data-ttu-id="01289-1299">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="01289-1299">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="01289-1300">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="01289-1300">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="01289-1301">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="01289-1301">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="01289-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="01289-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="01289-1303">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="01289-1303">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="01289-1304">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="01289-1304">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="01289-1305">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="01289-1305">Az.HDInsight</span></span>
* <span data-ttu-id="01289-1306">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="01289-1306">Removed two cmdlets:</span></span>
    - <span data-ttu-id="01289-1307">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="01289-1307">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="01289-1308">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="01289-1308">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="01289-1309">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1309">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="01289-1310">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="01289-1310">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="01289-1311">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="01289-1311">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="01289-1312">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="01289-1312">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="01289-1313">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="01289-1313">Az.Monitor</span></span>
* <span data-ttu-id="01289-1314">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="01289-1314">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="01289-1315">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="01289-1315">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="01289-1316">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="01289-1316">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="01289-1317">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="01289-1317">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="01289-1318">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="01289-1318">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="01289-1319">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="01289-1319">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="01289-1320">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="01289-1320">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="01289-1321">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="01289-1321">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="01289-1322">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="01289-1322">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="01289-1323">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="01289-1323">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="01289-1324">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="01289-1324">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="01289-1325">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="01289-1325">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="01289-1326">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="01289-1326">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="01289-1327">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1327">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-1328">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1328">Az.Network</span></span>
* <span data-ttu-id="01289-1329">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="01289-1329">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="01289-1330">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-1330">New cmdlets</span></span>
        - <span data-ttu-id="01289-1331">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="01289-1331">New-AzNatGateway</span></span>
        - <span data-ttu-id="01289-1332">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="01289-1332">Get-AzNatGateway</span></span>
        - <span data-ttu-id="01289-1333">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="01289-1333">Set-AzNatGateway</span></span>
        - <span data-ttu-id="01289-1334">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="01289-1334">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="01289-1335">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1335">Updated cmdlets</span></span>
        - <span data-ttu-id="01289-1336">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="01289-1336">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="01289-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="01289-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="01289-1338">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="01289-1338">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="01289-1339">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1339">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="01289-1340">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1340">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="01289-1341">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="01289-1341">Az.PolicyInsights</span></span>
* <span data-ttu-id="01289-1342">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-1342">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="01289-1343">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="01289-1343">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="01289-1344">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="01289-1344">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-1345">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-1345">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-1346">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-1346">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="01289-1347">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="01289-1347">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="01289-1348">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="01289-1348">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="01289-1349">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="01289-1349">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="01289-1350">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="01289-1350">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="01289-1351">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="01289-1351">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="01289-1352">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="01289-1352">Az.Relay</span></span>
* <span data-ttu-id="01289-1353">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="01289-1353">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="01289-1354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="01289-1354">Az.ServiceBus</span></span>
* <span data-ttu-id="01289-1355">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1355">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-1356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-1356">Az.Storage</span></span>
* <span data-ttu-id="01289-1357">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="01289-1357">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="01289-1358">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="01289-1358">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="01289-1359">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="01289-1359">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="01289-1360">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-1360">New-AzStorageAccount</span></span>
* <span data-ttu-id="01289-1361">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="01289-1361">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="01289-1362">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-1362">New-AzStorageAccount</span></span>
    - <span data-ttu-id="01289-1363">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-1363">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="01289-1364">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-1364">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-1365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-1365">Az.Websites</span></span>
* <span data-ttu-id="01289-1366">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="01289-1366">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="01289-1367">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="01289-1367">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="01289-1368">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1368">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="01289-1369">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="01289-1369">Highlights since the last major release</span></span>
* <span data-ttu-id="01289-1370">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="01289-1370">General availability of `Az` module</span></span>
* <span data-ttu-id="01289-1371">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="01289-1371">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="01289-1372">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="01289-1372">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="01289-1373">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1373">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="01289-1374">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1374">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="01289-1375">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1375">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="01289-1376">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-1376">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="01289-1377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-1377">Az.Accounts</span></span>
* <span data-ttu-id="01289-1378">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1378">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="01289-1379">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="01289-1379">Az.Batch</span></span>
* <span data-ttu-id="01289-1380">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1380">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="01289-1381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="01289-1381">Az.Cdn</span></span>
* <span data-ttu-id="01289-1382">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1382">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="01289-1383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="01289-1383">Az.CognitiveServices</span></span>
* <span data-ttu-id="01289-1384">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1384">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1385">Az.Compute</span></span>
* <span data-ttu-id="01289-1386">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1386">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="01289-1387">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1387">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="01289-1388">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1388">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-1389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-1389">Az.DataFactory</span></span>
* <span data-ttu-id="01289-1390">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1390">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="01289-1391">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-1391">Az.DataLakeStore</span></span>
* <span data-ttu-id="01289-1392">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1392">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="01289-1393">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="01289-1393">Az.EventGrid</span></span>
* <span data-ttu-id="01289-1394">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1394">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="01289-1395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="01289-1395">Az.EventHub</span></span>
* <span data-ttu-id="01289-1396">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1396">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="01289-1397">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="01289-1397">Az.HDInsight</span></span>
* <span data-ttu-id="01289-1398">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1398">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="01289-1399">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="01289-1399">Az.IotHub</span></span>
* <span data-ttu-id="01289-1400">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1400">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="01289-1401">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="01289-1401">Az.KeyVault</span></span>
* <span data-ttu-id="01289-1402">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1402">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="01289-1403">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1403">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="01289-1404">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="01289-1404">Az.MachineLearning</span></span>
* <span data-ttu-id="01289-1405">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1405">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="01289-1406">Az.Media</span><span class="sxs-lookup"><span data-stu-id="01289-1406">Az.Media</span></span>
* <span data-ttu-id="01289-1407">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1407">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="01289-1408">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="01289-1408">Az.Monitor</span></span>
  * <span data-ttu-id="01289-1409">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="01289-1409">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="01289-1410">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="01289-1410">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="01289-1411">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="01289-1411">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="01289-1412">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="01289-1412">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="01289-1413">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="01289-1413">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="01289-1414">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="01289-1414">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="01289-1415">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1415">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1416">Az.Network</span></span>
* <span data-ttu-id="01289-1417">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1417">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="01289-1418">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1418">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="01289-1419">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="01289-1419">Az.NotificationHubs</span></span>
* <span data-ttu-id="01289-1420">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1420">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="01289-1421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="01289-1421">Az.OperationalInsights</span></span>
* <span data-ttu-id="01289-1422">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1422">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="01289-1423">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="01289-1423">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="01289-1424">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1424">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-1425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-1425">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-1426">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1426">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="01289-1427">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="01289-1427">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="01289-1428">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1428">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="01289-1429">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1429">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="01289-1430">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="01289-1430">Az.RedisCache</span></span>
* <span data-ttu-id="01289-1431">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-1432">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1432">Az.Resources</span></span>
* <span data-ttu-id="01289-1433">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1433">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1434">Az.Sql</span></span>
* <span data-ttu-id="01289-1435">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1435">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="01289-1436">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="01289-1437">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1437">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="01289-1438">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1438">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="01289-1439">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1439">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="01289-1440">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-1440">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="01289-1441">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1441">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-1442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-1442">Az.Websites</span></span>
* <span data-ttu-id="01289-1443">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1443">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="01289-1444">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1444">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="01289-1445">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1445">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="01289-1446">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="01289-1446">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="01289-1447">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1447">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="01289-1448">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="01289-1448">Highlights since the last major release</span></span>
* <span data-ttu-id="01289-1449">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="01289-1449">General availability of `Az` module</span></span>
* <span data-ttu-id="01289-1450">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="01289-1450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="01289-1451">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="01289-1451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="01289-1452">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="01289-1453">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="01289-1454">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="01289-1455">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-1455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="01289-1456">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-1456">Az.Accounts</span></span>
* <span data-ttu-id="01289-1457">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1457">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="01289-1458">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="01289-1458">Az.AnalysisServices</span></span>
* <span data-ttu-id="01289-1459">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="01289-1459">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="01289-1460">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="01289-1460">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="01289-1461">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="01289-1461">Az.Automation</span></span>
* <span data-ttu-id="01289-1462">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1462">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="01289-1463">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="01289-1463">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="01289-1464">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="01289-1464">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1465">Az.Compute</span></span>
* <span data-ttu-id="01289-1466">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1466">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="01289-1467">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1467">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="01289-1468">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="01289-1468">Az.ContainerInstance</span></span>
* <span data-ttu-id="01289-1469">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1469">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-1470">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-1470">Az.DataFactory</span></span>
* <span data-ttu-id="01289-1471">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1471">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="01289-1472">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1472">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-1473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1473">Az.Resources</span></span>
* <span data-ttu-id="01289-1474">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1474">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="01289-1475">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1475">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="01289-1476">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="01289-1476">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="01289-1477">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="01289-1477">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="01289-1478">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1478">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="01289-1479">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="01289-1479">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-1480">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1480">Az.Sql</span></span>
* <span data-ttu-id="01289-1481">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-1481">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-1482">Az.Storage</span></span>
* <span data-ttu-id="01289-1483">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="01289-1483">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="01289-1484">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="01289-1484">New-AzStorageContext</span></span>
* <span data-ttu-id="01289-1485">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="01289-1485">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="01289-1486">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="01289-1486">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="01289-1487">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="01289-1487">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="01289-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="01289-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="01289-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="01289-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="01289-1490">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="01289-1490">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="01289-1491">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="01289-1491">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="01289-1492">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="01289-1492">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="01289-1493">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="01289-1493">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="01289-1494">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="01289-1494">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="01289-1495">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1495">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="01289-1496">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="01289-1496">Highlights since the last major release</span></span>
* <span data-ttu-id="01289-1497">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="01289-1497">General availability of `Az` module</span></span>
* <span data-ttu-id="01289-1498">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="01289-1498">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="01289-1499">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="01289-1499">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="01289-1500">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1500">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="01289-1501">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1501">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="01289-1502">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1502">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="01289-1503">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-1503">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="01289-1504">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="01289-1504">Az.Automation</span></span>
* <span data-ttu-id="01289-1505">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="01289-1505">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="01289-1506">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="01289-1506">Dynamic grouping</span></span>
    * <span data-ttu-id="01289-1507">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="01289-1507">Pre-Post script</span></span>
    * <span data-ttu-id="01289-1508">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="01289-1508">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1509">Az.Compute</span></span>
* <span data-ttu-id="01289-1510">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="01289-1510">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="01289-1511">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1511">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="01289-1512">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="01289-1512">Az.KeyVault</span></span>
* <span data-ttu-id="01289-1513">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1513">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-1514">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1514">Az.Network</span></span>
* <span data-ttu-id="01289-1515">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1515">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="01289-1516">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1516">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-1517">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-1517">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-1518">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1518">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="01289-1519">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1519">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-1520">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1520">Az.Resources</span></span>
* <span data-ttu-id="01289-1521">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1521">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="01289-1522">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1522">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-1523">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1523">Az.Sql</span></span>
* <span data-ttu-id="01289-1524">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1524">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-1525">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-1525">Az.Storage</span></span>
* <span data-ttu-id="01289-1526">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="01289-1526">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="01289-1527">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="01289-1527">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="01289-1528">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="01289-1528">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="01289-1529">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="01289-1529">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="01289-1530">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="01289-1530">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="01289-1531">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="01289-1531">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="01289-1532">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="01289-1532">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-1533">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-1533">Az.Websites</span></span>
* <span data-ttu-id="01289-1534">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1534">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="01289-1535">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1535">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="01289-1536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-1536">Az.Accounts</span></span>
* <span data-ttu-id="01289-1537">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1537">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="01289-1538">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1538">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="01289-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="01289-1539">Az.Automation</span></span>
* <span data-ttu-id="01289-1540">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1540">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="01289-1541">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1541">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="01289-1542">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="01289-1542">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="01289-1543">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="01289-1543">Az.Cdn</span></span>
* <span data-ttu-id="01289-1544">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="01289-1544">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1545">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1545">Az.Compute</span></span>
* <span data-ttu-id="01289-1546">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1546">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-1547">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-1547">Az.DataFactory</span></span>
* <span data-ttu-id="01289-1548">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1548">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="01289-1549">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="01289-1549">Az.LogicApp</span></span>
* <span data-ttu-id="01289-1550">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="01289-1550">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1551">Az.Network</span></span>
* <span data-ttu-id="01289-1552">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1552">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-1553">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-1553">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-1554">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1554">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="01289-1555">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="01289-1555">SDK Update</span></span>
* <span data-ttu-id="01289-1556">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-1556">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="01289-1557">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1557">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-1558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1558">Az.Resources</span></span>
* <span data-ttu-id="01289-1559">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1559">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="01289-1560">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="01289-1560">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="01289-1561">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1561">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="01289-1562">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="01289-1562">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="01289-1563">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1563">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="01289-1564">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="01289-1564">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-1565">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1565">Az.Sql</span></span>
* <span data-ttu-id="01289-1566">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="01289-1566">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="01289-1567">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="01289-1567">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-1568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-1568">Az.Storage</span></span>
* <span data-ttu-id="01289-1569">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01289-1569">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="01289-1570">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1570">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="01289-1571">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="01289-1571">Az.AnalysisServices</span></span>
* <span data-ttu-id="01289-1572">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="01289-1572">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="01289-1573">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="01289-1573">Az.Automation</span></span>
* <span data-ttu-id="01289-1574">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1574">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="01289-1575">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1575">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="01289-1576">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1576">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="01289-1577">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="01289-1577">Az.CognitiveServices</span></span>
* <span data-ttu-id="01289-1578">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1578">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1579">Az.Compute</span></span>
* <span data-ttu-id="01289-1580">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1580">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="01289-1581">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1581">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="01289-1582">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1582">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="01289-1583">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="01289-1583">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="01289-1584">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-1584">Az.DataLakeStore</span></span>
* <span data-ttu-id="01289-1585">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1585">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="01289-1586">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="01289-1586">Az.EventHub</span></span>
* <span data-ttu-id="01289-1587">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1587">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="01289-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="01289-1588">Az.KeyVault</span></span>
* <span data-ttu-id="01289-1589">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1589">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="01289-1590">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="01289-1590">Az.LogicApp</span></span>
* <span data-ttu-id="01289-1591">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1591">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="01289-1592">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1592">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="01289-1593">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-1593">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="01289-1594">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="01289-1594">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="01289-1595">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="01289-1595">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="01289-1596">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="01289-1596">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="01289-1597">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="01289-1597">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="01289-1598">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="01289-1598">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="01289-1599">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="01289-1599">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="01289-1600">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="01289-1600">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="01289-1601">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="01289-1601">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="01289-1602">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="01289-1602">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="01289-1603">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1603">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="01289-1604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="01289-1604">Az.Monitor</span></span>
* <span data-ttu-id="01289-1605">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1605">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-1606">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1606">Az.Network</span></span>
* <span data-ttu-id="01289-1607">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1607">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="01289-1608">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="01289-1608">Az.OperationalInsights</span></span>
* <span data-ttu-id="01289-1609">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="01289-1609">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="01289-1610">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1610">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="01289-1611">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1611">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="01289-1612">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1612">Az.Resources</span></span>
* <span data-ttu-id="01289-1613">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1613">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="01289-1614">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1614">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="01289-1615">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1615">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="01289-1616">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1616">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-1617">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1617">Az.Sql</span></span>
* <span data-ttu-id="01289-1618">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1618">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="01289-1619">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1619">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-1620">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-1620">Az.Websites</span></span>
* <span data-ttu-id="01289-1621">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1621">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="01289-1622">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1622">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="01289-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-1623">Az.Accounts</span></span>
* <span data-ttu-id="01289-1624">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="01289-1624">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="01289-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="01289-1625">Az.AnalysisServices</span></span>
<span data-ttu-id="01289-1626">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="01289-1626">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1627">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1627">Az.Compute</span></span>
* <span data-ttu-id="01289-1628">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1628">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="01289-1629">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1629">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="01289-1630">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1630">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-1631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-1631">Az.RecoveryServices</span></span>
<span data-ttu-id="01289-1632">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="01289-1632">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1633">Az.Resources</span></span>
* <span data-ttu-id="01289-1634">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1634">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="01289-1635">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="01289-1635">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="01289-1636">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1636">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="01289-1637">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="01289-1637">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-1638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1638">Az.Sql</span></span>
* <span data-ttu-id="01289-1639">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="01289-1639">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="01289-1640">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1640">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="01289-1641">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1641">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="01289-1642">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1642">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="01289-1643">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-1643">Az.Accounts</span></span>
* <span data-ttu-id="01289-1644">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="01289-1644">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="01289-1645">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="01289-1645">Az.AnalysisServices</span></span>
* <span data-ttu-id="01289-1646">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="01289-1646">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="01289-1647">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-1647">Az.RecoveryServices</span></span>
* <span data-ttu-id="01289-1648">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="01289-1648">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="01289-1649">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1649">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="01289-1650">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-1650">Az.Accounts</span></span>
* <span data-ttu-id="01289-1651">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1651">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="01289-1652">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="01289-1653">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1653">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="01289-1654">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="01289-1654">Az.Aks</span></span>
* <span data-ttu-id="01289-1655">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1655">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="01289-1656">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="01289-1656">Az.Automation</span></span>
* <span data-ttu-id="01289-1657">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1657">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="01289-1658">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1658">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="01289-1659">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="01289-1659">Az.Cdn</span></span>
* <span data-ttu-id="01289-1660">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1660">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1661">Az.Compute</span></span>
* <span data-ttu-id="01289-1662">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1662">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="01289-1663">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1663">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="01289-1664">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1664">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="01289-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="01289-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="01289-1666">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1666">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="01289-1667">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="01289-1667">Az.DataFactory</span></span>
* <span data-ttu-id="01289-1668">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1668">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="01289-1669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-1669">Az.DataLakeStore</span></span>
* <span data-ttu-id="01289-1670">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1670">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="01289-1671">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="01289-1671">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="01289-1672">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1672">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="01289-1673">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="01289-1673">Az.IotHub</span></span>
* <span data-ttu-id="01289-1674">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1674">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="01289-1675">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="01289-1675">Az.KeyVault</span></span>
* <span data-ttu-id="01289-1676">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1676">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-1677">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1677">Az.Network</span></span>
* <span data-ttu-id="01289-1678">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1678">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-1679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1679">Az.Resources</span></span>
* <span data-ttu-id="01289-1680">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1680">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="01289-1681">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1681">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="01289-1682">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1682">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="01289-1683">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1683">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="01289-1684">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1684">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="01289-1685">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1685">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="01289-1686">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="01289-1686">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="01289-1687">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="01289-1687">Az.ServiceFabric</span></span>
* <span data-ttu-id="01289-1688">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="01289-1688">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="01289-1689">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1689">Fix some error messages.</span></span>
* <span data-ttu-id="01289-1690">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1690">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="01289-1691">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1691">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="01289-1692">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="01289-1692">Az.SignalR</span></span>
* <span data-ttu-id="01289-1693">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1693">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-1694">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1694">Az.Sql</span></span>
* <span data-ttu-id="01289-1695">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1695">Update incorrect online help URLs</span></span>
* <span data-ttu-id="01289-1696">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1696">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="01289-1697">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1697">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="01289-1698">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="01289-1698">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-1699">Az.Storage</span></span>
* <span data-ttu-id="01289-1700">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1700">Update incorrect online help URLs</span></span>
* <span data-ttu-id="01289-1701">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="01289-1701">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="01289-1702">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="01289-1702">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="01289-1703">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="01289-1703">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="01289-1704">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="01289-1704">Az.TrafficManager</span></span>
* <span data-ttu-id="01289-1705">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1705">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-1706">Az.Websites</span></span>
* <span data-ttu-id="01289-1707">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1707">Update incorrect online help URLs</span></span>
* <span data-ttu-id="01289-1708">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1708">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="01289-1709">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1709">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="01289-1710">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="01289-1710">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="01289-1711">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-1711">Az.Accounts</span></span>
* <span data-ttu-id="01289-1712">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1712">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1713">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1713">Az.Compute</span></span>
* <span data-ttu-id="01289-1714">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="01289-1714">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="01289-1715">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1715">Updated the description of ID in help files</span></span>
* <span data-ttu-id="01289-1716">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="01289-1716">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="01289-1717">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-1717">Az.DataLakeStore</span></span>
* <span data-ttu-id="01289-1718">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1718">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="01289-1719">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1719">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="01289-1720">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="01289-1720">Az.EventGrid</span></span>
* <span data-ttu-id="01289-1721">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1721">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="01289-1722">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1722">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="01289-1723">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-1723">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="01289-1724">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="01289-1724">Event Time-To-Live,</span></span>
        - <span data-ttu-id="01289-1725">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="01289-1725">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="01289-1726">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="01289-1726">Dead letter endpoint.</span></span>
    - <span data-ttu-id="01289-1727">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-1727">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="01289-1728">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="01289-1728">Event Time-To-Live,</span></span>
        - <span data-ttu-id="01289-1729">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="01289-1729">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="01289-1730">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="01289-1730">Dead letter endpoint.</span></span>
* <span data-ttu-id="01289-1731">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1731">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="01289-1732">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="01289-1732">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="01289-1733">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="01289-1733">Az.IotHub</span></span>
* <span data-ttu-id="01289-1734">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1734">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="01289-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="01289-1735">Az.LogicApp</span></span>
* <span data-ttu-id="01289-1736">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="01289-1736">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-1737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1737">Az.Resources</span></span>
* <span data-ttu-id="01289-1738">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1738">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="01289-1739">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="01289-1739">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="01289-1740">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1740">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="01289-1741">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1741">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="01289-1742">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1742">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="01289-1743">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="01289-1743">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="01289-1744">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="01289-1744">Az.SignalR</span></span>
* <span data-ttu-id="01289-1745">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="01289-1745">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-1746">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1746">Az.Sql</span></span>
* <span data-ttu-id="01289-1747">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="01289-1747">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="01289-1748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-1748">Az.Storage</span></span>
* <span data-ttu-id="01289-1749">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="01289-1749">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="01289-1750">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="01289-1750">New-AzStorageContext</span></span>
* <span data-ttu-id="01289-1751">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1751">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="01289-1752">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="01289-1752">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-1753">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-1753">Az.Websites</span></span>
* <span data-ttu-id="01289-1754">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1754">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="01289-1755">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="01289-1755">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="01289-1756">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="01289-1756">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="01289-1757">Genel</span><span class="sxs-lookup"><span data-stu-id="01289-1757">General</span></span>

- <span data-ttu-id="01289-1758">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="01289-1758">General Availability of Az Module</span></span>
- <span data-ttu-id="01289-1759">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="01289-1759">Online help for each module</span></span>
- <span data-ttu-id="01289-1760">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="01289-1760">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="01289-1761">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1761">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="01289-1762">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="01289-1762">Az.Accounts</span></span>
- <span data-ttu-id="01289-1763">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="01289-1763">Changed from Az.Profile</span></span>
- <span data-ttu-id="01289-1764">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1764">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="01289-1765">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="01289-1765">Az.ApiManagement</span></span>
- <span data-ttu-id="01289-1766">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="01289-1766">Fixes for #7002</span></span>
- <span data-ttu-id="01289-1767">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="01289-1768">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="01289-1768">Az.Batch</span></span>
- <span data-ttu-id="01289-1769">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1769">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="01289-1770">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="01289-1770">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="01289-1771">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1771">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="01289-1772">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="01289-1772">Az.Billing</span></span>
- <span data-ttu-id="01289-1773">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1773">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="01289-1774">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="01289-1774">Az.CognitivServices</span></span>
- <span data-ttu-id="01289-1775">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1775">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="01289-1776">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-1776">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="01289-1777">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="01289-1777">Az.ContainerInstance</span></span>
- <span data-ttu-id="01289-1778">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1778">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="01289-1779">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="01289-1779">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="01289-1780">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="01289-1781">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-1781">Az.DataLakeStore</span></span>
- <span data-ttu-id="01289-1782">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1782">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="01289-1783">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="01289-1783">Az.Monitor</span></span>
- <span data-ttu-id="01289-1784">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1784">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="01289-1785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="01289-1785">Az.KeyVault</span></span>
- <span data-ttu-id="01289-1786">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-1786">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="01289-1787">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="01289-1787">Az.MachineLearning</span></span>
- <span data-ttu-id="01289-1788">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1788">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="01289-1789">Az.Media</span><span class="sxs-lookup"><span data-stu-id="01289-1789">Az.Media</span></span>
- <span data-ttu-id="01289-1790">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="01289-1790">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="01289-1791">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1791">Az.Network</span></span>
<span data-ttu-id="01289-1792">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1792">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="01289-1793">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="01289-1793">New cmdlets added:</span></span>
        - <span data-ttu-id="01289-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01289-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="01289-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01289-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="01289-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01289-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="01289-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01289-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="01289-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01289-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="01289-1799">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="01289-1799">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="01289-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="01289-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="01289-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="01289-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="01289-1802">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1802">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="01289-1803">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01289-1803">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="01289-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01289-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="01289-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01289-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="01289-1806">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01289-1806">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="01289-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="01289-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="01289-1808">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="01289-1808">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="01289-1809">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1809">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="01289-1810">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="01289-1810">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="01289-1811">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="01289-1811">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="01289-1812">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="01289-1812">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="01289-1813">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1813">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="01289-1814">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1814">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="01289-1815">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="01289-1815">Az.OperationalInsights</span></span>
- <span data-ttu-id="01289-1816">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="01289-1817">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="01289-1817">Az.Profile</span></span>
- <span data-ttu-id="01289-1818">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1818">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="01289-1819">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-1819">Az.RecoveryServices</span></span>
- <span data-ttu-id="01289-1820">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="01289-1821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1821">Az.Resources</span></span>
- <span data-ttu-id="01289-1822">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1822">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="01289-1823">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="01289-1823">Az.ServiceFabric</span></span>
- <span data-ttu-id="01289-1824">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="01289-1824">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="01289-1825">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1825">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="01289-1826">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="01289-1826">Az.SIgnalR</span></span>
- <span data-ttu-id="01289-1827">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="01289-1827">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="01289-1828">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1828">Az.Sql</span></span>
- <span data-ttu-id="01289-1829">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1829">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="01289-1830">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1830">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="01289-1831">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="01289-1832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-1832">Az.Storage</span></span>
- <span data-ttu-id="01289-1833">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1833">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="01289-1834">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-1834">Az.Websites</span></span>
- <span data-ttu-id="01289-1835">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="01289-1835">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="01289-1836">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="01289-1836">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="01289-1837">Genel</span><span class="sxs-lookup"><span data-stu-id="01289-1837">General</span></span>

* <span data-ttu-id="01289-1838">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="01289-1838">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="01289-1839">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1839">Az.Compute</span></span>

* <span data-ttu-id="01289-1840">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1840">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="01289-1841">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-1841">Az.DataLakeStore</span></span>

* <span data-ttu-id="01289-1842">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1842">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="01289-1843">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="01289-1843">Az.FrontDoor</span></span>

* <span data-ttu-id="01289-1844">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1844">Fixed some broken links</span></span>
    - <span data-ttu-id="01289-1845">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1845">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="01289-1846">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1846">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="01289-1847">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01289-1847">Az.RecoveryServices</span></span>

* <span data-ttu-id="01289-1848">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1848">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="01289-1849">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1849">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="01289-1850">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1850">Az.Resources</span></span>

* <span data-ttu-id="01289-1851">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="01289-1851">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="01289-1852">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1852">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="01289-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1853">Az.Sql</span></span>

* <span data-ttu-id="01289-1854">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="01289-1854">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="01289-1855">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1855">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="01289-1856">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1856">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="01289-1857">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="01289-1857">Az.Storage</span></span>

* <span data-ttu-id="01289-1858">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1858">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="01289-1859">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1859">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="01289-1860">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="01289-1860">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="01289-1861">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1861">Support Static Website configuration</span></span>
    - <span data-ttu-id="01289-1862">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="01289-1862">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="01289-1863">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="01289-1863">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="01289-1864">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-1864">Az.Websites</span></span>

* <span data-ttu-id="01289-1865">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="01289-1865">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="01289-1866">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1866">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="01289-1867">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="01289-1867">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="01289-1868">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="01289-1868">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="01289-1869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="01289-1869">Az.ApiManagement</span></span>
* <span data-ttu-id="01289-1870">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="01289-1870">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="01289-1871">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="01289-1871">Az.Automation</span></span>
* <span data-ttu-id="01289-1872">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="01289-1872">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="01289-1873">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1873">Added Update Management cmdlets</span></span>
* <span data-ttu-id="01289-1874">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1874">Added Source Control cmdlets</span></span>
* <span data-ttu-id="01289-1875">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1875">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="01289-1876">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1876">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="01289-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1877">Az.Compute</span></span>
* <span data-ttu-id="01289-1878">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1878">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="01289-1879">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="01289-1879">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="01289-1880">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="01289-1880">Az.ContainerInstance</span></span>
* <span data-ttu-id="01289-1881">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="01289-1881">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="01289-1882">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="01289-1882">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="01289-1883">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1883">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="01289-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1884">Az.Network</span></span>
* <span data-ttu-id="01289-1885">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1885">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="01289-1886">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1886">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="01289-1887">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1887">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="01289-1888">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1888">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="01289-1889">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="01289-1889">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="01289-1890">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1890">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="01289-1891">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="01289-1891">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="01289-1892">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="01289-1892">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="01289-1893">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1893">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="01289-1894">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="01289-1894">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="01289-1895">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="01289-1895">Az.Relay</span></span>
* <span data-ttu-id="01289-1896">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1896">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="01289-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1897">Az.Resources</span></span>
* <span data-ttu-id="01289-1898">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1898">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="01289-1899">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1899">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="01289-1900">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="01289-1900">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="01289-1901">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="01289-1901">Az.ServiceFabric</span></span>
* <span data-ttu-id="01289-1902">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1902">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="01289-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-1903">Az.Sql</span></span>
* <span data-ttu-id="01289-1904">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1904">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="01289-1905">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="01289-1905">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="01289-1906">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="01289-1906">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="01289-1907">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="01289-1907">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="01289-1908">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="01289-1908">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="01289-1909">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="01289-1909">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="01289-1910">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="01289-1910">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="01289-1911">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="01289-1911">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="01289-1912">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="01289-1912">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="01289-1913">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1913">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="01289-1914">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1914">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="01289-1915">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1915">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="01289-1916">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="01289-1916">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="01289-1917">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="01289-1917">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="01289-1918">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="01289-1918">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="01289-1919">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="01289-1919">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="01289-1920">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1920">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="01289-1921">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="01289-1921">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="01289-1922">Genel</span><span class="sxs-lookup"><span data-stu-id="01289-1922">General</span></span>
* <span data-ttu-id="01289-1923">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="01289-1923">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="01289-1924">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="01289-1924">Az.Profile</span></span>
* <span data-ttu-id="01289-1925">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1925">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="01289-1926">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1926">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="01289-1927">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1927">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="01289-1928">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1928">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="01289-1929">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1929">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="01289-1930">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1930">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="01289-1931">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1931">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="01289-1932">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="01289-1932">Az.CognitiveServices</span></span>
* <span data-ttu-id="01289-1933">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1933">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1934">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1934">Az.Compute</span></span>
* <span data-ttu-id="01289-1935">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1935">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="01289-1936">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="01289-1936">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="01289-1937">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1937">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="01289-1938">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-1938">Az.DataLakeStore</span></span>
* <span data-ttu-id="01289-1939">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1939">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="01289-1940">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1940">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="01289-1941">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="01289-1941">Az.Insights</span></span>
* <span data-ttu-id="01289-1942">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1942">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="01289-1943">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="01289-1943">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="01289-1944">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1944">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="01289-1945">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="01289-1945">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1946">Az.Network</span></span>
* <span data-ttu-id="01289-1947">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="01289-1947">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="01289-1948">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="01289-1948">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="01289-1949">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="01289-1949">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="01289-1950">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="01289-1950">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="01289-1951">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="01289-1951">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="01289-1952">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="01289-1952">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="01289-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="01289-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="01289-1954">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="01289-1954">Az.PolicyInsights</span></span>
* <span data-ttu-id="01289-1955">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1955">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-1956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1956">Az.Resources</span></span>
* <span data-ttu-id="01289-1957">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="01289-1957">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="01289-1958">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="01289-1958">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="01289-1959">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="01289-1959">Az.ServiceBus</span></span>
* <span data-ttu-id="01289-1960">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1960">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="01289-1961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="01289-1961">Az.ServiceFabric</span></span>
* <span data-ttu-id="01289-1962">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1962">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="01289-1963">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1963">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="01289-1964">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="01289-1964">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="01289-1965">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="01289-1965">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="01289-1966">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1966">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="01289-1967">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="01289-1967">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="01289-1968">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="01289-1968">Az.Profile</span></span>
* <span data-ttu-id="01289-1969">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="01289-1969">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="01289-1970">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="01289-1970">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1971">Az.Compute</span></span>
* <span data-ttu-id="01289-1972">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-1972">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="01289-1973">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1973">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="01289-1974">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01289-1974">Az.DataLakeStore</span></span>
* <span data-ttu-id="01289-1975">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="01289-1975">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="01289-1976">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="01289-1976">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="01289-1977">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="01289-1977">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="01289-1978">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="01289-1978">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="01289-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="01289-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-1980">Az.Network</span></span>
* <span data-ttu-id="01289-1981">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="01289-1981">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="01289-1982">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1982">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-1983">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-1983">Az.Resources</span></span>
* <span data-ttu-id="01289-1984">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="01289-1984">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="01289-1985">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="01289-1985">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="01289-1986">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="01289-1986">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="01289-1987">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="01289-1987">Azure.Storage</span></span>
* <span data-ttu-id="01289-1988">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="01289-1988">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="01289-1989">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="01289-1989">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="01289-1990">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="01289-1990">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="01289-1991">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="01289-1991">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="01289-1992">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="01289-1992">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="01289-1993">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="01289-1993">Az.CognitiveServices</span></span>
* <span data-ttu-id="01289-1994">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="01289-1994">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="01289-1995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="01289-1995">Az.Compute</span></span>
* <span data-ttu-id="01289-1996">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1996">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="01289-1997">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-1997">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="01289-1998">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-1998">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="01289-1999">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="01289-1999">Az.DataFactoryV2</span></span>
* <span data-ttu-id="01289-2000">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="01289-2000">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="01289-2001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="01289-2001">Az.Network</span></span>
* <span data-ttu-id="01289-2002">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="01289-2002">Added NetworkProfile functionality.</span></span> <span data-ttu-id="01289-2003">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-2003">new cmdlets added</span></span>
    - <span data-ttu-id="01289-2004">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="01289-2004">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="01289-2005">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="01289-2005">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="01289-2006">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="01289-2006">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="01289-2007">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="01289-2007">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="01289-2008">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="01289-2008">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="01289-2009">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="01289-2009">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="01289-2010">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-2010">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="01289-2011">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-2011">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="01289-2012">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-2012">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="01289-2013">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="01289-2013">Az.RedisCache</span></span>
* <span data-ttu-id="01289-2014">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="01289-2014">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="01289-2015">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-2015">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="01289-2016">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="01289-2016">Az.Resources</span></span>
* <span data-ttu-id="01289-2017">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="01289-2017">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="01289-2018">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-2018">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="01289-2019">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="01289-2019">Az.Sql</span></span>
* <span data-ttu-id="01289-2020">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="01289-2020">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="01289-2021">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="01289-2021">Az.Websites</span></span>
* <span data-ttu-id="01289-2022">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="01289-2022">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="01289-2023">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="01289-2023">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="01289-2024">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="01289-2024">0.2.0 - September 2018</span></span>
 <span data-ttu-id="01289-2025">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="01289-2025">Initial Release</span></span>
