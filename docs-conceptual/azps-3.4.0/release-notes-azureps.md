---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 694439934afb41b465a89188d59bc964db3c0032
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002682"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="dc16a-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="dc16a-103">Azure PowerShell release notes</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="dc16a-104">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="dc16a-104">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dc16a-105">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="dc16a-105">Highlights since the last major release</span></span>
* <span data-ttu-id="dc16a-106">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="dc16a-106">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="dc16a-107">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-107">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dc16a-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-108">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-109">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="dc16a-109">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="dc16a-110">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-110">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dc16a-111">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc16a-111">Az.ApiManagement</span></span>
* <span data-ttu-id="dc16a-112">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="dc16a-112">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="dc16a-113">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="dc16a-113">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="dc16a-114">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-114">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="dc16a-115">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-115">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-116">Az.Compute</span></span>
* <span data-ttu-id="dc16a-117">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="dc16a-117">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="dc16a-118">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-118">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="dc16a-119">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-119">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="dc16a-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="dc16a-121">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-121">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-122">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-123">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-123">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="dc16a-124">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="dc16a-124">Az.DeploymentManager</span></span>
* <span data-ttu-id="dc16a-125">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="dc16a-125">Adds LIST operations for resources</span></span>
* <span data-ttu-id="dc16a-126">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="dc16a-126">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dc16a-127">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dc16a-127">Az.HDInsight</span></span>
* <span data-ttu-id="dc16a-128">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-128">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dc16a-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc16a-129">Az.KeyVault</span></span>
* <span data-ttu-id="dc16a-130">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-130">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-131">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-131">Az.Network</span></span>
* <span data-ttu-id="dc16a-132">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-132">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="dc16a-133">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="dc16a-133">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="dc16a-134">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-134">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="dc16a-135">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-135">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="dc16a-136">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="dc16a-136">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="dc16a-137">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-137">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="dc16a-138">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-138">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="dc16a-139">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-139">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="dc16a-140">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-140">New cmdlets added:</span></span>
        - <span data-ttu-id="dc16a-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc16a-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="dc16a-142">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-142">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="dc16a-143">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="dc16a-143">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="dc16a-144">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-144">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dc16a-145">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-145">Az.PolicyInsights</span></span>
* <span data-ttu-id="dc16a-146">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="dc16a-146">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="dc16a-147">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-147">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="dc16a-148">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-148">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="dc16a-149">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-149">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-150">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-151">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-151">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="dc16a-152">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-152">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-153">Az.Resources</span></span>
* <span data-ttu-id="dc16a-154">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-154">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="dc16a-155">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-155">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-156">Az.Sql</span></span>
<span data-ttu-id="dc16a-157">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-157">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-158">Az.Storage</span></span>
* <span data-ttu-id="dc16a-159">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="dc16a-159">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="dc16a-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-160">New-AzStorageAccount</span></span>
* <span data-ttu-id="dc16a-161">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="dc16a-161">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="dc16a-162">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-162">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-163">Az.Websites</span></span>
* <span data-ttu-id="dc16a-164">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="dc16a-164">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="dc16a-165">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-165">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="dc16a-166">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="dc16a-166">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dc16a-167">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-167">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-168">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-168">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dc16a-169">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dc16a-169">Az.Cdn</span></span>
* <span data-ttu-id="dc16a-170">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="dc16a-170">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-171">Az.Compute</span></span>
* <span data-ttu-id="dc16a-172">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-172">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="dc16a-173">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dc16a-173">Az.ContainerInstance</span></span>
* <span data-ttu-id="dc16a-174">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-174">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="dc16a-175">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="dc16a-175">Az.DataBoxEdge</span></span>
* <span data-ttu-id="dc16a-176">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-176">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="dc16a-177">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="dc16a-177">Get the Edge Storage Container</span></span>
* <span data-ttu-id="dc16a-178">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-178">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="dc16a-179">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc16a-179">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="dc16a-180">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-180">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="dc16a-181">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="dc16a-181">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="dc16a-182">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-182">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="dc16a-183">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="dc16a-183">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="dc16a-184">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-184">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="dc16a-185">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="dc16a-185">Get the Edge Storage Account</span></span>
* <span data-ttu-id="dc16a-186">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-186">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="dc16a-187">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc16a-187">Create new Edge Storage Account</span></span>
* <span data-ttu-id="dc16a-188">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-188">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="dc16a-189">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="dc16a-189">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="dc16a-190">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="dc16a-190">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="dc16a-191">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="dc16a-191">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="dc16a-192">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-192">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="dc16a-193">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="dc16a-193">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-194">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-194">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-195">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-195">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="dc16a-196">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-196">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="dc16a-197">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-197">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="dc16a-198">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="dc16a-198">Az.DevTestLabs</span></span>
* <span data-ttu-id="dc16a-199">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-199">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dc16a-200">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-200">Az.EventHub</span></span>
* <span data-ttu-id="dc16a-201">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-201">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dc16a-202">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dc16a-202">Az.HDInsight</span></span>
* <span data-ttu-id="dc16a-203">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-203">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="dc16a-204">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="dc16a-204">Az.MachineLearning</span></span>
* <span data-ttu-id="dc16a-205">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-205">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="dc16a-206">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dc16a-206">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="dc16a-207">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="dc16a-207">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="dc16a-208">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dc16a-208">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="dc16a-209">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dc16a-209">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="dc16a-210">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dc16a-210">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="dc16a-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="dc16a-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="dc16a-212">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="dc16a-212">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-213">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-213">Az.Network</span></span>
* <span data-ttu-id="dc16a-214">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-214">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-215">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-215">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-216">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-216">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="dc16a-217">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-217">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="dc16a-218">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-218">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="dc16a-219">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-219">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-220">Az.Resources</span></span>
* <span data-ttu-id="dc16a-221">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-221">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-222">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-222">Az.Sql</span></span>
* <span data-ttu-id="dc16a-223">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-223">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="dc16a-224">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-224">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="dc16a-225">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dc16a-225">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="dc16a-226">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-226">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-227">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-227">Az.Storage</span></span>
* <span data-ttu-id="dc16a-228">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-228">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="dc16a-229">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc16a-229">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="dc16a-230">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="dc16a-230">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="dc16a-231">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-231">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="dc16a-232">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-232">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="dc16a-233">Genel</span><span class="sxs-lookup"><span data-stu-id="dc16a-233">General</span></span>
* <span data-ttu-id="dc16a-234">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-234">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dc16a-235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-235">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-236">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="dc16a-236">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="dc16a-237">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-237">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dc16a-238">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dc16a-238">Az.Batch</span></span>
* <span data-ttu-id="dc16a-239">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-239">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-240">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-240">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-241">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-241">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dc16a-242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dc16a-242">Az.FrontDoor</span></span>
* <span data-ttu-id="dc16a-243">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-243">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="dc16a-244">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-244">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="dc16a-245">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="dc16a-245">Az.HealthcareApis</span></span>
* <span data-ttu-id="dc16a-246">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="dc16a-246">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dc16a-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc16a-247">Az.KeyVault</span></span>
* <span data-ttu-id="dc16a-248">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-248">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="dc16a-249">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="dc16a-249">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="dc16a-250">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-250">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dc16a-251">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dc16a-251">Az.Monitor</span></span>
* <span data-ttu-id="dc16a-252">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-252">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="dc16a-253">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="dc16a-253">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="dc16a-254">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="dc16a-254">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-255">Az.Network</span></span>
* <span data-ttu-id="dc16a-256">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-256">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-257">Az.Resources</span></span>
* <span data-ttu-id="dc16a-258">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-258">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="dc16a-259">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-259">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-260">Az.Sql</span></span>
* <span data-ttu-id="dc16a-261">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-261">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-262">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-262">Az.Storage</span></span>
* <span data-ttu-id="dc16a-263">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="dc16a-263">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="dc16a-264">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="dc16a-264">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="dc16a-265">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="dc16a-265">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="dc16a-266">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="dc16a-266">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="dc16a-267">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="dc16a-267">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="dc16a-268">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-268">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="dc16a-269">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-269">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="dc16a-270">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dc16a-270">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="dc16a-271">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dc16a-271">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="dc16a-272">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-272">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="dc16a-273">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="dc16a-273">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="dc16a-274">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-274">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="dc16a-275">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="dc16a-275">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="dc16a-276">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-276">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dc16a-277">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="dc16a-277">Highlights since the last major release</span></span>
* <span data-ttu-id="dc16a-278">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="dc16a-278">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="dc16a-279">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="dc16a-279">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-280">Az.Compute</span></span>
* <span data-ttu-id="dc16a-281">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="dc16a-281">VM Reapply feature</span></span>
    - <span data-ttu-id="dc16a-282">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="dc16a-282">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="dc16a-283">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="dc16a-283">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="dc16a-284">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dc16a-284">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="dc16a-285">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="dc16a-285">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="dc16a-286">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-286">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="dc16a-287">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-287">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="dc16a-288">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-288">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="dc16a-289">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-289">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="dc16a-290">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-290">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="dc16a-291">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-291">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="dc16a-292">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="dc16a-292">Az.DataBoxEdge</span></span>
