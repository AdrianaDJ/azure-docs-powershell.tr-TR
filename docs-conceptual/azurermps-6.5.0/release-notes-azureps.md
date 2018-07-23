---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: e9fa2d75c1c4e6ffaa2f7dd8e400f5b13dd4527d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110492"
---
# <a name="release-notes"></a><span data-ttu-id="46f2e-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="46f2e-103">Release notes</span></span>

<span data-ttu-id="46f2e-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="46f2e-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="650---july-2018"></a><span data-ttu-id="46f2e-105">6.5.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="46f2e-105">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="46f2e-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46f2e-106">AzureRM.Profile</span></span>
* <span data-ttu-id="46f2e-107">'Get-AzureRmContextAutosaveSetting' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-107">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="46f2e-108">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="46f2e-108">Azure.Storage</span></span>
* <span data-ttu-id="46f2e-109">Salt yazılır Sas belirteciyle Karşıya Yükleme Blobu veya Dosyası desteği</span><span class="sxs-lookup"><span data-stu-id="46f2e-109">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="46f2e-110">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46f2e-110">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="46f2e-111">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46f2e-111">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="46f2e-112">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46f2e-112">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="46f2e-113">AS'ye gerekli ResourceGroupName özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-113">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="46f2e-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="46f2e-114">AzureRM.Automation</span></span>
* <span data-ttu-id="46f2e-115">'New-AzureRMAutomationSchedule' için yardım güncelleştirildi ve örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-115">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46f2e-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46f2e-116">AzureRM.Compute</span></span>
* <span data-ttu-id="46f2e-117">Update/New-AzureRmAvailabilitySet komutlarına -Tag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-117">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="46f2e-118">'Add-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-118">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="46f2e-119">'Remove-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-119">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="46f2e-120">'Set-AzureRmVMAccessExtension' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-120">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="46f2e-121">New-AzureRmVmss için SimpleParameterSet güncelleştirilerek SinglePlacementGroup varsayılan olarak false değerine ayarlandı ve kullanıcının tek yerleşim grubunda VMSS oluşturmasına olanak tanıyan 'SinglePlacementGroup' geçiş parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-121">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="46f2e-122">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="46f2e-122">AzureRM.EventHub</span></span>
* <span data-ttu-id="46f2e-123">PSEventHubDRConfigurationAttributes sınıfına, çoğaltma işlemi devam ederken bekleyen çoğaltma işlemlerinin sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-123">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="46f2e-124">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46f2e-124">AzureRM.KeyVault</span></span>
* <span data-ttu-id="46f2e-125">Set-AzureRmKeyVaultAccessPolicy için hata iletisi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-125">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="46f2e-126">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46f2e-126">AzureRM.LogicApp</span></span>
* <span data-ttu-id="46f2e-127">New-AzureRmLogicApp’te "parametre kümesi çözümlenemedi" hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-127">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46f2e-128">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46f2e-128">AzureRM.Network</span></span>
* <span data-ttu-id="46f2e-129">Set/Add-AzureRmVirtualNetworkPeering için birden çok Kiracıdaki Sanal Makineler arasında eşleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-129">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="46f2e-130">Aşağıdaki cmdlet’ler Application Gateway için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-130">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="46f2e-131">New-AzureRmApplicationGateway : EnableFIPS bayrağı ve Zones desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-131">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="46f2e-132">New-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-132">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="46f2e-133">Set-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-133">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="46f2e-134">RouteTable cmdlet’leri en son oluşturucu sürümüyle yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="46f2e-134">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="46f2e-135">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="46f2e-135">AzureRM.Relay</span></span>
* <span data-ttu-id="46f2e-136">Markdown dosyaları güncelleştirildi, örnekteki parametre adı sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="46f2e-136">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46f2e-137">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46f2e-137">AzureRM.Resources</span></span>
* <span data-ttu-id="46f2e-138">Roleassignment ve roledefinition cmdlet’leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46f2e-138">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="46f2e-139">Disk belleğinin parçası olarak yapılan ek roledefinition çağrıları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46f2e-139">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="46f2e-140">Get-AzureRmRoleAssignment cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-140">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="46f2e-141">-ExpandPrincipalGroups komut parametresi işlevselliği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-141">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="46f2e-142">'-ResourceType' parametresinin büyük/küçük harfe duyarlı olduğu 'Get-AzureRmResource' sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-142">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="46f2e-143">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46f2e-143">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="46f2e-144">Liste cmdlet’lerine top ve skip parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-144">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="46f2e-145">Standard'dan Premium NameSpace'e geçiş cmdlet’leri eklendi :</span><span class="sxs-lookup"><span data-stu-id="46f2e-145">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="46f2e-146">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="46f2e-146">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="46f2e-147">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="46f2e-147">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="46f2e-148">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="46f2e-148">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="46f2e-149">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="46f2e-149">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="46f2e-150">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="46f2e-150">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="46f2e-151">PSServiceBusDRConfigurationAttributes sınıfına, çoğaltma işlemi sürerken beklemede olan çoğaltma işlemi sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-151">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="46f2e-152">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46f2e-152">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="46f2e-153">'New-AzureRmServiceFabricCluster' için örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-153">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="46f2e-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46f2e-154">AzureRM.Sql</span></span>
* <span data-ttu-id="46f2e-155">Müşterilerin Sql Server örneğine veya Yönetilen Örneğe TDE Sertifikası ekleyebilmeleri için yeni Management.Sql Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-155">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="46f2e-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="46f2e-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="46f2e-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="46f2e-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="46f2e-158">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="46f2e-158">AzureRM.Websites</span></span>
* <span data-ttu-id="46f2e-159">Artık `Set-AzureRmWebApp -AssignIdentity` ve `Set-AzureRmWebAppSlot -AssignIdentity` false olarak ayarlandığında site object.Removing önizleme etiketinden Identity özelliğini kaldırıyor.</span><span class="sxs-lookup"><span data-stu-id="46f2e-159">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="46f2e-160">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-160">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="46f2e-161">`Set-AzureRmWebApp -PhpVersion` geçerli bir php sürümü off değerini destekliyor</span><span class="sxs-lookup"><span data-stu-id="46f2e-161">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="46f2e-162">6.4.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="46f2e-162">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="46f2e-163">Genel</span><span class="sxs-lookup"><span data-stu-id="46f2e-163">General</span></span>
* <span data-ttu-id="46f2e-164">Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-164">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="46f2e-165">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46f2e-165">AzureRM.Profile</span></span>
* <span data-ttu-id="46f2e-166">Temel çıkış türlerine Ps1Xml özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-166">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46f2e-167">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46f2e-167">AzureRM.Compute</span></span>
* <span data-ttu-id="46f2e-168">VMSS için IP Etiketi özelliği</span><span class="sxs-lookup"><span data-stu-id="46f2e-168">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="46f2e-169">'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-169">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="46f2e-170">New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-170">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="46f2e-171">VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-171">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="46f2e-172">New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-172">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="46f2e-173">VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği</span><span class="sxs-lookup"><span data-stu-id="46f2e-173">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="46f2e-174">Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-174">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="46f2e-175">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="46f2e-175">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="46f2e-176">Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:</span><span class="sxs-lookup"><span data-stu-id="46f2e-176">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="46f2e-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="46f2e-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="46f2e-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="46f2e-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="46f2e-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="46f2e-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="46f2e-180">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46f2e-180">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="46f2e-181">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-181">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="46f2e-182">Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-182">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="46f2e-183">Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-183">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="46f2e-184">DataLake cmdlet'lerinin test konumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-184">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="46f2e-185">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="46f2e-185">AzureRM.EventHub</span></span>
* <span data-ttu-id="46f2e-186">Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-186">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="46f2e-187">New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-187">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="46f2e-188">Varsayılan Parametre kümesi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="46f2e-188">Provided Default Parameter set.</span></span>
* <span data-ttu-id="46f2e-189">Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-189">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="46f2e-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46f2e-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="46f2e-191">Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-191">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="46f2e-192">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46f2e-192">AzureRM.Network</span></span>
* <span data-ttu-id="46f2e-193">Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46f2e-193">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="46f2e-194">ARM aracılığıyla ExpressRoute Partner API'leri özelliği için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-194">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="46f2e-195">Get-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-195">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="46f2e-196">Set-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-196">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="46f2e-197">Add-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-197">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="46f2e-198">Get-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-198">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="46f2e-199">Remove-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-199">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="46f2e-200">Get-AzureRMExpressRouteCrossConnectionArpTable eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-200">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="46f2e-201">Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-201">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="46f2e-202">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-202">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="46f2e-203">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="46f2e-203">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="46f2e-204">Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-204">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="46f2e-205">Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="46f2e-205">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="46f2e-206">Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46f2e-206">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46f2e-207">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46f2e-207">AzureRM.Resources</span></span>
* <span data-ttu-id="46f2e-208">Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46f2e-208">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="46f2e-209">Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-209">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="46f2e-210">Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-210">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="46f2e-211">control parametresine -Effective ve -All anahtarları eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-211">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="46f2e-212">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-212">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="46f2e-213">Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-213">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="46f2e-214">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-214">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="46f2e-215">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-215">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="46f2e-216">Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-216">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="46f2e-217">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-217">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="46f2e-218">'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-218">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="46f2e-219">'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-219">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="46f2e-220">'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-220">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="46f2e-221">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46f2e-221">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="46f2e-222">Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-222">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="46f2e-223">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46f2e-223">AzureRM.Sql</span></span>
* <span data-ttu-id="46f2e-224">New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-224">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="46f2e-225">Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-225">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="46f2e-226">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="46f2e-226">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="46f2e-227">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46f2e-227">AzureRM.Profile</span></span>
* <span data-ttu-id="46f2e-228">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-228">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="46f2e-229">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="46f2e-229">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="46f2e-230">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="46f2e-230">Azure.Storage</span></span>
* <span data-ttu-id="46f2e-231">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-231">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46f2e-232">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46f2e-232">AzureRM.Compute</span></span>
* <span data-ttu-id="46f2e-233">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-233">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="46f2e-234">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-234">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="46f2e-235">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="46f2e-235">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="46f2e-236">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="46f2e-236">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="46f2e-237">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="46f2e-237">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="46f2e-238">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="46f2e-238">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="46f2e-239">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="46f2e-239">Start-AzureRmVM</span></span>
    - <span data-ttu-id="46f2e-240">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="46f2e-240">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="46f2e-241">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="46f2e-241">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="46f2e-242">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="46f2e-242">Set-AzureRmVM</span></span>
    - <span data-ttu-id="46f2e-243">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="46f2e-243">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="46f2e-244">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f2e-244">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="46f2e-245">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="46f2e-245">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="46f2e-246">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="46f2e-246">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="46f2e-247">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f2e-247">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="46f2e-248">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f2e-248">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="46f2e-249">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f2e-249">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="46f2e-250">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46f2e-250">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="46f2e-251">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="46f2e-251">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="46f2e-252">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="46f2e-252">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="46f2e-253">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="46f2e-253">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="46f2e-254">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="46f2e-254">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="46f2e-255">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="46f2e-255">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="46f2e-256">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="46f2e-256">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="46f2e-257">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="46f2e-257">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="46f2e-258">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46f2e-258">AzureRM.EventGrid</span></span>