* <span data-ttu-id="dc16a-293">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-293">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="dc16a-294">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="dc16a-294">Get the Order</span></span>
* <span data-ttu-id="dc16a-295">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-295">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="dc16a-296">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="dc16a-296">Create new Order</span></span>
* <span data-ttu-id="dc16a-297">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-297">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="dc16a-298">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="dc16a-298">Remove the Order</span></span>
* <span data-ttu-id="dc16a-299">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="dc16a-299">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="dc16a-300">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="dc16a-300">Now creates Local Share</span></span>
* <span data-ttu-id="dc16a-301">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-301">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="dc16a-302">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="dc16a-302">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="dc16a-303">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-303">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="dc16a-304">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="dc16a-304">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="dc16a-305">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-305">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="dc16a-306">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="dc16a-306">Gets the information about Triggers</span></span>
* <span data-ttu-id="dc16a-307">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-307">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="dc16a-308">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="dc16a-308">Create new Triggers</span></span>
* <span data-ttu-id="dc16a-309">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-309">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="dc16a-310">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="dc16a-310">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-311">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-311">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-312">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-312">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="dc16a-313">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-313">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-314">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-314">Az.DataLakeStore</span></span>
* <span data-ttu-id="dc16a-315">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-315">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dc16a-316">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-316">Az.EventHub</span></span>
* <span data-ttu-id="dc16a-317">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-317">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dc16a-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dc16a-318">Az.FrontDoor</span></span>
* <span data-ttu-id="dc16a-319">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-319">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="dc16a-320">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-320">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="dc16a-321">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-321">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="dc16a-322">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="dc16a-322">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-323">Az.Network</span></span>
* <span data-ttu-id="dc16a-324">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-324">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="dc16a-325">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="dc16a-325">Az.PrivateDns</span></span>
* <span data-ttu-id="dc16a-326">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-326">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-327">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-327">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-328">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-328">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="dc16a-329">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-329">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="dc16a-330">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-330">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dc16a-331">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dc16a-331">Az.RedisCache</span></span>
* <span data-ttu-id="dc16a-332">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-332">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="dc16a-333">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-333">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="dc16a-334">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-334">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-335">Az.Resources</span></span>
- <span data-ttu-id="dc16a-336">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-336">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="dc16a-337">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-337">Updated create policy definition help example</span></span>
- <span data-ttu-id="dc16a-338">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-338">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="dc16a-339">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-339">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="dc16a-340">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-340">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-341">Az.Sql</span></span>
* <span data-ttu-id="dc16a-342">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-342">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="dc16a-343">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-343">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="dc16a-344">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-344">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="dc16a-345">Genel</span><span class="sxs-lookup"><span data-stu-id="dc16a-345">General</span></span>
* <span data-ttu-id="dc16a-346">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="dc16a-346">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dc16a-347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-347">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-348">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dc16a-348">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="dc16a-349">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="dc16a-349">Az.Advisor</span></span>
* <span data-ttu-id="dc16a-350">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-350">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dc16a-351">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dc16a-351">Az.Batch</span></span>
* <span data-ttu-id="dc16a-352">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-352">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="dc16a-353">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="dc16a-353">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="dc16a-354">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-354">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="dc16a-355">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-355">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="dc16a-356">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="dc16a-356">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="dc16a-357">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="dc16a-357">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="dc16a-358">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="dc16a-358">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="dc16a-359">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-359">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="dc16a-360">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-360">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="dc16a-361">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-361">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="dc16a-362">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="dc16a-362">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="dc16a-363">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="dc16a-363">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="dc16a-364">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-364">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="dc16a-365">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="dc16a-365">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="dc16a-366">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-366">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="dc16a-367">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-367">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="dc16a-368">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-368">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="dc16a-369">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-369">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="dc16a-370">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-370">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="dc16a-371">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-371">This operation is no longer supported.</span></span>
* <span data-ttu-id="dc16a-372">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-372">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="dc16a-373">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-373">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="dc16a-374">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-374">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="dc16a-375">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-375">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="dc16a-376">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-376">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="dc16a-377">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-377">New non-verified images are also now returned.</span></span> <span data-ttu-id="dc16a-378">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-378">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="dc16a-379">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-379">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="dc16a-380">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-380">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="dc16a-381">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-381">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="dc16a-382">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-382">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="dc16a-383">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-383">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="dc16a-384">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-384">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="dc16a-385">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-385">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="dc16a-386">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="dc16a-386">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="dc16a-387">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="dc16a-387">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dc16a-388">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dc16a-388">Az.Cdn</span></span>
* <span data-ttu-id="dc16a-389">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-389">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="dc16a-390">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-390">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-391">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-391">Az.Compute</span></span>
* <span data-ttu-id="dc16a-392">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="dc16a-392">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="dc16a-393">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="dc16a-393">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="dc16a-394">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="dc16a-394">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="dc16a-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="dc16a-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="dc16a-396">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-396">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="dc16a-397">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-397">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="dc16a-398">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="dc16a-398">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="dc16a-399">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-399">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="dc16a-400">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="dc16a-400">Breaking changes</span></span>
    - <span data-ttu-id="dc16a-401">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-401">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="dc16a-402">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="dc16a-402">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-403">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-404">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-404">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="dc16a-406">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-406">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="dc16a-407">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="dc16a-407">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="dc16a-408">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="dc16a-408">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="dc16a-409">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="dc16a-409">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="dc16a-410">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="dc16a-410">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="dc16a-411">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="dc16a-411">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dc16a-412">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dc16a-412">Az.FrontDoor</span></span>
* <span data-ttu-id="dc16a-413">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-413">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dc16a-414">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dc16a-414">Az.HDInsight</span></span>
* <span data-ttu-id="dc16a-415">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-415">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="dc16a-416">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-416">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="dc16a-417">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-417">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="dc16a-418">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="dc16a-418">Removed five cmdlets:</span></span>
    - <span data-ttu-id="dc16a-419">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="dc16a-419">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="dc16a-420">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="dc16a-420">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="dc16a-421">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="dc16a-421">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="dc16a-422">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dc16a-422">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="dc16a-423">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dc16a-423">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="dc16a-424">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-424">Added three cmdlets:</span></span>
    - <span data-ttu-id="dc16a-425">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="dc16a-425">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="dc16a-426">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="dc16a-426">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="dc16a-427">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="dc16a-427">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="dc16a-428">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-428">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="dc16a-429">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-429">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="dc16a-430">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-430">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="dc16a-431">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-431">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="dc16a-432">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-432">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="dc16a-433">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-433">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="dc16a-434">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-434">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="dc16a-435">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-435">Added some scenario test cases.</span></span>
* <span data-ttu-id="dc16a-436">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="dc16a-436">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dc16a-437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-437">Az.IotHub</span></span>
* <span data-ttu-id="dc16a-438">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="dc16a-438">Breaking changes:</span></span>
    - <span data-ttu-id="dc16a-439">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-439">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="dc16a-440">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-440">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="dc16a-441">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-441">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="dc16a-442">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-442">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="dc16a-443">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-443">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="dc16a-444">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-444">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="dc16a-445">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-445">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="dc16a-446">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-446">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="dc16a-447">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-447">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="dc16a-448">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-448">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="dc16a-449">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-449">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="dc16a-450">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-450">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-451">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-451">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-452">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-452">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="dc16a-453">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-453">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="dc16a-454">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-454">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="dc16a-455">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-455">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="dc16a-456">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-456">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="dc16a-457">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-457">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="dc16a-458">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-458">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="dc16a-459">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-459">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="dc16a-460">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-460">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-461">Az.Resources</span></span>
* <span data-ttu-id="dc16a-462">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-462">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-463">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-463">Az.Network</span></span>
* <span data-ttu-id="dc16a-464">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-464">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="dc16a-465">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-465">Updated cmdlet:</span></span>
        - <span data-ttu-id="dc16a-466">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-466">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dc16a-467">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-467">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dc16a-468">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-468">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dc16a-469">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-469">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dc16a-470">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-470">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="dc16a-471">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-471">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="dc16a-472">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="dc16a-472">New cmdlet:</span></span>
        - <span data-ttu-id="dc16a-473">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="dc16a-473">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="dc16a-474">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-474">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="dc16a-475">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-475">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="dc16a-476">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-476">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="dc16a-477">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-477">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="dc16a-478">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-478">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="dc16a-479">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-479">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="dc16a-480">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-480">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="dc16a-481">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-481">New cmdlets added:</span></span>
        - <span data-ttu-id="dc16a-482">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="dc16a-482">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="dc16a-483">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc16a-483">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="dc16a-484">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc16a-484">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="dc16a-485">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc16a-485">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="dc16a-486">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-486">Set-AzVirtualHub</span></span>
* <span data-ttu-id="dc16a-487">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-487">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="dc16a-488">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-488">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="dc16a-489">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-489">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="dc16a-490">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-490">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="dc16a-491">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-491">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="dc16a-492">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-492">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="dc16a-493">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-493">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="dc16a-494">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-494">New cmdlets added:</span></span>
        - <span data-ttu-id="dc16a-495">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-495">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="dc16a-496">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-496">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="dc16a-497">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-497">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="dc16a-498">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-498">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="dc16a-499">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-499">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="dc16a-500">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-500">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="dc16a-501">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-501">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="dc16a-502">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-502">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="dc16a-503">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-503">New cmdlets added:</span></span>
        - <span data-ttu-id="dc16a-504">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="dc16a-504">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="dc16a-505">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="dc16a-505">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="dc16a-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="dc16a-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="dc16a-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="dc16a-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="dc16a-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="dc16a-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="dc16a-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc16a-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="dc16a-510">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-510">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="dc16a-511">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-511">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="dc16a-512">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-512">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="dc16a-513">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-513">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="dc16a-514">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-514">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="dc16a-515">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-515">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="dc16a-516">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-516">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="dc16a-517">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-517">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="dc16a-518">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-518">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="dc16a-519">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="dc16a-519">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="dc16a-520">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-520">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="dc16a-521">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-521">New cmdlets added:</span></span>
        - <span data-ttu-id="dc16a-522">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="dc16a-522">New-AzIpGroup</span></span>
        - <span data-ttu-id="dc16a-523">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="dc16a-523">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="dc16a-524">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="dc16a-524">Get-AzIpGroup</span></span>
        - <span data-ttu-id="dc16a-525">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="dc16a-525">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dc16a-526">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc16a-526">Az.ServiceFabric</span></span>
* <span data-ttu-id="dc16a-527">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-527">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-528">Az.Sql</span></span>
* <span data-ttu-id="dc16a-529">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-529">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="dc16a-530">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-530">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="dc16a-531">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="dc16a-531">Removed deprecated aliases:</span></span>
* <span data-ttu-id="dc16a-532">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="dc16a-532">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="dc16a-533">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="dc16a-533">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="dc16a-534">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-534">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="dc16a-535">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-535">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="dc16a-536">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-536">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="dc16a-537">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-537">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-538">Az.Storage</span></span>
* <span data-ttu-id="dc16a-539">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="dc16a-539">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="dc16a-540">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-540">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="dc16a-541">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-541">Set-AzStorageAccount</span></span>
* <span data-ttu-id="dc16a-542">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="dc16a-542">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="dc16a-543">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dc16a-543">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="dc16a-544">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dc16a-544">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="dc16a-545">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-545">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="dc16a-546">Genel</span><span class="sxs-lookup"><span data-stu-id="dc16a-546">General</span></span>
* <span data-ttu-id="dc16a-547">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="dc16a-547">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dc16a-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-548">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-549">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-549">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dc16a-550">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc16a-550">Az.ApiManagement</span></span>
* <span data-ttu-id="dc16a-551">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-551">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="dc16a-552">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-552">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dc16a-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dc16a-553">Az.Automation</span></span>
* <span data-ttu-id="dc16a-554">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-554">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="dc16a-555">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dc16a-555">Az.Batch</span></span>
* <span data-ttu-id="dc16a-556">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="dc16a-556">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-557">Az.Compute</span></span>
* <span data-ttu-id="dc16a-558">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-558">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="dc16a-559">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-559">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="dc16a-560">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-560">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="dc16a-561">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-561">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-562">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-562">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-563">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="dc16a-563">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="dc16a-564">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="dc16a-564">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="dc16a-565">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-565">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-566">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-566">Az.DataLakeStore</span></span>
* <span data-ttu-id="dc16a-567">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-567">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="dc16a-568">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="dc16a-568">Az.HealthcareApis</span></span>
* <span data-ttu-id="dc16a-569">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-569">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="dc16a-570">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-570">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="dc16a-571">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-571">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="dc16a-572">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-572">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dc16a-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-573">Az.IotHub</span></span>
* <span data-ttu-id="dc16a-574">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="dc16a-574">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="dc16a-575">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-575">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="dc16a-576">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dc16a-576">Az.Monitor</span></span>
* <span data-ttu-id="dc16a-577">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-577">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="dc16a-578">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc16a-578">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="dc16a-579">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="dc16a-579">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="dc16a-580">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-580">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-581">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-581">Az.Network</span></span>
* <span data-ttu-id="dc16a-582">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-582">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="dc16a-583">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-583">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="dc16a-584">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-584">New cmdlets added:</span></span>
        - <span data-ttu-id="dc16a-585">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="dc16a-585">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="dc16a-586">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-586">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="dc16a-587">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-587">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="dc16a-588">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-588">Updated cmdlets:</span></span>
        - <span data-ttu-id="dc16a-589">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-589">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dc16a-590">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-590">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dc16a-591">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-591">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="dc16a-592">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-592">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="dc16a-593">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="dc16a-593">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="dc16a-594">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="dc16a-594">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="dc16a-595">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="dc16a-595">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dc16a-596">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dc16a-596">Az.RedisCache</span></span>
* <span data-ttu-id="dc16a-597">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-597">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-598">Az.Sql</span></span>
* <span data-ttu-id="dc16a-599">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-599">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-600">Az.Storage</span></span>
* <span data-ttu-id="dc16a-601">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-601">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="dc16a-602">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="dc16a-602">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="dc16a-603">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="dc16a-603">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="dc16a-604">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="dc16a-604">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="dc16a-605">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-605">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dc16a-606">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dc16a-606">Az.StorageSync</span></span>
* <span data-ttu-id="dc16a-607">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-607">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-608">Az.Websites</span></span>
* <span data-ttu-id="dc16a-609">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-609">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="dc16a-610">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-610">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="dc16a-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc16a-611">Az.ApiManagement</span></span>
* <span data-ttu-id="dc16a-612">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-612">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="dc16a-613">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-613">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="dc16a-614">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc16a-614">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dc16a-615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dc16a-615">Az.Automation</span></span>
* <span data-ttu-id="dc16a-616">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-616">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="dc16a-617">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-617">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="dc16a-618">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-618">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-619">Az.Compute</span></span>
* <span data-ttu-id="dc16a-620">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-620">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="dc16a-621">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-621">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="dc16a-622">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-622">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="dc16a-623">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-623">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="dc16a-624">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-624">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="dc16a-625">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-625">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="dc16a-626">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-626">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="dc16a-627">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-627">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="dc16a-628">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-628">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-629">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-629">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-630">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="dc16a-630">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="dc16a-631">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-631">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dc16a-632">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dc16a-632">Az.HDInsight</span></span>
* <span data-ttu-id="dc16a-633">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="dc16a-633">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dc16a-634">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-634">Az.IotHub</span></span>
* <span data-ttu-id="dc16a-635">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-635">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="dc16a-636">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-636">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="dc16a-637">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="dc16a-637">New cmdlets are:</span></span>
    - <span data-ttu-id="dc16a-638">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dc16a-638">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="dc16a-639">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dc16a-639">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="dc16a-640">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dc16a-640">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="dc16a-641">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dc16a-641">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dc16a-642">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dc16a-642">Az.Monitor</span></span>
* <span data-ttu-id="dc16a-643">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="dc16a-643">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="dc16a-644">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-644">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="dc16a-645">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="dc16a-645">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="dc16a-646">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="dc16a-646">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="dc16a-647">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-647">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="dc16a-648">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-648">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="dc16a-649">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-649">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="dc16a-650">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="dc16a-650">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="dc16a-651">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-651">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="dc16a-652">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="dc16a-652">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="dc16a-653">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-653">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="dc16a-654">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="dc16a-654">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="dc16a-655">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-655">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="dc16a-656">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="dc16a-656">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="dc16a-657">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="dc16a-657">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="dc16a-658">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="dc16a-658">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="dc16a-659">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="dc16a-659">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="dc16a-660">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="dc16a-660">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="dc16a-661">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-661">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="dc16a-662">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-662">Overall improved help files</span></span>
* <span data-ttu-id="dc16a-663">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-663">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-664">Az.Network</span></span>
* <span data-ttu-id="dc16a-665">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-665">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="dc16a-666">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-666">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="dc16a-667">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-667">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="dc16a-668">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-668">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="dc16a-669">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-669">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="dc16a-670">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-670">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="dc16a-671">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-671">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="dc16a-672">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-672">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="dc16a-673">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-673">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="dc16a-674">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-674">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="dc16a-675">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-675">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="dc16a-676">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="dc16a-676">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="dc16a-677">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-677">New cmdlets</span></span>
        - <span data-ttu-id="dc16a-678">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="dc16a-678">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="dc16a-679">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-679">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="dc16a-680">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-680">Updated cmdlet:</span></span>
        - <span data-ttu-id="dc16a-681">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="dc16a-681">New-VpnSite</span></span>
        - <span data-ttu-id="dc16a-682">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="dc16a-682">Update-VpnSite</span></span>
        - <span data-ttu-id="dc16a-683">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-683">New-VpnConnection</span></span>
        - <span data-ttu-id="dc16a-684">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-684">Update-VpnConnection</span></span>
* <span data-ttu-id="dc16a-685">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-685">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-686">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-686">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-687">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-687">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="dc16a-688">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-688">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-689">Az.Resources</span></span>
* <span data-ttu-id="dc16a-690">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-690">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dc16a-691">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc16a-691">Az.ServiceFabric</span></span>
* <span data-ttu-id="dc16a-692">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-692">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="dc16a-693">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="dc16a-693">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="dc16a-694">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dc16a-694">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dc16a-695">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dc16a-695">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="dc16a-696">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="dc16a-696">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="dc16a-697">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="dc16a-697">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="dc16a-698">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dc16a-698">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dc16a-699">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dc16a-699">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dc16a-700">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dc16a-700">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="dc16a-701">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="dc16a-701">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="dc16a-702">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="dc16a-702">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="dc16a-703">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dc16a-703">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dc16a-704">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dc16a-704">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="dc16a-705">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="dc16a-705">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="dc16a-706">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="dc16a-706">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="dc16a-707">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-707">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dc16a-708">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dc16a-708">Az.SignalR</span></span>
* <span data-ttu-id="dc16a-709">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-709">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-710">Az.Sql</span></span>
* <span data-ttu-id="dc16a-711">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-711">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="dc16a-712">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-712">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="dc16a-713">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-713">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="dc16a-714">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-714">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="dc16a-715">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-715">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-716">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-716">Az.Storage</span></span>
* <span data-ttu-id="dc16a-717">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-717">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="dc16a-718">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-718">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="dc16a-719">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dc16a-719">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="dc16a-720">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dc16a-720">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="dc16a-721">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-721">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="dc16a-722">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dc16a-722">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="dc16a-723">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-723">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="dc16a-724">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dc16a-724">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="dc16a-725">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dc16a-725">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="dc16a-726">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dc16a-726">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="dc16a-727">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dc16a-727">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-728">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-728">Az.Websites</span></span>
* <span data-ttu-id="dc16a-729">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-729">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="dc16a-730">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-730">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="dc16a-731">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-731">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="dc16a-732">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-732">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="dc16a-733">Genel</span><span class="sxs-lookup"><span data-stu-id="dc16a-733">General</span></span>
* <span data-ttu-id="dc16a-734">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-734">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dc16a-735">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-735">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-736">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="dc16a-736">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="dc16a-737">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dc16a-737">Az.Aks</span></span>
* <span data-ttu-id="dc16a-738">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-738">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="dc16a-739">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="dc16a-739">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dc16a-740">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc16a-740">Az.ApiManagement</span></span>
* <span data-ttu-id="dc16a-741">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-741">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="dc16a-742">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-742">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="dc16a-743">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-743">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="dc16a-744">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="dc16a-744">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="dc16a-745">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-745">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dc16a-746">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dc16a-746">Az.Batch</span></span>
* <span data-ttu-id="dc16a-747">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-747">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dc16a-748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dc16a-748">Az.Cdn</span></span>
* <span data-ttu-id="dc16a-749">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-749">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-750">Az.Compute</span></span>
* <span data-ttu-id="dc16a-751">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-751">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="dc16a-752">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-752">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="dc16a-753">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-753">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="dc16a-754">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-754">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="dc16a-755">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="dc16a-755">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="dc16a-756">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-756">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="dc16a-757">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-757">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="dc16a-758">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-758">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-759">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-760">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-760">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="dc16a-761">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-761">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="dc16a-762">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-762">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="dc16a-763">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-763">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-764">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-764">Az.DataLakeStore</span></span>
* <span data-ttu-id="dc16a-765">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-765">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dc16a-766">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-766">Az.EventHub</span></span>
* <span data-ttu-id="dc16a-767">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="dc16a-767">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="dc16a-768">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="dc16a-768">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="dc16a-769">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-769">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="dc16a-770">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="dc16a-770">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="dc16a-771">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="dc16a-771">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="dc16a-772">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-772">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dc16a-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dc16a-773">Az.Monitor</span></span>
* <span data-ttu-id="dc16a-774">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-774">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-775">Az.Network</span></span>
* <span data-ttu-id="dc16a-776">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-776">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="dc16a-777">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-777">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="dc16a-778">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-778">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="dc16a-779">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="dc16a-779">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="dc16a-780">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-780">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="dc16a-781">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-781">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="dc16a-782">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-782">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dc16a-783">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-783">Az.OperationalInsights</span></span>
* <span data-ttu-id="dc16a-784">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-784">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="dc16a-785">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-785">Added example</span></span>
    - <span data-ttu-id="dc16a-786">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-786">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="dc16a-787">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-787">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="dc16a-788">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-788">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-789">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-789">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-790">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-790">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-791">Az.Resources</span></span>