* <span data-ttu-id="46f2e-259">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46f2e-259">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="46f2e-260">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46f2e-260">AzureRM.KeyVault</span></span>
* <span data-ttu-id="46f2e-261">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-261">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="46f2e-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46f2e-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="46f2e-263">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46f2e-263">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="46f2e-264">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="46f2e-264">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="46f2e-265">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-265">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="46f2e-266">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="46f2e-266">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="46f2e-267">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-267">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="46f2e-268">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="46f2e-268">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="46f2e-269">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46f2e-269">AzureRM.Sql</span></span>
* <span data-ttu-id="46f2e-270">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-270">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="46f2e-271">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="46f2e-271">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="46f2e-272">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-272">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="46f2e-273">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="46f2e-273">AzureRM.Websites</span></span>
* <span data-ttu-id="46f2e-274">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-274">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="46f2e-275">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-275">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="46f2e-276">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="46f2e-276">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="46f2e-277">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46f2e-277">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="46f2e-278">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-278">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="46f2e-279">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="46f2e-279">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="46f2e-280">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46f2e-280">AzureRM.Profile</span></span>
* <span data-ttu-id="46f2e-281">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-281">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="46f2e-282">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="46f2e-282">AzureRM.Compute</span></span>
* <span data-ttu-id="46f2e-283">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="46f2e-283">VMSS VM Update feature</span></span>
    - <span data-ttu-id="46f2e-284">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-284">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="46f2e-285">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-285">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="46f2e-286">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="46f2e-286">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="46f2e-287">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46f2e-287">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="46f2e-288">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-288">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="46f2e-289">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-289">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="46f2e-290">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-290">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="46f2e-291">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-291">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="46f2e-292">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46f2e-292">AzureRM.KeyVault</span></span>