* <span data-ttu-id="dc16a-792">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-792">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="dc16a-793">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-793">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="dc16a-794">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="dc16a-794">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="dc16a-795">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-795">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dc16a-796">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dc16a-796">Az.ServiceBus</span></span>
* <span data-ttu-id="dc16a-797">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="dc16a-797">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="dc16a-798">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="dc16a-798">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="dc16a-799">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-799">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="dc16a-800">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc16a-800">Az.ServiceFabric</span></span>
* <span data-ttu-id="dc16a-801">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-801">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="dc16a-802">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="dc16a-802">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="dc16a-803">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="dc16a-803">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="dc16a-804">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-804">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="dc16a-805">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="dc16a-805">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="dc16a-806">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-806">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-807">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-807">Az.Sql</span></span>
* <span data-ttu-id="dc16a-808">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-808">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-809">Az.Storage</span></span>
* <span data-ttu-id="dc16a-810">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-810">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="dc16a-811">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="dc16a-811">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="dc16a-812">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dc16a-812">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="dc16a-813">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dc16a-813">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="dc16a-814">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="dc16a-814">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="dc16a-815">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dc16a-815">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-816">Az.Websites</span></span>
* <span data-ttu-id="dc16a-817">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-817">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="dc16a-818">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-818">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dc16a-819">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-819">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-820">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-820">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="dc16a-821">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-821">Az.ApplicationInsights</span></span>
* <span data-ttu-id="dc16a-822">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-822">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="dc16a-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dc16a-823">Az.Automation</span></span>
* <span data-ttu-id="dc16a-824">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-824">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="dc16a-825">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-825">Az.CognitiveServices</span></span>
* <span data-ttu-id="dc16a-826">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-826">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-827">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-827">Az.Compute</span></span>
* <span data-ttu-id="dc16a-828">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-828">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="dc16a-829">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dc16a-829">Az.ContainerRegistry</span></span>
* <span data-ttu-id="dc16a-830">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-830">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="dc16a-831">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="dc16a-831">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-832">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-832">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-833">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-833">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="dc16a-834">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-834">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dc16a-835">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-835">Az.EventHub</span></span>
* <span data-ttu-id="dc16a-836">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="dc16a-836">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="dc16a-837">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-837">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dc16a-838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc16a-838">Az.KeyVault</span></span>
* <span data-ttu-id="dc16a-839">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-839">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dc16a-840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dc16a-840">Az.LogicApp</span></span>
* <span data-ttu-id="dc16a-841">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="dc16a-841">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="dc16a-842">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-842">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="dc16a-843">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-843">Az.ManagedServices</span></span>
* <span data-ttu-id="dc16a-844">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="dc16a-844">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-845">Az.Network</span></span>
* <span data-ttu-id="dc16a-846">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-846">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="dc16a-847">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-847">New cmdlets</span></span>
        - <span data-ttu-id="dc16a-848">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc16a-848">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dc16a-849">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dc16a-849">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dc16a-850">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-850">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dc16a-851">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-851">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dc16a-852">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-852">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dc16a-853">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-853">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dc16a-854">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="dc16a-854">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="dc16a-855">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dc16a-855">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="dc16a-856">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="dc16a-856">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="dc16a-857">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-857">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="dc16a-858">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-858">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="dc16a-859">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-859">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="dc16a-860">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-860">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="dc16a-861">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-861">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="dc16a-862">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-862">Updated cmdlets</span></span>
        - <span data-ttu-id="dc16a-863">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-863">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dc16a-864">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-864">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dc16a-865">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-865">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="dc16a-866">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-866">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="dc16a-867">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-867">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="dc16a-868">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-868">Updated cmdlet:</span></span>
        - <span data-ttu-id="dc16a-869">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-869">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="dc16a-870">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-870">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="dc16a-871">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-871">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="dc16a-872">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-872">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="dc16a-873">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-873">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="dc16a-874">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="dc16a-874">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dc16a-875">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-875">Az.OperationalInsights</span></span>
* <span data-ttu-id="dc16a-876">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-876">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="dc16a-877">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-877">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-878">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-878">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-879">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-879">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="dc16a-880">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-880">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="dc16a-881">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-881">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="dc16a-882">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-882">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="dc16a-883">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-883">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="dc16a-884">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-884">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="dc16a-885">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-885">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="dc16a-886">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-886">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="dc16a-887">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-887">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="dc16a-888">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-888">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-889">Az.Resources</span></span>
- <span data-ttu-id="dc16a-890">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-890">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="dc16a-891">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-891">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dc16a-892">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dc16a-892">Az.ServiceBus</span></span>
* <span data-ttu-id="dc16a-893">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="dc16a-893">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="dc16a-894">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-894">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-895">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-895">Az.Sql</span></span>
* <span data-ttu-id="dc16a-896">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-896">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="dc16a-897">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-897">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="dc16a-898">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-898">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-899">Az.Storage</span></span>
* <span data-ttu-id="dc16a-900">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-900">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dc16a-901">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dc16a-901">Az.StorageSync</span></span>
* <span data-ttu-id="dc16a-902">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-902">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="dc16a-903">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-903">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-904">Az.Websites</span></span>
* <span data-ttu-id="dc16a-905">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-905">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="dc16a-906">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-906">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="dc16a-907">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-907">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="dc16a-908">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-908">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dc16a-909">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-909">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-910">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-910">Add support for profile cmdlets</span></span>
* <span data-ttu-id="dc16a-911">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-911">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="dc16a-912">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-912">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="dc16a-913">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="dc16a-913">Az.Advisor</span></span>
* <span data-ttu-id="dc16a-914">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="dc16a-914">GA release of Az.Advisor</span></span>
* <span data-ttu-id="dc16a-915">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="dc16a-915">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dc16a-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc16a-916">Az.ApiManagement</span></span>
* <span data-ttu-id="dc16a-917">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-917">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="dc16a-918">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="dc16a-918">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="dc16a-919">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-919">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="dc16a-920">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="dc16a-920">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="dc16a-921">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="dc16a-921">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="dc16a-922">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="dc16a-922">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="dc16a-923">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-923">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dc16a-924">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dc16a-924">Az.Automation</span></span>
* <span data-ttu-id="dc16a-925">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-925">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-926">Az.Compute</span></span>
* <span data-ttu-id="dc16a-927">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-927">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-928">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-928">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-929">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-929">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dc16a-930">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dc16a-930">Az.EventGrid</span></span>
* <span data-ttu-id="dc16a-931">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-931">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dc16a-932">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-932">Az.IotHub</span></span>
* <span data-ttu-id="dc16a-933">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-933">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-934">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-934">Az.Network</span></span>
* <span data-ttu-id="dc16a-935">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-935">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="dc16a-936">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-936">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dc16a-937">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-937">Az.PolicyInsights</span></span>
* <span data-ttu-id="dc16a-938">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-938">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="dc16a-939">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="dc16a-939">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dc16a-940">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-940">Az.OperationalInsights</span></span>
* <span data-ttu-id="dc16a-941">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-941">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-942">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-942">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-943">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="dc16a-943">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-944">Az.Resources</span></span>
    - <span data-ttu-id="dc16a-945">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="dc16a-945">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="dc16a-946">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-946">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="dc16a-947">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-947">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="dc16a-948">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-948">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dc16a-949">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dc16a-949">Az.ServiceBus</span></span>
* <span data-ttu-id="dc16a-950">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-950">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-951">Az.Sql</span></span>
* <span data-ttu-id="dc16a-952">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-952">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="dc16a-953">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-953">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="dc16a-954">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="dc16a-954">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="dc16a-955">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="dc16a-955">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="dc16a-956">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="dc16a-956">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="dc16a-957">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dc16a-957">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="dc16a-958">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dc16a-958">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="dc16a-959">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dc16a-959">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="dc16a-960">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-960">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-961">Az.Storage</span></span>
* <span data-ttu-id="dc16a-962">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-962">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="dc16a-963">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="dc16a-963">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="dc16a-964">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-964">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="dc16a-965">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-965">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="dc16a-966">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-966">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="dc16a-967">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-967">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="dc16a-968">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-968">Set-AzStorageAccount</span></span>
* <span data-ttu-id="dc16a-969">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-969">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="dc16a-970">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dc16a-970">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="dc16a-971">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dc16a-971">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dc16a-972">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dc16a-972">Az.StorageSync</span></span>
* <span data-ttu-id="dc16a-973">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="dc16a-973">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="dc16a-974">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-974">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dc16a-975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-975">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-976">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-976">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="dc16a-977">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="dc16a-977">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="dc16a-978">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-978">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="dc16a-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="dc16a-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="dc16a-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="dc16a-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-981">Az.Compute</span></span>
* <span data-ttu-id="dc16a-982">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-982">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="dc16a-983">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-983">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="dc16a-984">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="dc16a-984">Az.Dns</span></span>
* <span data-ttu-id="dc16a-985">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-985">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dc16a-986">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dc16a-986">Az.EventGrid</span></span>
* <span data-ttu-id="dc16a-987">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-987">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="dc16a-988">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="dc16a-988">New cmdlets:</span></span>
    - <span data-ttu-id="dc16a-989">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dc16a-989">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="dc16a-990">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc16a-990">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="dc16a-991">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dc16a-991">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="dc16a-992">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="dc16a-992">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="dc16a-993">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dc16a-993">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="dc16a-994">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dc16a-994">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="dc16a-995">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="dc16a-995">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="dc16a-996">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="dc16a-996">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="dc16a-997">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="dc16a-997">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="dc16a-998">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="dc16a-998">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="dc16a-999">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="dc16a-999">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="dc16a-1000">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1000">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="dc16a-1001">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="dc16a-1001">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="dc16a-1002">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="dc16a-1002">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="dc16a-1003">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1003">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="dc16a-1004">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1004">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="dc16a-1005">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1005">Updated cmdlets:</span></span>
    - <span data-ttu-id="dc16a-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="dc16a-1007">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1007">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="dc16a-1008">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1008">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="dc16a-1009">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1009">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="dc16a-1010">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1010">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="dc16a-1011">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="dc16a-1011">Event subscription expiration date,</span></span>
            - <span data-ttu-id="dc16a-1012">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1012">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="dc16a-1013">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1013">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="dc16a-1014">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="dc16a-1014">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="dc16a-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="dc16a-1016">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1016">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="dc16a-1017">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="dc16a-1017">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="dc16a-1018">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1018">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="dc16a-1019">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1019">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dc16a-1020">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1020">Az.FrontDoor</span></span>
* <span data-ttu-id="dc16a-1021">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="dc16a-1021">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="dc16a-1022">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1022">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="dc16a-1023">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="dc16a-1023">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="dc16a-1024">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1024">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1025">Az.Network</span></span>
* <span data-ttu-id="dc16a-1026">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1026">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="dc16a-1027">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1027">New cmdlets</span></span>
        - <span data-ttu-id="dc16a-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="dc16a-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="dc16a-1029">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1029">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="dc16a-1030">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1030">New cmdlets</span></span> 
        - <span data-ttu-id="dc16a-1031">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="dc16a-1031">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="dc16a-1032">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1032">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="dc16a-1033">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1033">New cmdlets</span></span> 
        - <span data-ttu-id="dc16a-1034">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dc16a-1034">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="dc16a-1035">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dc16a-1035">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dc16a-1036">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dc16a-1036">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dc16a-1037">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-1037">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="dc16a-1038">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-1038">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="dc16a-1039">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1039">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="dc16a-1040">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1040">New cmdlets</span></span>
        - <span data-ttu-id="dc16a-1041">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc16a-1041">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dc16a-1042">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc16a-1042">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dc16a-1043">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc16a-1043">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dc16a-1044">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="dc16a-1044">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="dc16a-1045">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="dc16a-1045">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="dc16a-1046">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1046">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="dc16a-1047">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1047">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="dc16a-1048">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1048">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="dc16a-1049">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1049">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="dc16a-1050">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1050">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="dc16a-1051">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1051">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="dc16a-1052">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1052">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="dc16a-1053">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1053">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="dc16a-1054">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1054">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="dc16a-1055">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1055">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="dc16a-1056">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1056">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="dc16a-1057">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1057">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="dc16a-1058">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1058">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="dc16a-1059">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1059">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="dc16a-1060">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1060">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="dc16a-1061">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1061">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="dc16a-1062">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="dc16a-1062">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="dc16a-1063">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="dc16a-1063">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="dc16a-1064">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1064">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="dc16a-1065">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1065">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="dc16a-1066">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1066">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="dc16a-1067">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1067">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dc16a-1068">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-1068">Az.OperationalInsights</span></span>
* <span data-ttu-id="dc16a-1069">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1069">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-1070">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1070">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1071">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="dc16a-1071">Support for additional Template Export options</span></span>
    - <span data-ttu-id="dc16a-1072">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1072">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="dc16a-1073">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1073">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="dc16a-1074">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1074">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dc16a-1075">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc16a-1075">Az.ServiceFabric</span></span>
* <span data-ttu-id="dc16a-1076">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1076">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-1077">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1077">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1078">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1078">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="dc16a-1079">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1079">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="dc16a-1080">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1080">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="dc16a-1081">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dc16a-1081">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="dc16a-1082">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dc16a-1082">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="dc16a-1083">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dc16a-1083">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="dc16a-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="dc16a-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="dc16a-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="dc16a-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-1086">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-1086">Az.Storage</span></span>
* <span data-ttu-id="dc16a-1087">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="dc16a-1087">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="dc16a-1088">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-1088">New-AzStorageAccount</span></span>
* <span data-ttu-id="dc16a-1089">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1089">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="dc16a-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="dc16a-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-1091">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-1091">Az.Websites</span></span>
* <span data-ttu-id="dc16a-1092">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="dc16a-1092">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="dc16a-1093">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1093">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="dc16a-1094">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-1094">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="dc16a-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dc16a-1095">Az.Cdn</span></span>
* <span data-ttu-id="dc16a-1096">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1096">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1097">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1098">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1098">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="dc16a-1099">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="dc16a-1099">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dc16a-1100">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-1100">Az.EventHub</span></span>
* <span data-ttu-id="dc16a-1101">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1101">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="dc16a-1102">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1102">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-1103">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1103">Az.Network</span></span>
* <span data-ttu-id="dc16a-1104">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1104">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="dc16a-1105">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1105">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dc16a-1106">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-1106">Az.PolicyInsights</span></span>
* <span data-ttu-id="dc16a-1107">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1107">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-1108">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1108">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-1109">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1109">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dc16a-1110">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dc16a-1110">Az.ServiceBus</span></span>
* <span data-ttu-id="dc16a-1111">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="dc16a-1111">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dc16a-1112">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc16a-1112">Az.ServiceFabric</span></span>
* <span data-ttu-id="dc16a-1113">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1113">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="dc16a-1114">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1114">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-1115">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1115">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1116">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1116">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="dc16a-1117">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-1117">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="dc16a-1118">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-1118">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="dc16a-1119">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1119">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-1120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-1120">Az.Websites</span></span>
* <span data-ttu-id="dc16a-1121">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1121">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="dc16a-1122">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-1122">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="dc16a-1123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc16a-1123">Az.ApiManagement</span></span>
* <span data-ttu-id="dc16a-1124">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1124">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="dc16a-1125">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="dc16a-1125">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="dc16a-1126">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="dc16a-1126">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="dc16a-1127">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="dc16a-1127">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="dc16a-1128">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1128">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="dc16a-1129">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="dc16a-1129">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="dc16a-1130">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="dc16a-1130">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="dc16a-1131">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="dc16a-1131">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="dc16a-1132">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1132">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="dc16a-1133">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="dc16a-1133">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="dc16a-1134">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="dc16a-1134">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="dc16a-1135">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="dc16a-1135">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="dc16a-1136">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="dc16a-1136">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="dc16a-1137">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1137">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="dc16a-1138">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="dc16a-1138">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="dc16a-1139">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="dc16a-1139">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="dc16a-1140">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="dc16a-1140">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="dc16a-1141">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="dc16a-1141">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="dc16a-1142">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1142">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="dc16a-1143">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="dc16a-1143">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="dc16a-1144">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1144">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="dc16a-1145">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1145">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="dc16a-1146">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1146">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="dc16a-1147">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1147">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="dc16a-1148">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1148">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="dc16a-1149">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1149">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="dc16a-1150">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1150">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="dc16a-1151">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1151">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="dc16a-1152">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1152">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="dc16a-1153">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1153">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="dc16a-1154">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1154">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="dc16a-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="dc16a-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="dc16a-1156">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1156">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="dc16a-1157">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1157">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="dc16a-1158">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="dc16a-1158">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="dc16a-1159">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1159">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="dc16a-1160">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1160">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="dc16a-1161">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1161">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="dc16a-1162">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1162">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="dc16a-1163">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1163">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="dc16a-1164">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1164">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="dc16a-1165">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="dc16a-1165">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="dc16a-1166">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1166">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="dc16a-1167">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1167">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="dc16a-1168">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1168">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="dc16a-1169">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1169">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="dc16a-1170">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="dc16a-1170">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="dc16a-1171">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1171">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="dc16a-1172">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1172">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="dc16a-1173">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1173">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="dc16a-1174">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1174">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="dc16a-1175">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="dc16a-1175">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="dc16a-1176">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1176">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="dc16a-1177">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1177">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="dc16a-1178">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="dc16a-1178">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="dc16a-1179">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="dc16a-1179">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="dc16a-1180">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1180">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="dc16a-1181">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="dc16a-1181">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="dc16a-1182">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="dc16a-1182">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="dc16a-1183">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1183">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="dc16a-1184">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1184">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="dc16a-1185">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="dc16a-1185">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="dc16a-1186">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="dc16a-1186">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="dc16a-1187">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1187">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="dc16a-1188">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1188">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="dc16a-1189">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="dc16a-1189">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="dc16a-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="dc16a-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="dc16a-1191">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="dc16a-1191">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="dc16a-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="dc16a-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="dc16a-1193">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="dc16a-1193">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="dc16a-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="dc16a-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="dc16a-1195">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="dc16a-1195">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="dc16a-1196">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="dc16a-1196">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="dc16a-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="dc16a-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="dc16a-1198">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="dc16a-1198">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="dc16a-1199">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="dc16a-1199">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="dc16a-1200">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="dc16a-1200">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dc16a-1201">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dc16a-1201">Az.Automation</span></span>
* <span data-ttu-id="dc16a-1202">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1202">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="dc16a-1203">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1203">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="dc16a-1204">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="dc16a-1205">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1205">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="dc16a-1206">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1206">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="dc16a-1207">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1207">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="dc16a-1208">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1208">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1209">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1210">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1210">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="dc16a-1211">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1211">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-1212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-1212">Az.DataLakeStore</span></span>
* <span data-ttu-id="dc16a-1213">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1213">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dc16a-1214">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1214">Az.Monitor</span></span>
* <span data-ttu-id="dc16a-1215">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1215">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-1216">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1216">Az.Network</span></span>
* <span data-ttu-id="dc16a-1217">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1217">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="dc16a-1218">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1218">Updated cmdlet:</span></span>
        - <span data-ttu-id="dc16a-1219">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc16a-1219">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="dc16a-1220">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1220">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-1221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1221">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1222">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1222">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1223">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1224">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1224">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="dc16a-1225">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-1225">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dc16a-1226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-1226">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-1227">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="dc16a-1227">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dc16a-1228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1228">Az.CognitiveServices</span></span>
* <span data-ttu-id="dc16a-1229">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1229">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="dc16a-1230">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1230">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1231">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1232">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1232">Proximity placement group feature.</span></span>
    - <span data-ttu-id="dc16a-1233">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="dc16a-1233">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="dc16a-1234">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-1234">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="dc16a-1235">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1235">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="dc16a-1236">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1236">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="dc16a-1237">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1237">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="dc16a-1238">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1238">Breaking changes</span></span>
    - <span data-ttu-id="dc16a-1239">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1239">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="dc16a-1240">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1240">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="dc16a-1241">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="dc16a-1241">Az.DeploymentManager</span></span>
* <span data-ttu-id="dc16a-1242">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="dc16a-1242">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="dc16a-1243">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="dc16a-1243">Az.Dns</span></span>
* <span data-ttu-id="dc16a-1244">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1244">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="dc16a-1245">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1245">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="dc16a-1246">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1246">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dc16a-1247">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1247">Az.FrontDoor</span></span>
* <span data-ttu-id="dc16a-1248">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="dc16a-1248">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="dc16a-1249">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="dc16a-1249">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="dc16a-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dc16a-1250">Az.HDInsight</span></span>
* <span data-ttu-id="dc16a-1251">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1251">Removed two cmdlets:</span></span>
    - <span data-ttu-id="dc16a-1252">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dc16a-1252">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="dc16a-1253">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dc16a-1253">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="dc16a-1254">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1254">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="dc16a-1255">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1255">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="dc16a-1256">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1256">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="dc16a-1257">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1257">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dc16a-1258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1258">Az.Monitor</span></span>
* <span data-ttu-id="dc16a-1259">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1259">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="dc16a-1260">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="dc16a-1260">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="dc16a-1261">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="dc16a-1261">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="dc16a-1262">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="dc16a-1262">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="dc16a-1263">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="dc16a-1263">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="dc16a-1264">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="dc16a-1264">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="dc16a-1265">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="dc16a-1265">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="dc16a-1266">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dc16a-1266">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dc16a-1267">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dc16a-1267">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dc16a-1268">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dc16a-1268">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dc16a-1269">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dc16a-1269">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dc16a-1270">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dc16a-1270">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dc16a-1271">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1271">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="dc16a-1272">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1272">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-1273">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1273">Az.Network</span></span>
* <span data-ttu-id="dc16a-1274">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="dc16a-1274">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="dc16a-1275">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1275">New cmdlets</span></span>
        - <span data-ttu-id="dc16a-1276">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dc16a-1276">New-AzNatGateway</span></span>
        - <span data-ttu-id="dc16a-1277">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dc16a-1277">Get-AzNatGateway</span></span>
        - <span data-ttu-id="dc16a-1278">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dc16a-1278">Set-AzNatGateway</span></span>
        - <span data-ttu-id="dc16a-1279">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dc16a-1279">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="dc16a-1280">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1280">Updated cmdlets</span></span>
        - <span data-ttu-id="dc16a-1281">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="dc16a-1281">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="dc16a-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="dc16a-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="dc16a-1283">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1283">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="dc16a-1284">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1284">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="dc16a-1285">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1285">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dc16a-1286">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-1286">Az.PolicyInsights</span></span>
* <span data-ttu-id="dc16a-1287">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1287">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="dc16a-1288">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1288">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="dc16a-1289">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1289">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-1290">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1290">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-1291">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1291">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="dc16a-1292">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1292">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="dc16a-1293">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1293">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="dc16a-1294">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1294">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="dc16a-1295">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1295">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="dc16a-1296">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1296">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="dc16a-1297">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="dc16a-1297">Az.Relay</span></span>
* <span data-ttu-id="dc16a-1298">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="dc16a-1298">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dc16a-1299">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dc16a-1299">Az.ServiceBus</span></span>
* <span data-ttu-id="dc16a-1300">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1300">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-1301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-1301">Az.Storage</span></span>
* <span data-ttu-id="dc16a-1302">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1302">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="dc16a-1303">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1303">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="dc16a-1304">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="dc16a-1304">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="dc16a-1305">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-1305">New-AzStorageAccount</span></span>
* <span data-ttu-id="dc16a-1306">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="dc16a-1306">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="dc16a-1307">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-1307">New-AzStorageAccount</span></span>
    - <span data-ttu-id="dc16a-1308">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-1308">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="dc16a-1309">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-1309">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-1310">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-1310">Az.Websites</span></span>