* <span data-ttu-id="46f2e-293">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-293">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="46f2e-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46f2e-294">AzureRM.Network</span></span>
* <span data-ttu-id="46f2e-295">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-295">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="46f2e-296">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="46f2e-296">AzureRM.Resources</span></span>
* <span data-ttu-id="46f2e-297">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-297">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="46f2e-298">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="46f2e-298">AzureRM.Scheduler</span></span>
* <span data-ttu-id="46f2e-299">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-299">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="46f2e-300">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46f2e-300">AzureRM.Sql</span></span>
* <span data-ttu-id="46f2e-301">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46f2e-301">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="46f2e-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46f2e-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="46f2e-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46f2e-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="46f2e-304">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="46f2e-304">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="46f2e-305">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="46f2e-305">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="46f2e-306">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46f2e-306">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="46f2e-307">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="46f2e-307">AzureRM.Websites</span></span>
* <span data-ttu-id="46f2e-308">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-308">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="46f2e-309">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="46f2e-309">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="46f2e-310">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="46f2e-310">AzureRM.Profile</span></span>
* <span data-ttu-id="46f2e-311">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-311">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="46f2e-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46f2e-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="46f2e-313">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="46f2e-313">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="46f2e-314">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46f2e-314">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="46f2e-315">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-315">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="46f2e-316">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-316">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="46f2e-317">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-317">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="46f2e-318">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-318">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="46f2e-319">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-319">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="46f2e-320">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-320">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="46f2e-321">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-321">Added support for MSI identity</span></span>
* <span data-ttu-id="46f2e-322">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="46f2e-322">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="46f2e-323">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="46f2e-323">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="46f2e-324">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="46f2e-324">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="46f2e-325">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="46f2e-325">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="46f2e-326">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="46f2e-326">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="46f2e-327">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="46f2e-327">AzureRM.Batch</span></span>
* <span data-ttu-id="46f2e-328">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="46f2e-328">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="46f2e-329">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="46f2e-329">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="46f2e-330">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="46f2e-330">AzureRM.Consumption</span></span>
* <span data-ttu-id="46f2e-331">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="46f2e-331">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="46f2e-332">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46f2e-332">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="46f2e-333">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="46f2e-333">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="46f2e-334">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="46f2e-334">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="46f2e-335">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="46f2e-335">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="46f2e-336">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="46f2e-336">AzureRM.Network</span></span>
* <span data-ttu-id="46f2e-337">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="46f2e-337">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="46f2e-338">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-338">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="46f2e-339">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="46f2e-339">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="46f2e-340">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-340">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="46f2e-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="46f2e-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="46f2e-342">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-342">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="46f2e-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="46f2e-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="46f2e-344">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46f2e-344">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="46f2e-345">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="46f2e-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="46f2e-346">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46f2e-346">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="46f2e-347">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="46f2e-347">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="46f2e-348">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="46f2e-348">AzureRM.Sql</span></span>
* <span data-ttu-id="46f2e-349">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46f2e-349">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="46f2e-350">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46f2e-350">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="46f2e-351">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-351">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="46f2e-352">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="46f2e-352">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="46f2e-353">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="46f2e-353">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="46f2e-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46f2e-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="46f2e-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46f2e-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="46f2e-356">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="46f2e-356">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="46f2e-357">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="46f2e-357">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="46f2e-358">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46f2e-358">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="46f2e-359">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="46f2e-359">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="46f2e-360">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="46f2e-360">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>