* <span data-ttu-id="dc16a-1311">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="dc16a-1311">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="dc16a-1312">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1312">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="dc16a-1313">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-1313">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dc16a-1314">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="dc16a-1314">Highlights since the last major release</span></span>
* <span data-ttu-id="dc16a-1315">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1315">General availability of `Az` module</span></span>
* <span data-ttu-id="dc16a-1316">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="dc16a-1316">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="dc16a-1317">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="dc16a-1317">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="dc16a-1318">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1318">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="dc16a-1319">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1319">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dc16a-1320">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1320">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="dc16a-1321">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1321">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dc16a-1322">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-1322">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-1323">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1323">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dc16a-1324">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dc16a-1324">Az.Batch</span></span>
* <span data-ttu-id="dc16a-1325">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1325">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dc16a-1326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dc16a-1326">Az.Cdn</span></span>
* <span data-ttu-id="dc16a-1327">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dc16a-1328">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1328">Az.CognitiveServices</span></span>
* <span data-ttu-id="dc16a-1329">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1329">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1330">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1331">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1331">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="dc16a-1332">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dc16a-1333">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1333">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-1334">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-1334">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-1335">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1335">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-1336">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-1336">Az.DataLakeStore</span></span>
* <span data-ttu-id="dc16a-1337">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1337">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dc16a-1338">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dc16a-1338">Az.EventGrid</span></span>
* <span data-ttu-id="dc16a-1339">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1339">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dc16a-1340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-1340">Az.EventHub</span></span>
* <span data-ttu-id="dc16a-1341">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1341">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="dc16a-1342">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dc16a-1342">Az.HDInsight</span></span>
* <span data-ttu-id="dc16a-1343">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1343">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dc16a-1344">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-1344">Az.IotHub</span></span>
* <span data-ttu-id="dc16a-1345">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1345">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dc16a-1346">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc16a-1346">Az.KeyVault</span></span>
* <span data-ttu-id="dc16a-1347">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1347">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dc16a-1348">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1348">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="dc16a-1349">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="dc16a-1349">Az.MachineLearning</span></span>
* <span data-ttu-id="dc16a-1350">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="dc16a-1351">Az.Media</span><span class="sxs-lookup"><span data-stu-id="dc16a-1351">Az.Media</span></span>
* <span data-ttu-id="dc16a-1352">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dc16a-1353">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1353">Az.Monitor</span></span>
  * <span data-ttu-id="dc16a-1354">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1354">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="dc16a-1355">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="dc16a-1355">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="dc16a-1356">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="dc16a-1356">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="dc16a-1357">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="dc16a-1357">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="dc16a-1358">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="dc16a-1358">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="dc16a-1359">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="dc16a-1359">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="dc16a-1360">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1360">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-1361">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1361">Az.Network</span></span>
* <span data-ttu-id="dc16a-1362">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1362">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dc16a-1363">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1363">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="dc16a-1364">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="dc16a-1364">Az.NotificationHubs</span></span>
* <span data-ttu-id="dc16a-1365">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1365">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dc16a-1366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-1366">Az.OperationalInsights</span></span>
* <span data-ttu-id="dc16a-1367">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1367">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="dc16a-1368">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="dc16a-1368">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="dc16a-1369">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-1370">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1370">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-1371">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1371">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dc16a-1372">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1372">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="dc16a-1373">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1373">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="dc16a-1374">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1374">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dc16a-1375">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dc16a-1375">Az.RedisCache</span></span>
* <span data-ttu-id="dc16a-1376">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-1377">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1377">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1378">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1378">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-1379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1379">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1380">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1380">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="dc16a-1381">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1381">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dc16a-1382">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1382">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="dc16a-1383">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1383">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="dc16a-1384">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1384">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="dc16a-1385">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1385">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="dc16a-1386">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1386">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-1387">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-1387">Az.Websites</span></span>
* <span data-ttu-id="dc16a-1388">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1388">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="dc16a-1389">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1389">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dc16a-1390">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1390">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="dc16a-1391">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1391">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="dc16a-1392">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-1392">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dc16a-1393">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="dc16a-1393">Highlights since the last major release</span></span>
* <span data-ttu-id="dc16a-1394">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1394">General availability of `Az` module</span></span>
* <span data-ttu-id="dc16a-1395">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="dc16a-1395">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="dc16a-1396">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="dc16a-1396">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="dc16a-1397">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1397">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="dc16a-1398">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1398">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dc16a-1399">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1399">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="dc16a-1400">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1400">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dc16a-1401">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-1401">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-1402">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1402">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dc16a-1403">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1403">Az.AnalysisServices</span></span>
* <span data-ttu-id="dc16a-1404">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="dc16a-1404">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="dc16a-1405">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="dc16a-1405">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dc16a-1406">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dc16a-1406">Az.Automation</span></span>
* <span data-ttu-id="dc16a-1407">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1407">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="dc16a-1408">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1408">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="dc16a-1409">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1409">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1410">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1410">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1411">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1411">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="dc16a-1412">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1412">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="dc16a-1413">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dc16a-1413">Az.ContainerInstance</span></span>
* <span data-ttu-id="dc16a-1414">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1414">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-1415">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-1415">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-1416">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1416">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="dc16a-1417">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1417">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-1418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1418">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1419">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1419">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="dc16a-1420">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1420">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="dc16a-1421">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1421">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="dc16a-1422">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="dc16a-1422">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="dc16a-1423">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1423">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="dc16a-1424">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="dc16a-1424">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-1425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1425">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1426">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1426">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-1427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-1427">Az.Storage</span></span>
* <span data-ttu-id="dc16a-1428">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="dc16a-1428">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="dc16a-1429">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dc16a-1429">New-AzStorageContext</span></span>
* <span data-ttu-id="dc16a-1430">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="dc16a-1430">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="dc16a-1431">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="dc16a-1431">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="dc16a-1432">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="dc16a-1432">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="dc16a-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc16a-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="dc16a-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc16a-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="dc16a-1435">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="dc16a-1435">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="dc16a-1436">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dc16a-1436">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="dc16a-1437">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dc16a-1437">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="dc16a-1438">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dc16a-1438">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="dc16a-1439">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dc16a-1439">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="dc16a-1440">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-1440">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dc16a-1441">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="dc16a-1441">Highlights since the last major release</span></span>
* <span data-ttu-id="dc16a-1442">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1442">General availability of `Az` module</span></span>
* <span data-ttu-id="dc16a-1443">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="dc16a-1443">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="dc16a-1444">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="dc16a-1444">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="dc16a-1445">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1445">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="dc16a-1446">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1446">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dc16a-1447">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1447">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="dc16a-1448">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1448">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dc16a-1449">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dc16a-1449">Az.Automation</span></span>
* <span data-ttu-id="dc16a-1450">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1450">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="dc16a-1451">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="dc16a-1451">Dynamic grouping</span></span>
    * <span data-ttu-id="dc16a-1452">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="dc16a-1452">Pre-Post script</span></span>
    * <span data-ttu-id="dc16a-1453">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="dc16a-1453">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1454">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1454">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1455">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="dc16a-1455">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="dc16a-1456">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1456">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dc16a-1457">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc16a-1457">Az.KeyVault</span></span>
* <span data-ttu-id="dc16a-1458">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1458">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-1459">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1459">Az.Network</span></span>
* <span data-ttu-id="dc16a-1460">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1460">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="dc16a-1461">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1461">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-1463">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1463">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="dc16a-1464">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1464">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1465">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1466">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1466">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="dc16a-1467">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1467">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-1468">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1468">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1469">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1469">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-1470">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-1470">Az.Storage</span></span>
* <span data-ttu-id="dc16a-1471">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="dc16a-1471">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="dc16a-1472">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dc16a-1472">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="dc16a-1473">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dc16a-1473">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="dc16a-1474">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dc16a-1474">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="dc16a-1475">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="dc16a-1475">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="dc16a-1476">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="dc16a-1476">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="dc16a-1477">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="dc16a-1477">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-1478">Az.Websites</span></span>
* <span data-ttu-id="dc16a-1479">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1479">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="dc16a-1480">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-1480">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dc16a-1481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-1481">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-1482">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1482">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="dc16a-1483">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1483">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dc16a-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dc16a-1484">Az.Automation</span></span>
* <span data-ttu-id="dc16a-1485">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1485">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="dc16a-1486">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1486">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="dc16a-1487">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="dc16a-1487">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dc16a-1488">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dc16a-1488">Az.Cdn</span></span>
* <span data-ttu-id="dc16a-1489">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-1489">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1490">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1491">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1491">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-1492">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-1492">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-1493">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1493">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dc16a-1494">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dc16a-1494">Az.LogicApp</span></span>
* <span data-ttu-id="dc16a-1495">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="dc16a-1495">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-1496">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1496">Az.Network</span></span>
* <span data-ttu-id="dc16a-1497">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1497">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-1498">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1498">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-1499">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1499">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="dc16a-1500">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1500">SDK Update</span></span>
* <span data-ttu-id="dc16a-1501">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-1501">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="dc16a-1502">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1502">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-1503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1503">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1504">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1504">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="dc16a-1505">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="dc16a-1505">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="dc16a-1506">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1506">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="dc16a-1507">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="dc16a-1507">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="dc16a-1508">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1508">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="dc16a-1509">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="dc16a-1509">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1510">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1511">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1511">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="dc16a-1512">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1512">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-1513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-1513">Az.Storage</span></span>
* <span data-ttu-id="dc16a-1514">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc16a-1514">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="dc16a-1515">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-1515">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="dc16a-1516">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1516">Az.AnalysisServices</span></span>
* <span data-ttu-id="dc16a-1517">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-1517">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dc16a-1518">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dc16a-1518">Az.Automation</span></span>
* <span data-ttu-id="dc16a-1519">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1519">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="dc16a-1520">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1520">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="dc16a-1521">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1521">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dc16a-1522">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1522">Az.CognitiveServices</span></span>
* <span data-ttu-id="dc16a-1523">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1523">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1524">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1524">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1525">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1525">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="dc16a-1526">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1526">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="dc16a-1527">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1527">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="dc16a-1528">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1528">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-1529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-1529">Az.DataLakeStore</span></span>
* <span data-ttu-id="dc16a-1530">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1530">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dc16a-1531">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-1531">Az.EventHub</span></span>
* <span data-ttu-id="dc16a-1532">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1532">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="dc16a-1533">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc16a-1533">Az.KeyVault</span></span>
* <span data-ttu-id="dc16a-1534">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1534">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dc16a-1535">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dc16a-1535">Az.LogicApp</span></span>
* <span data-ttu-id="dc16a-1536">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1536">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="dc16a-1537">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1537">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="dc16a-1538">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1538">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="dc16a-1539">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dc16a-1539">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="dc16a-1540">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dc16a-1540">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="dc16a-1541">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dc16a-1541">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="dc16a-1542">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dc16a-1542">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="dc16a-1543">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1543">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="dc16a-1544">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc16a-1544">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="dc16a-1545">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc16a-1545">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="dc16a-1546">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc16a-1546">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="dc16a-1547">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc16a-1547">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="dc16a-1548">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1548">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dc16a-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1549">Az.Monitor</span></span>
* <span data-ttu-id="dc16a-1550">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1550">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1551">Az.Network</span></span>
* <span data-ttu-id="dc16a-1552">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1552">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dc16a-1553">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-1553">Az.OperationalInsights</span></span>
* <span data-ttu-id="dc16a-1554">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1554">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="dc16a-1555">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1555">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="dc16a-1556">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1556">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="dc16a-1557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1557">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1558">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1558">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="dc16a-1559">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1559">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="dc16a-1560">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1560">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="dc16a-1561">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1561">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1562">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1563">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1563">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="dc16a-1564">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1564">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-1565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-1565">Az.Websites</span></span>
* <span data-ttu-id="dc16a-1566">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1566">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="dc16a-1567">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-1567">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dc16a-1568">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-1568">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-1569">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="dc16a-1569">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dc16a-1570">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1570">Az.AnalysisServices</span></span>
<span data-ttu-id="dc16a-1571">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1571">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1572">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1573">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1573">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="dc16a-1574">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1574">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="dc16a-1575">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1575">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1576">Az.RecoveryServices</span></span>
<span data-ttu-id="dc16a-1577">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1577">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-1578">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1578">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1579">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1579">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="dc16a-1580">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="dc16a-1580">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="dc16a-1581">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1581">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="dc16a-1582">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="dc16a-1582">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1583">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1584">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc16a-1584">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="dc16a-1585">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1585">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="dc16a-1586">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1586">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="dc16a-1587">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-1587">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dc16a-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-1588">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-1589">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="dc16a-1589">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dc16a-1590">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1590">Az.AnalysisServices</span></span>
* <span data-ttu-id="dc16a-1591">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="dc16a-1591">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="dc16a-1593">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="dc16a-1593">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="dc16a-1594">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-1594">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dc16a-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-1595">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-1596">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1596">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dc16a-1597">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1597">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dc16a-1598">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1598">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="dc16a-1599">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dc16a-1599">Az.Aks</span></span>
* <span data-ttu-id="dc16a-1600">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1600">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dc16a-1601">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dc16a-1601">Az.Automation</span></span>
* <span data-ttu-id="dc16a-1602">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1602">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="dc16a-1603">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1603">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dc16a-1604">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dc16a-1604">Az.Cdn</span></span>
* <span data-ttu-id="dc16a-1605">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1605">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1606">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1606">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1607">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1607">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="dc16a-1608">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1608">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="dc16a-1609">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1609">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="dc16a-1610">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dc16a-1610">Az.ContainerRegistry</span></span>
* <span data-ttu-id="dc16a-1611">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1611">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dc16a-1612">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dc16a-1612">Az.DataFactory</span></span>
* <span data-ttu-id="dc16a-1613">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1613">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-1614">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-1614">Az.DataLakeStore</span></span>
* <span data-ttu-id="dc16a-1615">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1615">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="dc16a-1616">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="dc16a-1616">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="dc16a-1617">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1617">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dc16a-1618">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-1618">Az.IotHub</span></span>
* <span data-ttu-id="dc16a-1619">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1619">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dc16a-1620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc16a-1620">Az.KeyVault</span></span>
* <span data-ttu-id="dc16a-1621">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1621">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-1622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1622">Az.Network</span></span>
* <span data-ttu-id="dc16a-1623">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1623">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-1624">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1624">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1625">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1625">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="dc16a-1626">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1626">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="dc16a-1627">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1627">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="dc16a-1628">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1628">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="dc16a-1629">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1629">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="dc16a-1630">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1630">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="dc16a-1631">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="dc16a-1631">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dc16a-1632">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc16a-1632">Az.ServiceFabric</span></span>
* <span data-ttu-id="dc16a-1633">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="dc16a-1633">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="dc16a-1634">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1634">Fix some error messages.</span></span>
* <span data-ttu-id="dc16a-1635">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1635">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="dc16a-1636">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1636">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dc16a-1637">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dc16a-1637">Az.SignalR</span></span>
* <span data-ttu-id="dc16a-1638">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1638">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-1639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1639">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1640">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1640">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dc16a-1641">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1641">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="dc16a-1642">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1642">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="dc16a-1643">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="dc16a-1643">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-1644">Az.Storage</span></span>
* <span data-ttu-id="dc16a-1645">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1645">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dc16a-1646">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1646">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="dc16a-1647">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="dc16a-1647">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="dc16a-1648">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="dc16a-1648">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="dc16a-1649">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="dc16a-1649">Az.TrafficManager</span></span>
* <span data-ttu-id="dc16a-1650">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1650">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-1651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-1651">Az.Websites</span></span>
* <span data-ttu-id="dc16a-1652">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dc16a-1653">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1653">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="dc16a-1654">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1654">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="dc16a-1655">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="dc16a-1655">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dc16a-1656">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-1656">Az.Accounts</span></span>
* <span data-ttu-id="dc16a-1657">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1657">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1658">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1659">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="dc16a-1659">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="dc16a-1660">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1660">Updated the description of ID in help files</span></span>
* <span data-ttu-id="dc16a-1661">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="dc16a-1661">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-1662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-1662">Az.DataLakeStore</span></span>
* <span data-ttu-id="dc16a-1663">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1663">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="dc16a-1664">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1664">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dc16a-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dc16a-1665">Az.EventGrid</span></span>
* <span data-ttu-id="dc16a-1666">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1666">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="dc16a-1667">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1667">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="dc16a-1668">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1668">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="dc16a-1669">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="dc16a-1669">Event Time-To-Live,</span></span>
        - <span data-ttu-id="dc16a-1670">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="dc16a-1670">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="dc16a-1671">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1671">Dead letter endpoint.</span></span>
    - <span data-ttu-id="dc16a-1672">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1672">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="dc16a-1673">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="dc16a-1673">Event Time-To-Live,</span></span>
        - <span data-ttu-id="dc16a-1674">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="dc16a-1674">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="dc16a-1675">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1675">Dead letter endpoint.</span></span>
* <span data-ttu-id="dc16a-1676">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1676">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="dc16a-1677">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1677">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dc16a-1678">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dc16a-1678">Az.IotHub</span></span>
* <span data-ttu-id="dc16a-1679">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1679">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dc16a-1680">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dc16a-1680">Az.LogicApp</span></span>
* <span data-ttu-id="dc16a-1681">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1681">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1682">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1683">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1683">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="dc16a-1684">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="dc16a-1684">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="dc16a-1685">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1685">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="dc16a-1686">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1686">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="dc16a-1687">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1687">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="dc16a-1688">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="dc16a-1688">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dc16a-1689">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dc16a-1689">Az.SignalR</span></span>
* <span data-ttu-id="dc16a-1690">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="dc16a-1690">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-1691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1691">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1692">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1692">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dc16a-1693">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-1693">Az.Storage</span></span>
* <span data-ttu-id="dc16a-1694">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1694">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="dc16a-1695">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dc16a-1695">New-AzStorageContext</span></span>
* <span data-ttu-id="dc16a-1696">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1696">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="dc16a-1697">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="dc16a-1697">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-1698">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-1698">Az.Websites</span></span>
* <span data-ttu-id="dc16a-1699">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1699">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="dc16a-1700">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="dc16a-1700">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="dc16a-1701">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="dc16a-1701">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="dc16a-1702">Genel</span><span class="sxs-lookup"><span data-stu-id="dc16a-1702">General</span></span>

- <span data-ttu-id="dc16a-1703">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1703">General Availability of Az Module</span></span>
- <span data-ttu-id="dc16a-1704">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="dc16a-1704">Online help for each module</span></span>
- <span data-ttu-id="dc16a-1705">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1705">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="dc16a-1706">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1706">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="dc16a-1707">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dc16a-1707">Az.Accounts</span></span>
- <span data-ttu-id="dc16a-1708">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dc16a-1708">Changed from Az.Profile</span></span>
- <span data-ttu-id="dc16a-1709">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1709">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="dc16a-1710">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc16a-1710">Az.ApiManagement</span></span>
- <span data-ttu-id="dc16a-1711">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="dc16a-1711">Fixes for #7002</span></span>
- <span data-ttu-id="dc16a-1712">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1712">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="dc16a-1713">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dc16a-1713">Az.Batch</span></span>
- <span data-ttu-id="dc16a-1714">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1714">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="dc16a-1715">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1715">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="dc16a-1716">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="dc16a-1717">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="dc16a-1717">Az.Billing</span></span>
- <span data-ttu-id="dc16a-1718">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1718">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="dc16a-1719">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1719">Az.CognitivServices</span></span>
- <span data-ttu-id="dc16a-1720">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1720">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="dc16a-1721">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-1721">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="dc16a-1722">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dc16a-1722">Az.ContainerInstance</span></span>
- <span data-ttu-id="dc16a-1723">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1723">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="dc16a-1724">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="dc16a-1724">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="dc16a-1725">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1725">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-1726">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-1726">Az.DataLakeStore</span></span>
- <span data-ttu-id="dc16a-1727">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1727">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="dc16a-1728">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1728">Az.Monitor</span></span>
- <span data-ttu-id="dc16a-1729">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1729">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="dc16a-1730">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dc16a-1730">Az.KeyVault</span></span>
- <span data-ttu-id="dc16a-1731">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-1731">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="dc16a-1732">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="dc16a-1732">Az.MachineLearning</span></span>
- <span data-ttu-id="dc16a-1733">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1733">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="dc16a-1734">Az.Media</span><span class="sxs-lookup"><span data-stu-id="dc16a-1734">Az.Media</span></span>
- <span data-ttu-id="dc16a-1735">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="dc16a-1735">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="dc16a-1736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1736">Az.Network</span></span>
<span data-ttu-id="dc16a-1737">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1737">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="dc16a-1738">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="dc16a-1738">New cmdlets added:</span></span>
        - <span data-ttu-id="dc16a-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc16a-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dc16a-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc16a-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dc16a-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc16a-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dc16a-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc16a-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dc16a-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc16a-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dc16a-1744">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="dc16a-1744">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="dc16a-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="dc16a-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="dc16a-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc16a-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="dc16a-1747">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1747">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="dc16a-1748">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc16a-1748">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="dc16a-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dc16a-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="dc16a-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dc16a-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="dc16a-1751">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-1751">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="dc16a-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="dc16a-1753">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1753">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="dc16a-1754">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1754">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="dc16a-1755">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dc16a-1755">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="dc16a-1756">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dc16a-1756">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="dc16a-1757">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dc16a-1757">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="dc16a-1758">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1758">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="dc16a-1759">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1759">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="dc16a-1760">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-1760">Az.OperationalInsights</span></span>
- <span data-ttu-id="dc16a-1761">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1761">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="dc16a-1762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dc16a-1762">Az.Profile</span></span>
- <span data-ttu-id="dc16a-1763">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1763">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-1764">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1764">Az.RecoveryServices</span></span>
- <span data-ttu-id="dc16a-1765">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1765">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="dc16a-1766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1766">Az.Resources</span></span>
- <span data-ttu-id="dc16a-1767">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="dc16a-1768">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc16a-1768">Az.ServiceFabric</span></span>
- <span data-ttu-id="dc16a-1769">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="dc16a-1769">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="dc16a-1770">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1770">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="dc16a-1771">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="dc16a-1771">Az.SIgnalR</span></span>
- <span data-ttu-id="dc16a-1772">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1772">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="dc16a-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1773">Az.Sql</span></span>
- <span data-ttu-id="dc16a-1774">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1774">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="dc16a-1775">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1775">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="dc16a-1776">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1776">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="dc16a-1777">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-1777">Az.Storage</span></span>
- <span data-ttu-id="dc16a-1778">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1778">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="dc16a-1779">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-1779">Az.Websites</span></span>
- <span data-ttu-id="dc16a-1780">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="dc16a-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="dc16a-1781">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="dc16a-1781">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="dc16a-1782">Genel</span><span class="sxs-lookup"><span data-stu-id="dc16a-1782">General</span></span>

* <span data-ttu-id="dc16a-1783">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1783">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="dc16a-1784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1784">Az.Compute</span></span>

* <span data-ttu-id="dc16a-1785">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1785">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-1786">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-1786">Az.DataLakeStore</span></span>

* <span data-ttu-id="dc16a-1787">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1787">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="dc16a-1788">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1788">Az.FrontDoor</span></span>

* <span data-ttu-id="dc16a-1789">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1789">Fixed some broken links</span></span>
    - <span data-ttu-id="dc16a-1790">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1790">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="dc16a-1791">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1791">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="dc16a-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1792">Az.RecoveryServices</span></span>

* <span data-ttu-id="dc16a-1793">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1793">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="dc16a-1794">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1794">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="dc16a-1795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1795">Az.Resources</span></span>

* <span data-ttu-id="dc16a-1796">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1796">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="dc16a-1797">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1797">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="dc16a-1798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1798">Az.Sql</span></span>

* <span data-ttu-id="dc16a-1799">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="dc16a-1799">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="dc16a-1800">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1800">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="dc16a-1801">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1801">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="dc16a-1802">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dc16a-1802">Az.Storage</span></span>

* <span data-ttu-id="dc16a-1803">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1803">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="dc16a-1804">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1804">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="dc16a-1805">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="dc16a-1805">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="dc16a-1806">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1806">Support Static Website configuration</span></span>
    - <span data-ttu-id="dc16a-1807">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="dc16a-1807">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="dc16a-1808">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="dc16a-1808">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="dc16a-1809">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-1809">Az.Websites</span></span>

* <span data-ttu-id="dc16a-1810">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc16a-1810">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="dc16a-1811">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1811">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="dc16a-1812">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1812">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="dc16a-1813">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="dc16a-1813">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="dc16a-1814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc16a-1814">Az.ApiManagement</span></span>
* <span data-ttu-id="dc16a-1815">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1815">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="dc16a-1816">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dc16a-1816">Az.Automation</span></span>
* <span data-ttu-id="dc16a-1817">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="dc16a-1817">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="dc16a-1818">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1818">Added Update Management cmdlets</span></span>
* <span data-ttu-id="dc16a-1819">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1819">Added Source Control cmdlets</span></span>
* <span data-ttu-id="dc16a-1820">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1820">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="dc16a-1821">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1821">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="dc16a-1822">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1822">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1823">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1823">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="dc16a-1824">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1824">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="dc16a-1825">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dc16a-1825">Az.ContainerInstance</span></span>
* <span data-ttu-id="dc16a-1826">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1826">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="dc16a-1827">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="dc16a-1827">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="dc16a-1828">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1828">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="dc16a-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1829">Az.Network</span></span>
* <span data-ttu-id="dc16a-1830">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1830">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="dc16a-1831">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1831">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="dc16a-1832">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1832">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="dc16a-1833">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1833">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="dc16a-1834">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="dc16a-1834">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="dc16a-1835">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1835">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="dc16a-1836">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1836">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="dc16a-1837">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="dc16a-1837">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="dc16a-1838">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1838">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="dc16a-1839">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="dc16a-1839">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="dc16a-1840">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="dc16a-1840">Az.Relay</span></span>
* <span data-ttu-id="dc16a-1841">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1841">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="dc16a-1842">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1842">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1843">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1843">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="dc16a-1844">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1844">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="dc16a-1845">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="dc16a-1845">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="dc16a-1846">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc16a-1846">Az.ServiceFabric</span></span>
* <span data-ttu-id="dc16a-1847">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1847">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="dc16a-1848">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1848">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1849">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1849">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="dc16a-1850">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dc16a-1850">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dc16a-1851">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dc16a-1851">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dc16a-1852">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dc16a-1852">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dc16a-1853">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dc16a-1853">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dc16a-1854">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dc16a-1854">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="dc16a-1855">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dc16a-1855">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="dc16a-1856">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dc16a-1856">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="dc16a-1857">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dc16a-1857">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="dc16a-1858">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1858">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="dc16a-1859">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1859">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="dc16a-1860">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1860">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="dc16a-1861">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1861">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="dc16a-1862">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1862">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="dc16a-1863">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1863">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="dc16a-1864">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1864">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="dc16a-1865">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1865">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="dc16a-1866">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="dc16a-1866">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="dc16a-1867">Genel</span><span class="sxs-lookup"><span data-stu-id="dc16a-1867">General</span></span>
* <span data-ttu-id="dc16a-1868">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="dc16a-1868">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="dc16a-1869">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dc16a-1869">Az.Profile</span></span>
* <span data-ttu-id="dc16a-1870">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1870">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="dc16a-1871">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1871">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="dc16a-1872">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1872">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="dc16a-1873">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1873">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="dc16a-1874">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1874">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="dc16a-1875">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1875">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="dc16a-1876">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1876">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="dc16a-1877">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1877">Az.CognitiveServices</span></span>
* <span data-ttu-id="dc16a-1878">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1878">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1879">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1879">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1880">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1880">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="dc16a-1881">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1881">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="dc16a-1882">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1882">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-1883">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-1883">Az.DataLakeStore</span></span>
* <span data-ttu-id="dc16a-1884">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1884">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="dc16a-1885">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1885">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="dc16a-1886">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="dc16a-1886">Az.Insights</span></span>
* <span data-ttu-id="dc16a-1887">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1887">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="dc16a-1888">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="dc16a-1888">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="dc16a-1889">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1889">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="dc16a-1890">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1890">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-1891">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1891">Az.Network</span></span>
* <span data-ttu-id="dc16a-1892">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="dc16a-1892">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="dc16a-1893">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc16a-1893">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="dc16a-1894">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="dc16a-1894">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="dc16a-1895">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dc16a-1895">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="dc16a-1896">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="dc16a-1896">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="dc16a-1897">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc16a-1897">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="dc16a-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dc16a-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dc16a-1899">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dc16a-1899">Az.PolicyInsights</span></span>
* <span data-ttu-id="dc16a-1900">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1900">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-1901">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1901">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1902">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1902">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="dc16a-1903">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="dc16a-1903">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dc16a-1904">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dc16a-1904">Az.ServiceBus</span></span>
* <span data-ttu-id="dc16a-1905">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1905">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dc16a-1906">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dc16a-1906">Az.ServiceFabric</span></span>
* <span data-ttu-id="dc16a-1907">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1907">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="dc16a-1908">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1908">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="dc16a-1909">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="dc16a-1909">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="dc16a-1910">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="dc16a-1910">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="dc16a-1911">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1911">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="dc16a-1912">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="dc16a-1912">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="dc16a-1913">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dc16a-1913">Az.Profile</span></span>
* <span data-ttu-id="dc16a-1914">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="dc16a-1914">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="dc16a-1915">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1915">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1916">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1916">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1917">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1917">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="dc16a-1918">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1918">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dc16a-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc16a-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="dc16a-1920">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="dc16a-1920">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="dc16a-1921">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1921">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="dc16a-1922">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1922">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="dc16a-1923">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1923">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="dc16a-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1925">Az.Network</span></span>
* <span data-ttu-id="dc16a-1926">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1926">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="dc16a-1927">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1927">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-1928">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1928">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1929">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1929">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="dc16a-1930">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1930">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="dc16a-1931">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="dc16a-1931">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="dc16a-1932">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="dc16a-1932">Azure.Storage</span></span>
* <span data-ttu-id="dc16a-1933">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="dc16a-1933">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="dc16a-1934">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dc16a-1934">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="dc16a-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="dc16a-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="dc16a-1936">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1936">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="dc16a-1937">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="dc16a-1937">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="dc16a-1938">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dc16a-1938">Az.CognitiveServices</span></span>
* <span data-ttu-id="dc16a-1939">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1939">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dc16a-1940">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dc16a-1940">Az.Compute</span></span>
* <span data-ttu-id="dc16a-1941">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1941">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="dc16a-1942">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1942">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="dc16a-1943">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1943">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="dc16a-1944">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dc16a-1944">Az.DataFactoryV2</span></span>
* <span data-ttu-id="dc16a-1945">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1945">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dc16a-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dc16a-1946">Az.Network</span></span>
* <span data-ttu-id="dc16a-1947">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1947">Added NetworkProfile functionality.</span></span> <span data-ttu-id="dc16a-1948">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1948">new cmdlets added</span></span>
    - <span data-ttu-id="dc16a-1949">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dc16a-1949">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="dc16a-1950">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dc16a-1950">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="dc16a-1951">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dc16a-1951">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="dc16a-1952">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dc16a-1952">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="dc16a-1953">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-1953">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="dc16a-1954">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="dc16a-1954">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="dc16a-1955">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1955">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="dc16a-1956">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1956">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="dc16a-1957">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1957">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dc16a-1958">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dc16a-1958">Az.RedisCache</span></span>
* <span data-ttu-id="dc16a-1959">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="dc16a-1959">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="dc16a-1960">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1960">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="dc16a-1961">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dc16a-1961">Az.Resources</span></span>
* <span data-ttu-id="dc16a-1962">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1962">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="dc16a-1963">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1963">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="dc16a-1964">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dc16a-1964">Az.Sql</span></span>
* <span data-ttu-id="dc16a-1965">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="dc16a-1965">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dc16a-1966">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dc16a-1966">Az.Websites</span></span>
* <span data-ttu-id="dc16a-1967">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1967">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="dc16a-1968">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="dc16a-1968">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="dc16a-1969">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="dc16a-1969">0.2.0 - September 2018</span></span>
 <span data-ttu-id="dc16a-1970">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="dc16a-1970">Initial Release</span></span>
