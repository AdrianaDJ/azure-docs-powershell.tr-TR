---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: bee24af99da4b36e89cff9852c77214e2e09a542
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740550"
---
## <a name="380---april-2020"></a><span data-ttu-id="08d27-103">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="08d27-103">3.8.0 - April 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-104">Az.Accounts</span></span>
* <span data-ttu-id="08d27-105">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="08d27-105">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08d27-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08d27-106">Az.ApiManagement</span></span>
* <span data-ttu-id="08d27-107">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-107">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="08d27-108">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-108">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08d27-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08d27-109">Az.Cdn</span></span>
* <span data-ttu-id="08d27-110">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-110">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08d27-111">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d27-111">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d27-112">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="08d27-112">Supported Identity, Encryption, UserOwnedStorage</span></span> 

#### <a name="azcompute"></a><span data-ttu-id="08d27-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-113">Az.Compute</span></span>
* <span data-ttu-id="08d27-114">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-114">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="08d27-115">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-115">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d27-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d27-116">Az.IotHub</span></span>
* <span data-ttu-id="08d27-117">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="08d27-117">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="08d27-118">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="08d27-118">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="08d27-119">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="08d27-119">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="08d27-120">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-120">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="08d27-121">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="08d27-121">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="08d27-122">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="08d27-122">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="08d27-123">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="08d27-123">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="08d27-124">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="08d27-124">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="08d27-125">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="08d27-125">New cmdlets are:</span></span>
    - <span data-ttu-id="08d27-126">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="08d27-126">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="08d27-127">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="08d27-127">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="08d27-128">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="08d27-128">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="08d27-129">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="08d27-129">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="08d27-130">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-130">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d27-131">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d27-131">Az.KeyVault</span></span>
* <span data-ttu-id="08d27-132">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-132">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="08d27-133">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="08d27-133">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="08d27-134">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="08d27-134">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="08d27-135">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-135">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="08d27-136">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="08d27-136">Az.Maintenance</span></span>
* <span data-ttu-id="08d27-137">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="08d27-137">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d27-138">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-138">Az.Monitor</span></span>
* <span data-ttu-id="08d27-139">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-139">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="08d27-140">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="08d27-140">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="08d27-141">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="08d27-141">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="08d27-142">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="08d27-142">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="08d27-143">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="08d27-143">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="08d27-144">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="08d27-144">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="08d27-145">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="08d27-145">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="08d27-146">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="08d27-146">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-147">Az.Network</span></span>
* <span data-ttu-id="08d27-148">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-148">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="08d27-149">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="08d27-149">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="08d27-150">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="08d27-150">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="08d27-151">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="08d27-151">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="08d27-152">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="08d27-152">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="08d27-153">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-153">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="08d27-154">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="08d27-154">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="08d27-155">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="08d27-155">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="08d27-156">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-156">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="08d27-157">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-157">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="08d27-158">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="08d27-158">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="08d27-159">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-159">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="08d27-160">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-160">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="08d27-161">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-161">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="08d27-162">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-162">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="08d27-163">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-163">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08d27-164">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-164">Az.PolicyInsights</span></span>
* <span data-ttu-id="08d27-165">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-165">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="08d27-166">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-166">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08d27-167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d27-167">Az.ServiceFabric</span></span>
* <span data-ttu-id="08d27-168">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-168">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-169">Az.Sql</span></span>
* <span data-ttu-id="08d27-170">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-170">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="08d27-171">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-171">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-172">Az.Storage</span></span>
* <span data-ttu-id="08d27-173">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-173">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="08d27-174">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-174">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="08d27-175">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="08d27-175">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="08d27-176">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="08d27-176">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="08d27-177">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-177">Supported DataLake Gen2</span></span> 
    - <span data-ttu-id="08d27-178">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="08d27-178">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="08d27-179">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="08d27-179">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="08d27-180">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="08d27-180">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="08d27-181">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="08d27-181">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="08d27-182">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="08d27-182">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="08d27-183">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="08d27-183">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="08d27-184">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="08d27-184">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="08d27-185">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="08d27-185">'Remove-AzDataLakeGen2Item'</span></span>

# <a name="azure-powershell-release-notes"></a><span data-ttu-id="08d27-186">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="08d27-186">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="08d27-187">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="08d27-187">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-188">Az.Accounts</span></span>
* <span data-ttu-id="08d27-189">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="08d27-189">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-190">Az.Compute</span></span>
* <span data-ttu-id="08d27-191">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-191">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="08d27-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="08d27-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="08d27-193">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-193">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="08d27-194">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-194">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="08d27-195">[#11354]</span><span class="sxs-lookup"><span data-stu-id="08d27-195">[#11354]</span></span>
* <span data-ttu-id="08d27-196">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-196">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="08d27-197">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="08d27-197">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="08d27-198">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="08d27-198">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="08d27-199">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="08d27-199">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="08d27-200">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="08d27-200">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="08d27-201">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-201">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="08d27-202">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-202">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="08d27-203">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-203">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="08d27-204">[#11257]</span><span class="sxs-lookup"><span data-stu-id="08d27-204">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-205">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-206">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-206">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="08d27-207">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-207">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-208">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-209">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-209">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="08d27-210">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-210">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08d27-211">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08d27-211">Az.HDInsight</span></span>
* <span data-ttu-id="08d27-212">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-212">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d27-213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d27-213">Az.IotHub</span></span>
* <span data-ttu-id="08d27-214">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-214">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="08d27-215">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="08d27-215">New Cmdlets are:</span></span>
    - <span data-ttu-id="08d27-216">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="08d27-216">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="08d27-217">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="08d27-217">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d27-218">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d27-218">Az.KeyVault</span></span>
* <span data-ttu-id="08d27-219">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-219">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d27-220">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-220">Az.Monitor</span></span>
* <span data-ttu-id="08d27-221">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-221">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-222">Az.Network</span></span>
* <span data-ttu-id="08d27-223">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-223">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="08d27-224">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="08d27-224">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="08d27-225">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="08d27-225">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="08d27-226">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="08d27-226">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="08d27-227">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="08d27-227">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="08d27-228">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-228">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08d27-229">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-229">Az.PolicyInsights</span></span>
* <span data-ttu-id="08d27-230">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-230">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-231">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-231">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-232">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-232">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="08d27-233">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-233">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="08d27-234">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-234">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="08d27-235">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-235">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="08d27-236">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-236">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="08d27-237">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-237">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-238">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-238">Az.Resources</span></span>
* <span data-ttu-id="08d27-239">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="08d27-239">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="08d27-240">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-240">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="08d27-241">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-241">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="08d27-242">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-242">Added example.</span></span>
* <span data-ttu-id="08d27-243">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="08d27-243">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="08d27-244">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="08d27-244">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-245">Az.Sql</span></span>
* <span data-ttu-id="08d27-246">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-246">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="08d27-247">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-247">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="08d27-248">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-248">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="08d27-249">Az.Support</span><span class="sxs-lookup"><span data-stu-id="08d27-249">Az.Support</span></span>
* <span data-ttu-id="08d27-250">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-250">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-251">Az.Websites</span></span>
* <span data-ttu-id="08d27-252">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-252">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="08d27-253">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="08d27-253">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="08d27-254">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="08d27-254">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="08d27-255">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="08d27-255">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="08d27-256">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="08d27-256">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="08d27-257">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="08d27-257">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-258">Az.Accounts</span></span>
* <span data-ttu-id="08d27-259">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="08d27-259">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="08d27-260">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="08d27-260">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="08d27-261">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-261">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08d27-262">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08d27-262">Az.ApiManagement</span></span>
* <span data-ttu-id="08d27-263">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="08d27-263">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="08d27-264">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="08d27-264">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="08d27-265">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-265">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="08d27-266">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="08d27-266">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-267">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-268">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-268">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d27-269">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d27-269">Az.IotHub</span></span>
* <span data-ttu-id="08d27-270">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-270">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="08d27-271">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="08d27-271">New Cmdlets are:</span></span>
    - <span data-ttu-id="08d27-272">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="08d27-272">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="08d27-273">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="08d27-273">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="08d27-274">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="08d27-274">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="08d27-275">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="08d27-275">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="08d27-276">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-276">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="08d27-277">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="08d27-277">New Cmdlets are:</span></span>
    - <span data-ttu-id="08d27-278">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="08d27-278">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="08d27-279">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="08d27-279">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="08d27-280">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="08d27-280">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="08d27-281">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="08d27-281">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="08d27-282">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-282">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="08d27-283">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-283">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="08d27-284">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-284">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="08d27-285">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="08d27-285">New Cmdlets are:</span></span>
    - <span data-ttu-id="08d27-286">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="08d27-286">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="08d27-287">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="08d27-287">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="08d27-288">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-288">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d27-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-289">Az.Monitor</span></span>
* <span data-ttu-id="08d27-290">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="08d27-290">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-291">Az.Network</span></span>
* <span data-ttu-id="08d27-292">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-292">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="08d27-293">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-293">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="08d27-294">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-294">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="08d27-295">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-295">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-296">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-296">Az.Resources</span></span>
* <span data-ttu-id="08d27-297">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-297">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="08d27-298">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="08d27-298">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="08d27-299">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="08d27-299">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="08d27-300">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="08d27-300">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="08d27-301">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-301">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="08d27-302">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-302">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="08d27-303">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-303">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="08d27-304">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="08d27-304">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="08d27-305">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="08d27-305">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="08d27-306">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="08d27-306">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="08d27-307">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="08d27-307">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="08d27-308">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-308">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="08d27-309">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="08d27-309">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="08d27-310">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-310">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-311">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-311">Az.Sql</span></span>
* <span data-ttu-id="08d27-312">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-312">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="08d27-313">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-313">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="08d27-314">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="08d27-314">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="08d27-315">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="08d27-315">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="08d27-316">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="08d27-316">Remove an LTR backup</span></span>
    - <span data-ttu-id="08d27-317">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="08d27-317">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="08d27-318">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-318">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="08d27-319">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-319">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="08d27-320">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-320">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-321">Az.Storage</span></span>
* <span data-ttu-id="08d27-322">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-322">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="08d27-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="08d27-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="08d27-324">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-324">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="08d27-325">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="08d27-325">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="08d27-326">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="08d27-326">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-327">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-327">Az.Websites</span></span>
* <span data-ttu-id="08d27-328">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-328">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="08d27-329">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="08d27-329">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="08d27-330">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-330">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="08d27-331">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="08d27-331">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="08d27-332">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-332">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="08d27-333">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="08d27-333">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08d27-334">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="08d27-334">Highlights since the last major release</span></span>
* <span data-ttu-id="08d27-335">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-335">Updated client side telemetry.</span></span>
* <span data-ttu-id="08d27-336">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-336">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="08d27-337">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-337">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08d27-338">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-338">Az.Accounts</span></span>
* <span data-ttu-id="08d27-339">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-339">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d27-340">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d27-340">Az.Automation</span></span>
* <span data-ttu-id="08d27-341">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-341">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08d27-342">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d27-342">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d27-343">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-343">Updated SDK to 7.0</span></span>
* <span data-ttu-id="08d27-344">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-344">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-345">Az.Compute</span></span>
* <span data-ttu-id="08d27-346">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="08d27-346">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08d27-347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08d27-347">Az.FrontDoor</span></span>
* <span data-ttu-id="08d27-348">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-348">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d27-349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d27-349">Az.IotHub</span></span>
* <span data-ttu-id="08d27-350">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-350">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="08d27-351">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="08d27-351">New Cmdlets are:</span></span>
    - <span data-ttu-id="08d27-352">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="08d27-352">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="08d27-353">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="08d27-353">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="08d27-354">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="08d27-354">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="08d27-355">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="08d27-355">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d27-356">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d27-356">Az.KeyVault</span></span>
* <span data-ttu-id="08d27-357">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-357">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d27-358">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-358">Az.Monitor</span></span>
* <span data-ttu-id="08d27-359">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-359">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="08d27-360">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-360">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="08d27-361">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="08d27-361">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-362">Az.Network</span></span>
* <span data-ttu-id="08d27-363">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-363">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="08d27-364">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-364">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="08d27-365">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-365">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="08d27-366">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="08d27-366">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="08d27-367">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="08d27-367">No new cmdlets are added.</span></span> <span data-ttu-id="08d27-368">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="08d27-368">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-370">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-370">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-371">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-371">Az.Resources</span></span>
* <span data-ttu-id="08d27-372">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="08d27-372">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="08d27-373">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="08d27-373">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="08d27-374">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="08d27-374">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="08d27-375">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="08d27-375">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="08d27-376">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-376">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="08d27-377">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-377">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="08d27-378">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-378">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="08d27-379">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-379">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-380">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-380">Az.Sql</span></span>
* <span data-ttu-id="08d27-381">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-381">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="08d27-382">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-382">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="08d27-383">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="08d27-383">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="08d27-384">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="08d27-384">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="08d27-385">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-385">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="08d27-386">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="08d27-386">Az.StorageSync</span></span>
* <span data-ttu-id="08d27-387">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-387">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="08d27-388">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="08d27-388">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08d27-389">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="08d27-389">Highlights since the last major release</span></span>
* <span data-ttu-id="08d27-390">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="08d27-390">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="08d27-391">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-391">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08d27-392">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-392">Az.Accounts</span></span>
* <span data-ttu-id="08d27-393">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="08d27-393">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="08d27-394">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-394">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08d27-395">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08d27-395">Az.ApiManagement</span></span>
* <span data-ttu-id="08d27-396">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="08d27-396">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="08d27-397">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="08d27-397">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="08d27-398">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-398">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="08d27-399">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-399">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-400">Az.Compute</span></span>
* <span data-ttu-id="08d27-401">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="08d27-401">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="08d27-402">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-402">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="08d27-403">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-403">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="08d27-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="08d27-405">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-405">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-406">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-407">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-407">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="08d27-408">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="08d27-408">Az.DeploymentManager</span></span>
* <span data-ttu-id="08d27-409">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="08d27-409">Adds LIST operations for resources</span></span>
* <span data-ttu-id="08d27-410">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="08d27-410">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08d27-411">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08d27-411">Az.HDInsight</span></span>
* <span data-ttu-id="08d27-412">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-412">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d27-413">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d27-413">Az.KeyVault</span></span>
* <span data-ttu-id="08d27-414">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-414">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-415">Az.Network</span></span>
* <span data-ttu-id="08d27-416">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-416">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="08d27-417">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="08d27-417">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="08d27-418">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-418">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="08d27-419">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-419">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="08d27-420">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="08d27-420">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="08d27-421">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-421">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="08d27-422">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-422">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="08d27-423">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-423">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="08d27-424">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-424">New cmdlets added:</span></span>
        - <span data-ttu-id="08d27-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d27-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="08d27-426">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-426">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="08d27-427">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="08d27-427">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="08d27-428">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-428">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08d27-429">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-429">Az.PolicyInsights</span></span>
* <span data-ttu-id="08d27-430">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="08d27-430">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="08d27-431">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-431">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="08d27-432">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-432">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="08d27-433">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-433">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-434">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-434">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-435">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-435">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="08d27-436">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="08d27-436">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-437">Az.Resources</span></span>
* <span data-ttu-id="08d27-438">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-438">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="08d27-439">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-439">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-440">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-440">Az.Sql</span></span>
<span data-ttu-id="08d27-441">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-441">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-442">Az.Storage</span></span>
* <span data-ttu-id="08d27-443">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="08d27-443">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="08d27-444">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-444">New-AzStorageAccount</span></span>
* <span data-ttu-id="08d27-445">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="08d27-445">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="08d27-446">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-446">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-447">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-447">Az.Websites</span></span>
* <span data-ttu-id="08d27-448">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="08d27-448">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="08d27-449">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-449">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="08d27-450">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="08d27-450">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-451">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-451">Az.Accounts</span></span>
* <span data-ttu-id="08d27-452">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-452">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08d27-453">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08d27-453">Az.Cdn</span></span>
* <span data-ttu-id="08d27-454">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="08d27-454">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-455">Az.Compute</span></span>
* <span data-ttu-id="08d27-456">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-456">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="08d27-457">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="08d27-457">Az.ContainerInstance</span></span>
* <span data-ttu-id="08d27-458">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-458">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="08d27-459">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="08d27-459">Az.DataBoxEdge</span></span>
* <span data-ttu-id="08d27-460">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-460">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="08d27-461">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="08d27-461">Get the Edge Storage Container</span></span>
* <span data-ttu-id="08d27-462">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-462">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="08d27-463">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="08d27-463">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="08d27-464">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-464">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="08d27-465">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="08d27-465">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="08d27-466">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-466">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="08d27-467">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="08d27-467">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="08d27-468">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-468">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="08d27-469">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="08d27-469">Get the Edge Storage Account</span></span>
* <span data-ttu-id="08d27-470">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-470">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="08d27-471">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="08d27-471">Create new Edge Storage Account</span></span>
* <span data-ttu-id="08d27-472">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-472">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="08d27-473">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="08d27-473">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="08d27-474">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="08d27-474">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="08d27-475">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="08d27-475">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="08d27-476">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-476">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="08d27-477">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="08d27-477">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-478">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-478">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-479">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-479">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="08d27-480">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-480">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="08d27-481">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-481">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="08d27-482">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="08d27-482">Az.DevTestLabs</span></span>
* <span data-ttu-id="08d27-483">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-483">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08d27-484">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08d27-484">Az.EventHub</span></span>
* <span data-ttu-id="08d27-485">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-485">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08d27-486">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08d27-486">Az.HDInsight</span></span>
* <span data-ttu-id="08d27-487">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-487">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="08d27-488">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="08d27-488">Az.MachineLearning</span></span>
* <span data-ttu-id="08d27-489">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-489">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="08d27-490">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="08d27-490">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="08d27-491">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="08d27-491">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="08d27-492">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="08d27-492">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="08d27-493">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="08d27-493">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="08d27-494">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="08d27-494">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="08d27-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="08d27-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="08d27-496">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="08d27-496">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-497">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-497">Az.Network</span></span>
* <span data-ttu-id="08d27-498">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-498">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-499">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-499">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-500">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-500">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="08d27-501">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-501">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="08d27-502">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-502">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="08d27-503">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-503">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-504">Az.Resources</span></span>
* <span data-ttu-id="08d27-505">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-505">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-506">Az.Sql</span></span>
* <span data-ttu-id="08d27-507">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-507">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="08d27-508">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-508">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="08d27-509">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="08d27-509">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="08d27-510">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-510">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-511">Az.Storage</span></span>
* <span data-ttu-id="08d27-512">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-512">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="08d27-513">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d27-513">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="08d27-514">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="08d27-514">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="08d27-515">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-515">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="08d27-516">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-516">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="08d27-517">Genel</span><span class="sxs-lookup"><span data-stu-id="08d27-517">General</span></span>
* <span data-ttu-id="08d27-518">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-518">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08d27-519">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-519">Az.Accounts</span></span>
* <span data-ttu-id="08d27-520">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="08d27-520">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="08d27-521">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="08d27-521">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08d27-522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08d27-522">Az.Batch</span></span>
* <span data-ttu-id="08d27-523">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-523">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-524">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-524">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-525">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-525">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08d27-526">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08d27-526">Az.FrontDoor</span></span>
* <span data-ttu-id="08d27-527">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-527">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="08d27-528">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-528">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="08d27-529">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="08d27-529">Az.HealthcareApis</span></span>
* <span data-ttu-id="08d27-530">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="08d27-530">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d27-531">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d27-531">Az.KeyVault</span></span>
* <span data-ttu-id="08d27-532">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-532">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="08d27-533">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="08d27-533">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="08d27-534">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-534">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d27-535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-535">Az.Monitor</span></span>
* <span data-ttu-id="08d27-536">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-536">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="08d27-537">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="08d27-537">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="08d27-538">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="08d27-538">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-539">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-539">Az.Network</span></span>
* <span data-ttu-id="08d27-540">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-540">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-541">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-541">Az.Resources</span></span>
* <span data-ttu-id="08d27-542">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-542">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="08d27-543">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-543">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-544">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-544">Az.Sql</span></span>
* <span data-ttu-id="08d27-545">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-545">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-546">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-546">Az.Storage</span></span>
* <span data-ttu-id="08d27-547">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="08d27-547">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="08d27-548">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="08d27-548">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="08d27-549">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="08d27-549">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="08d27-550">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="08d27-550">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="08d27-551">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="08d27-551">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="08d27-552">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-552">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="08d27-553">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-553">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="08d27-554">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08d27-554">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="08d27-555">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08d27-555">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="08d27-556">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-556">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="08d27-557">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="08d27-557">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="08d27-558">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-558">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="08d27-559">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="08d27-559">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="08d27-560">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-560">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08d27-561">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="08d27-561">Highlights since the last major release</span></span>
* <span data-ttu-id="08d27-562">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="08d27-562">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="08d27-563">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="08d27-563">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-564">Az.Compute</span></span>
* <span data-ttu-id="08d27-565">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="08d27-565">VM Reapply feature</span></span>
    - <span data-ttu-id="08d27-566">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="08d27-566">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="08d27-567">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="08d27-567">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="08d27-568">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08d27-568">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="08d27-569">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="08d27-569">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="08d27-570">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-570">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="08d27-571">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-571">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="08d27-572">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-572">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="08d27-573">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-573">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="08d27-574">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-574">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="08d27-575">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-575">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="08d27-576">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="08d27-576">Az.DataBoxEdge</span></span>
* <span data-ttu-id="08d27-577">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-577">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="08d27-578">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="08d27-578">Get the Order</span></span>
* <span data-ttu-id="08d27-579">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-579">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="08d27-580">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="08d27-580">Create new Order</span></span>
* <span data-ttu-id="08d27-581">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-581">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="08d27-582">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="08d27-582">Remove the Order</span></span>
* <span data-ttu-id="08d27-583">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="08d27-583">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="08d27-584">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="08d27-584">Now creates Local Share</span></span>
* <span data-ttu-id="08d27-585">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-585">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="08d27-586">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="08d27-586">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="08d27-587">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-587">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="08d27-588">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="08d27-588">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="08d27-589">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-589">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="08d27-590">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="08d27-590">Gets the information about Triggers</span></span>
* <span data-ttu-id="08d27-591">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-591">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="08d27-592">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="08d27-592">Create new Triggers</span></span>
* <span data-ttu-id="08d27-593">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-593">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="08d27-594">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="08d27-594">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-595">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-596">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-596">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="08d27-597">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-597">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-598">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-599">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-599">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08d27-600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08d27-600">Az.EventHub</span></span>
* <span data-ttu-id="08d27-601">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-601">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08d27-602">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08d27-602">Az.FrontDoor</span></span>
* <span data-ttu-id="08d27-603">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-603">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="08d27-604">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-604">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="08d27-605">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-605">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="08d27-606">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="08d27-606">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-607">Az.Network</span></span>
* <span data-ttu-id="08d27-608">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-608">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="08d27-609">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="08d27-609">Az.PrivateDns</span></span>
* <span data-ttu-id="08d27-610">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-610">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-612">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-612">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="08d27-613">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="08d27-613">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="08d27-614">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-614">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="08d27-615">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="08d27-615">Az.RedisCache</span></span>
* <span data-ttu-id="08d27-616">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-616">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="08d27-617">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-617">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="08d27-618">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-618">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-619">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-619">Az.Resources</span></span>
- <span data-ttu-id="08d27-620">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-620">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="08d27-621">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-621">Updated create policy definition help example</span></span>
- <span data-ttu-id="08d27-622">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-622">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="08d27-623">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-623">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="08d27-624">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-624">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-625">Az.Sql</span></span>
* <span data-ttu-id="08d27-626">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-626">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="08d27-627">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-627">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="08d27-628">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-628">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="08d27-629">Genel</span><span class="sxs-lookup"><span data-stu-id="08d27-629">General</span></span>
* <span data-ttu-id="08d27-630">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="08d27-630">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08d27-631">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-631">Az.Accounts</span></span>
* <span data-ttu-id="08d27-632">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="08d27-632">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="08d27-633">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="08d27-633">Az.Advisor</span></span>
* <span data-ttu-id="08d27-634">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-634">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08d27-635">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08d27-635">Az.Batch</span></span>
* <span data-ttu-id="08d27-636">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-636">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="08d27-637">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="08d27-637">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="08d27-638">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-638">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="08d27-639">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-639">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="08d27-640">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="08d27-640">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="08d27-641">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="08d27-641">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="08d27-642">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="08d27-642">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="08d27-643">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-643">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="08d27-644">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-644">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="08d27-645">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-645">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="08d27-646">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="08d27-646">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="08d27-647">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="08d27-647">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="08d27-648">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-648">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="08d27-649">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="08d27-649">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="08d27-650">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-650">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="08d27-651">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-651">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="08d27-652">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-652">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="08d27-653">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-653">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="08d27-654">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-654">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="08d27-655">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-655">This operation is no longer supported.</span></span>
* <span data-ttu-id="08d27-656">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-656">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="08d27-657">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-657">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="08d27-658">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-658">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="08d27-659">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-659">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="08d27-660">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-660">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="08d27-661">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-661">New non-verified images are also now returned.</span></span> <span data-ttu-id="08d27-662">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-662">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="08d27-663">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-663">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="08d27-664">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-664">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="08d27-665">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-665">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="08d27-666">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-666">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="08d27-667">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-667">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="08d27-668">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-668">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="08d27-669">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-669">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="08d27-670">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="08d27-670">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="08d27-671">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="08d27-671">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08d27-672">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08d27-672">Az.Cdn</span></span>
* <span data-ttu-id="08d27-673">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-673">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="08d27-674">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-674">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-675">Az.Compute</span></span>
* <span data-ttu-id="08d27-676">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="08d27-676">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="08d27-677">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="08d27-677">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="08d27-678">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="08d27-678">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="08d27-679">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-679">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="08d27-680">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-680">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="08d27-681">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="08d27-681">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="08d27-682">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-682">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="08d27-683">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="08d27-683">Breaking changes</span></span>
    - <span data-ttu-id="08d27-684">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="08d27-684">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="08d27-685">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="08d27-685">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-686">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-686">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-687">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-687">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-688">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-688">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-689">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="08d27-689">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="08d27-690">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="08d27-690">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="08d27-691">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="08d27-691">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="08d27-692">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="08d27-692">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="08d27-693">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="08d27-693">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="08d27-694">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="08d27-694">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08d27-695">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08d27-695">Az.FrontDoor</span></span>
* <span data-ttu-id="08d27-696">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-696">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08d27-697">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08d27-697">Az.HDInsight</span></span>
* <span data-ttu-id="08d27-698">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-698">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="08d27-699">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-699">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="08d27-700">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-700">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="08d27-701">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="08d27-701">Removed five cmdlets:</span></span>
    - <span data-ttu-id="08d27-702">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="08d27-702">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="08d27-703">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="08d27-703">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="08d27-704">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="08d27-704">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="08d27-705">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="08d27-705">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="08d27-706">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="08d27-706">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="08d27-707">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-707">Added three cmdlets:</span></span>
    - <span data-ttu-id="08d27-708">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="08d27-708">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="08d27-709">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="08d27-709">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="08d27-710">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="08d27-710">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="08d27-711">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-711">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="08d27-712">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-712">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="08d27-713">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-713">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="08d27-714">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-714">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="08d27-715">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-715">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="08d27-716">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-716">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="08d27-717">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-717">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="08d27-718">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-718">Added some scenario test cases.</span></span>
* <span data-ttu-id="08d27-719">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="08d27-719">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d27-720">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d27-720">Az.IotHub</span></span>
* <span data-ttu-id="08d27-721">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="08d27-721">Breaking changes:</span></span>
    - <span data-ttu-id="08d27-722">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="08d27-722">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="08d27-723">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-723">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="08d27-724">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="08d27-724">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="08d27-725">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-725">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="08d27-726">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-726">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="08d27-727">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-727">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="08d27-728">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-728">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="08d27-729">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-729">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="08d27-730">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="08d27-730">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="08d27-731">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-731">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="08d27-732">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="08d27-732">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="08d27-733">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-733">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-734">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-734">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-735">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-735">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="08d27-736">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-736">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="08d27-737">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-737">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="08d27-738">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-738">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="08d27-739">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-739">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="08d27-740">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-740">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="08d27-741">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-741">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="08d27-742">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-742">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="08d27-743">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-743">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-744">Az.Resources</span></span>
* <span data-ttu-id="08d27-745">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-745">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-746">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-746">Az.Network</span></span>
* <span data-ttu-id="08d27-747">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-747">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="08d27-748">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-748">Updated cmdlet:</span></span>
        - <span data-ttu-id="08d27-749">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-749">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08d27-750">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-750">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08d27-751">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-751">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08d27-752">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-752">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08d27-753">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-753">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="08d27-754">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-754">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="08d27-755">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="08d27-755">New cmdlet:</span></span>
        - <span data-ttu-id="08d27-756">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="08d27-756">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="08d27-757">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-757">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="08d27-758">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-758">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="08d27-759">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-759">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="08d27-760">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-760">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="08d27-761">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-761">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="08d27-762">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-762">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="08d27-763">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-763">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="08d27-764">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-764">New cmdlets added:</span></span>
        - <span data-ttu-id="08d27-765">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="08d27-765">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="08d27-766">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="08d27-766">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="08d27-767">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="08d27-767">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="08d27-768">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="08d27-768">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="08d27-769">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="08d27-769">Set-AzVirtualHub</span></span>
* <span data-ttu-id="08d27-770">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-770">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="08d27-771">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="08d27-772">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-772">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="08d27-773">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-773">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="08d27-774">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-774">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="08d27-775">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-775">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="08d27-776">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-776">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="08d27-777">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-777">New cmdlets added:</span></span>
        - <span data-ttu-id="08d27-778">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-778">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="08d27-779">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-779">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="08d27-780">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-780">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="08d27-781">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-781">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="08d27-782">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-782">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="08d27-783">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-783">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="08d27-784">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-784">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="08d27-785">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-785">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="08d27-786">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-786">New cmdlets added:</span></span>
        - <span data-ttu-id="08d27-787">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="08d27-787">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="08d27-788">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="08d27-788">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="08d27-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="08d27-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="08d27-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="08d27-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="08d27-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="08d27-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="08d27-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d27-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="08d27-793">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="08d27-794">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-794">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="08d27-795">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-795">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="08d27-796">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-796">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="08d27-797">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-797">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="08d27-798">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-798">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="08d27-799">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-799">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="08d27-800">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-800">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="08d27-801">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-801">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="08d27-802">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="08d27-802">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="08d27-803">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-803">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="08d27-804">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-804">New cmdlets added:</span></span>
        - <span data-ttu-id="08d27-805">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="08d27-805">New-AzIpGroup</span></span>
        - <span data-ttu-id="08d27-806">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="08d27-806">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="08d27-807">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="08d27-807">Get-AzIpGroup</span></span>
        - <span data-ttu-id="08d27-808">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="08d27-808">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08d27-809">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d27-809">Az.ServiceFabric</span></span>
* <span data-ttu-id="08d27-810">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-810">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-811">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-811">Az.Sql</span></span>
* <span data-ttu-id="08d27-812">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-812">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="08d27-813">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-813">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="08d27-814">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="08d27-814">Removed deprecated aliases:</span></span>
* <span data-ttu-id="08d27-815">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="08d27-815">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="08d27-816">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="08d27-816">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="08d27-817">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-817">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="08d27-818">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-818">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="08d27-819">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-819">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="08d27-820">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-820">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-821">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-821">Az.Storage</span></span>
* <span data-ttu-id="08d27-822">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="08d27-822">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="08d27-823">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-823">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="08d27-824">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-824">Set-AzStorageAccount</span></span>
* <span data-ttu-id="08d27-825">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="08d27-825">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="08d27-826">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="08d27-826">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="08d27-827">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="08d27-827">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="08d27-828">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-828">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="08d27-829">Genel</span><span class="sxs-lookup"><span data-stu-id="08d27-829">General</span></span>
* <span data-ttu-id="08d27-830">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="08d27-830">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08d27-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-831">Az.Accounts</span></span>
* <span data-ttu-id="08d27-832">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-832">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08d27-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08d27-833">Az.ApiManagement</span></span>
* <span data-ttu-id="08d27-834">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-834">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="08d27-835">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-835">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d27-836">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d27-836">Az.Automation</span></span>
* <span data-ttu-id="08d27-837">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-837">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08d27-838">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08d27-838">Az.Batch</span></span>
* <span data-ttu-id="08d27-839">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="08d27-839">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-840">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-840">Az.Compute</span></span>
* <span data-ttu-id="08d27-841">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-841">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="08d27-842">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-842">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="08d27-843">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-843">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="08d27-844">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-844">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-845">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-845">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-846">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="08d27-846">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="08d27-847">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="08d27-847">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="08d27-848">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-848">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-849">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-849">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-850">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-850">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="08d27-851">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="08d27-851">Az.HealthcareApis</span></span>
* <span data-ttu-id="08d27-852">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-852">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="08d27-853">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-853">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="08d27-854">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-854">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="08d27-855">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-855">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d27-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d27-856">Az.IotHub</span></span>
* <span data-ttu-id="08d27-857">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="08d27-857">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="08d27-858">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="08d27-858">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d27-859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-859">Az.Monitor</span></span>
* <span data-ttu-id="08d27-860">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-860">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="08d27-861">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="08d27-861">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="08d27-862">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="08d27-862">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="08d27-863">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-863">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-864">Az.Network</span></span>
* <span data-ttu-id="08d27-865">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-865">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="08d27-866">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-866">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="08d27-867">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-867">New cmdlets added:</span></span>
        - <span data-ttu-id="08d27-868">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="08d27-868">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="08d27-869">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-869">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="08d27-870">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-870">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="08d27-871">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-871">Updated cmdlets:</span></span>
        - <span data-ttu-id="08d27-872">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-872">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="08d27-873">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-873">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="08d27-874">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-874">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="08d27-875">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-875">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="08d27-876">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="08d27-876">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="08d27-877">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="08d27-877">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="08d27-878">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="08d27-878">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="08d27-879">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="08d27-879">Az.RedisCache</span></span>
* <span data-ttu-id="08d27-880">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-880">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-881">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-881">Az.Sql</span></span>
* <span data-ttu-id="08d27-882">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-882">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-883">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-883">Az.Storage</span></span>
* <span data-ttu-id="08d27-884">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-884">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="08d27-885">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="08d27-885">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="08d27-886">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="08d27-886">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="08d27-887">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="08d27-887">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="08d27-888">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-888">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="08d27-889">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="08d27-889">Az.StorageSync</span></span>
* <span data-ttu-id="08d27-890">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-890">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-891">Az.Websites</span></span>
* <span data-ttu-id="08d27-892">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="08d27-892">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="08d27-893">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-893">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="08d27-894">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08d27-894">Az.ApiManagement</span></span>
* <span data-ttu-id="08d27-895">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-895">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="08d27-896">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-896">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="08d27-897">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="08d27-897">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d27-898">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d27-898">Az.Automation</span></span>
* <span data-ttu-id="08d27-899">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-899">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="08d27-900">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-900">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="08d27-901">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-901">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-902">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-902">Az.Compute</span></span>
* <span data-ttu-id="08d27-903">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-903">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="08d27-904">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-904">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="08d27-905">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-905">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="08d27-906">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-906">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="08d27-907">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-907">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="08d27-908">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-908">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="08d27-909">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-909">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="08d27-910">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-910">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="08d27-911">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-911">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-912">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-912">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-913">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="08d27-913">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="08d27-914">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-914">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08d27-915">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08d27-915">Az.HDInsight</span></span>
* <span data-ttu-id="08d27-916">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="08d27-916">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d27-917">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d27-917">Az.IotHub</span></span>
* <span data-ttu-id="08d27-918">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-918">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="08d27-919">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-919">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="08d27-920">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="08d27-920">New cmdlets are:</span></span>
    - <span data-ttu-id="08d27-921">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="08d27-921">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="08d27-922">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="08d27-922">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="08d27-923">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="08d27-923">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="08d27-924">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="08d27-924">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d27-925">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-925">Az.Monitor</span></span>
* <span data-ttu-id="08d27-926">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="08d27-926">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="08d27-927">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="08d27-927">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="08d27-928">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="08d27-928">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="08d27-929">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="08d27-929">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="08d27-930">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-930">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="08d27-931">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-931">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="08d27-932">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="08d27-932">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="08d27-933">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="08d27-933">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="08d27-934">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-934">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="08d27-935">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="08d27-935">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="08d27-936">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-936">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="08d27-937">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="08d27-937">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="08d27-938">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-938">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="08d27-939">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="08d27-939">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="08d27-940">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="08d27-940">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="08d27-941">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="08d27-941">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="08d27-942">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="08d27-942">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="08d27-943">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="08d27-943">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="08d27-944">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-944">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="08d27-945">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-945">Overall improved help files</span></span>
* <span data-ttu-id="08d27-946">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-946">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-947">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-947">Az.Network</span></span>
* <span data-ttu-id="08d27-948">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-948">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="08d27-949">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-949">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="08d27-950">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-950">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="08d27-951">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-951">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="08d27-952">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-952">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="08d27-953">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-953">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="08d27-954">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-954">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="08d27-955">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-955">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="08d27-956">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-956">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="08d27-957">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-957">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="08d27-958">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-958">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="08d27-959">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="08d27-959">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="08d27-960">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-960">New cmdlets</span></span>
        - <span data-ttu-id="08d27-961">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="08d27-961">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="08d27-962">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-962">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="08d27-963">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="08d27-964">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="08d27-964">New-VpnSite</span></span>
        - <span data-ttu-id="08d27-965">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="08d27-965">Update-VpnSite</span></span>
        - <span data-ttu-id="08d27-966">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-966">New-VpnConnection</span></span>
        - <span data-ttu-id="08d27-967">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-967">Update-VpnConnection</span></span>
* <span data-ttu-id="08d27-968">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-968">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-969">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-970">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-970">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="08d27-971">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-971">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-972">Az.Resources</span></span>
* <span data-ttu-id="08d27-973">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-973">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08d27-974">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d27-974">Az.ServiceFabric</span></span>
* <span data-ttu-id="08d27-975">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-975">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="08d27-976">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="08d27-976">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="08d27-977">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="08d27-977">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="08d27-978">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="08d27-978">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="08d27-979">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="08d27-979">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="08d27-980">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="08d27-980">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="08d27-981">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="08d27-981">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="08d27-982">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="08d27-982">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="08d27-983">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="08d27-983">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="08d27-984">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="08d27-984">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="08d27-985">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="08d27-985">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="08d27-986">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="08d27-986">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="08d27-987">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="08d27-987">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="08d27-988">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="08d27-988">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="08d27-989">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="08d27-989">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="08d27-990">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-990">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="08d27-991">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="08d27-991">Az.SignalR</span></span>
* <span data-ttu-id="08d27-992">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-992">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-993">Az.Sql</span></span>
* <span data-ttu-id="08d27-994">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-994">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="08d27-995">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-995">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="08d27-996">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-996">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="08d27-997">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-997">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="08d27-998">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-998">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-999">Az.Storage</span></span>
* <span data-ttu-id="08d27-1000">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1000">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="08d27-1001">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1001">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="08d27-1002">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="08d27-1002">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="08d27-1003">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="08d27-1003">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="08d27-1004">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1004">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="08d27-1005">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="08d27-1005">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="08d27-1006">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1006">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="08d27-1007">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08d27-1007">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="08d27-1008">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08d27-1008">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="08d27-1009">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08d27-1009">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="08d27-1010">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08d27-1010">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-1011">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-1011">Az.Websites</span></span>
* <span data-ttu-id="08d27-1012">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="08d27-1012">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="08d27-1013">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="08d27-1013">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="08d27-1014">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1014">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="08d27-1015">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1015">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="08d27-1016">Genel</span><span class="sxs-lookup"><span data-stu-id="08d27-1016">General</span></span>
* <span data-ttu-id="08d27-1017">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1017">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08d27-1018">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1018">Az.Accounts</span></span>
* <span data-ttu-id="08d27-1019">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="08d27-1019">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="08d27-1020">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="08d27-1020">Az.Aks</span></span>
* <span data-ttu-id="08d27-1021">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1021">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="08d27-1022">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="08d27-1022">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08d27-1023">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08d27-1023">Az.ApiManagement</span></span>
* <span data-ttu-id="08d27-1024">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1024">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="08d27-1025">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1025">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="08d27-1026">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1026">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="08d27-1027">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="08d27-1027">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="08d27-1028">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1028">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08d27-1029">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08d27-1029">Az.Batch</span></span>
* <span data-ttu-id="08d27-1030">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1030">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08d27-1031">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08d27-1031">Az.Cdn</span></span>
* <span data-ttu-id="08d27-1032">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1032">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1033">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1033">Az.Compute</span></span>
* <span data-ttu-id="08d27-1034">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1034">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="08d27-1035">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1035">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="08d27-1036">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1036">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="08d27-1037">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1037">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="08d27-1038">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="08d27-1038">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="08d27-1039">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1039">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="08d27-1040">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1040">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="08d27-1041">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1041">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-1042">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-1042">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-1043">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1043">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="08d27-1044">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1044">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="08d27-1045">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1045">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="08d27-1046">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1046">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-1047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-1047">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-1048">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1048">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08d27-1049">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08d27-1049">Az.EventHub</span></span>
* <span data-ttu-id="08d27-1050">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="08d27-1050">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="08d27-1051">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="08d27-1051">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="08d27-1052">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1052">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="08d27-1053">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="08d27-1053">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="08d27-1054">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="08d27-1054">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="08d27-1055">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1055">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d27-1056">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-1056">Az.Monitor</span></span>
* <span data-ttu-id="08d27-1057">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1057">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-1058">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-1058">Az.Network</span></span>
* <span data-ttu-id="08d27-1059">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1059">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="08d27-1060">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1060">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="08d27-1061">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1061">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="08d27-1062">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="08d27-1062">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="08d27-1063">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1063">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="08d27-1064">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1064">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="08d27-1065">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1065">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08d27-1066">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-1066">Az.OperationalInsights</span></span>
* <span data-ttu-id="08d27-1067">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1067">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="08d27-1068">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1068">Added example</span></span>
    - <span data-ttu-id="08d27-1069">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1069">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="08d27-1070">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1070">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="08d27-1071">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1071">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-1073">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1073">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1074">Az.Resources</span></span>
* <span data-ttu-id="08d27-1075">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1075">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="08d27-1076">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1076">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="08d27-1077">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="08d27-1077">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="08d27-1078">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1078">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08d27-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08d27-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="08d27-1080">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="08d27-1080">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="08d27-1081">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="08d27-1081">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="08d27-1082">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1082">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08d27-1083">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d27-1083">Az.ServiceFabric</span></span>
* <span data-ttu-id="08d27-1084">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-1084">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="08d27-1085">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="08d27-1085">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="08d27-1086">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="08d27-1086">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="08d27-1087">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1087">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="08d27-1088">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="08d27-1088">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="08d27-1089">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-1089">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1090">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1090">Az.Sql</span></span>
* <span data-ttu-id="08d27-1091">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1091">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-1092">Az.Storage</span></span>
* <span data-ttu-id="08d27-1093">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1093">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="08d27-1094">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="08d27-1094">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="08d27-1095">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="08d27-1095">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="08d27-1096">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="08d27-1096">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="08d27-1097">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="08d27-1097">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="08d27-1098">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="08d27-1098">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-1099">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-1099">Az.Websites</span></span>
* <span data-ttu-id="08d27-1100">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1100">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="08d27-1101">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-1102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1102">Az.Accounts</span></span>
* <span data-ttu-id="08d27-1103">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="08d27-1104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-1104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="08d27-1105">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d27-1106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d27-1106">Az.Automation</span></span>
* <span data-ttu-id="08d27-1107">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1107">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08d27-1108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1108">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d27-1109">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1110">Az.Compute</span></span>
* <span data-ttu-id="08d27-1111">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="08d27-1112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="08d27-1112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="08d27-1113">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="08d27-1114">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="08d27-1114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-1115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-1115">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-1116">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="08d27-1117">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08d27-1118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08d27-1118">Az.EventHub</span></span>
* <span data-ttu-id="08d27-1119">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="08d27-1119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="08d27-1120">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d27-1121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d27-1121">Az.KeyVault</span></span>
* <span data-ttu-id="08d27-1122">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="08d27-1123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="08d27-1123">Az.LogicApp</span></span>
* <span data-ttu-id="08d27-1124">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="08d27-1124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="08d27-1125">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="08d27-1126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1126">Az.ManagedServices</span></span>
* <span data-ttu-id="08d27-1127">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="08d27-1127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-1128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-1128">Az.Network</span></span>
* <span data-ttu-id="08d27-1129">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="08d27-1130">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1130">New cmdlets</span></span>
        - <span data-ttu-id="08d27-1131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="08d27-1131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="08d27-1132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="08d27-1132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="08d27-1133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-1133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08d27-1134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-1134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08d27-1135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-1135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08d27-1136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-1136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08d27-1137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="08d27-1137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="08d27-1138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="08d27-1138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="08d27-1139">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="08d27-1139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="08d27-1140">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="08d27-1141">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="08d27-1142">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="08d27-1143">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-1143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="08d27-1144">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="08d27-1145">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1145">Updated cmdlets</span></span>
        - <span data-ttu-id="08d27-1146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-1146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="08d27-1147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-1147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="08d27-1148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-1148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="08d27-1149">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="08d27-1150">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="08d27-1151">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-1151">Updated cmdlet:</span></span>
        - <span data-ttu-id="08d27-1152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-1152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="08d27-1153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-1153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="08d27-1154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-1154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="08d27-1155">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="08d27-1156">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="08d27-1157">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="08d27-1157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08d27-1158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-1158">Az.OperationalInsights</span></span>
* <span data-ttu-id="08d27-1159">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1159">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="08d27-1160">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-1162">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="08d27-1163">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="08d27-1164">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="08d27-1165">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="08d27-1166">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="08d27-1167">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="08d27-1168">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="08d27-1169">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="08d27-1170">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="08d27-1171">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1172">Az.Resources</span></span>
- <span data-ttu-id="08d27-1173">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-1173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="08d27-1174">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08d27-1175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08d27-1175">Az.ServiceBus</span></span>
* <span data-ttu-id="08d27-1176">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="08d27-1176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="08d27-1177">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1178">Az.Sql</span></span>
* <span data-ttu-id="08d27-1179">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="08d27-1180">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="08d27-1181">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-1182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-1182">Az.Storage</span></span>
* <span data-ttu-id="08d27-1183">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="08d27-1184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="08d27-1184">Az.StorageSync</span></span>
* <span data-ttu-id="08d27-1185">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-1185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="08d27-1186">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-1187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-1187">Az.Websites</span></span>
* <span data-ttu-id="08d27-1188">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="08d27-1189">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="08d27-1190">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="08d27-1191">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-1192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1192">Az.Accounts</span></span>
* <span data-ttu-id="08d27-1193">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="08d27-1194">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="08d27-1195">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="08d27-1196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="08d27-1196">Az.Advisor</span></span>
* <span data-ttu-id="08d27-1197">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-1197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="08d27-1198">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="08d27-1198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08d27-1199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08d27-1199">Az.ApiManagement</span></span>
* <span data-ttu-id="08d27-1200">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="08d27-1201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="08d27-1201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="08d27-1202">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="08d27-1203">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="08d27-1203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="08d27-1204">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="08d27-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="08d27-1205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="08d27-1205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="08d27-1206">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d27-1207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d27-1207">Az.Automation</span></span>
* <span data-ttu-id="08d27-1208">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1209">Az.Compute</span></span>
* <span data-ttu-id="08d27-1210">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-1211">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-1212">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-1212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="08d27-1213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="08d27-1213">Az.EventGrid</span></span>
* <span data-ttu-id="08d27-1214">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d27-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d27-1215">Az.IotHub</span></span>
* <span data-ttu-id="08d27-1216">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-1217">Az.Network</span></span>
* <span data-ttu-id="08d27-1218">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="08d27-1219">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08d27-1220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-1220">Az.PolicyInsights</span></span>
* <span data-ttu-id="08d27-1221">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="08d27-1222">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="08d27-1222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08d27-1223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-1223">Az.OperationalInsights</span></span>
* <span data-ttu-id="08d27-1224">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-1225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1225">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-1226">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="08d27-1226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1227">Az.Resources</span></span>
    - <span data-ttu-id="08d27-1228">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="08d27-1228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="08d27-1229">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="08d27-1230">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="08d27-1231">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08d27-1232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08d27-1232">Az.ServiceBus</span></span>
* <span data-ttu-id="08d27-1233">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1234">Az.Sql</span></span>
* <span data-ttu-id="08d27-1235">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="08d27-1236">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-1236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="08d27-1237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="08d27-1237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="08d27-1238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="08d27-1238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="08d27-1239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="08d27-1239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="08d27-1240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="08d27-1240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="08d27-1241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="08d27-1241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="08d27-1242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="08d27-1242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="08d27-1243">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-1243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-1244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-1244">Az.Storage</span></span>
* <span data-ttu-id="08d27-1245">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-1245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="08d27-1246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="08d27-1246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="08d27-1247">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="08d27-1248">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="08d27-1248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="08d27-1249">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="08d27-1250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-1250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="08d27-1251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-1251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="08d27-1252">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="08d27-1253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="08d27-1253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="08d27-1254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="08d27-1254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="08d27-1255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="08d27-1255">Az.StorageSync</span></span>
* <span data-ttu-id="08d27-1256">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="08d27-1256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="08d27-1257">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-1258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1258">Az.Accounts</span></span>
* <span data-ttu-id="08d27-1259">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="08d27-1260">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="08d27-1260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="08d27-1261">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="08d27-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="08d27-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="08d27-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="08d27-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1264">Az.Compute</span></span>
* <span data-ttu-id="08d27-1265">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-1265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="08d27-1266">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="08d27-1267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="08d27-1267">Az.Dns</span></span>
* <span data-ttu-id="08d27-1268">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="08d27-1269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="08d27-1269">Az.EventGrid</span></span>
* <span data-ttu-id="08d27-1270">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="08d27-1271">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="08d27-1271">New cmdlets:</span></span>
    - <span data-ttu-id="08d27-1272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="08d27-1272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="08d27-1273">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="08d27-1273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="08d27-1274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="08d27-1274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="08d27-1275">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="08d27-1275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="08d27-1276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="08d27-1276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="08d27-1277">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="08d27-1277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="08d27-1278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="08d27-1278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="08d27-1279">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="08d27-1279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="08d27-1280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="08d27-1280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="08d27-1281">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="08d27-1281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="08d27-1282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="08d27-1282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="08d27-1283">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="08d27-1283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="08d27-1284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="08d27-1284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="08d27-1285">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="08d27-1285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="08d27-1286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="08d27-1286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="08d27-1287">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="08d27-1287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="08d27-1288">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-1288">Updated cmdlets:</span></span>
    - <span data-ttu-id="08d27-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="08d27-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="08d27-1290">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="08d27-1290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="08d27-1291">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="08d27-1291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="08d27-1292">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="08d27-1292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="08d27-1293">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-1293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="08d27-1294">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="08d27-1294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="08d27-1295">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="08d27-1295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="08d27-1296">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="08d27-1296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="08d27-1297">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="08d27-1297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="08d27-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="08d27-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="08d27-1299">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="08d27-1299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="08d27-1300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="08d27-1300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="08d27-1301">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="08d27-1301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="08d27-1302">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="08d27-1302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08d27-1303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08d27-1303">Az.FrontDoor</span></span>
* <span data-ttu-id="08d27-1304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="08d27-1304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="08d27-1305">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="08d27-1305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="08d27-1306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="08d27-1306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="08d27-1307">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="08d27-1307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-1308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-1308">Az.Network</span></span>
* <span data-ttu-id="08d27-1309">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="08d27-1309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="08d27-1310">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1310">New cmdlets</span></span>
        - <span data-ttu-id="08d27-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="08d27-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="08d27-1312">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="08d27-1312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="08d27-1313">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1313">New cmdlets</span></span>
        - <span data-ttu-id="08d27-1314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="08d27-1314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="08d27-1315">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="08d27-1315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="08d27-1316">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1316">New cmdlets</span></span>
        - <span data-ttu-id="08d27-1317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="08d27-1317">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="08d27-1318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="08d27-1318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="08d27-1319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="08d27-1319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="08d27-1320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-1320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="08d27-1321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-1321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="08d27-1322">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="08d27-1322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="08d27-1323">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1323">New cmdlets</span></span>
        - <span data-ttu-id="08d27-1324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="08d27-1324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="08d27-1325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="08d27-1325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="08d27-1326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="08d27-1326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="08d27-1327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="08d27-1327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="08d27-1328">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="08d27-1328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="08d27-1329">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="08d27-1330">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="08d27-1331">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="08d27-1332">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="08d27-1333">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="08d27-1334">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="08d27-1335">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="08d27-1336">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="08d27-1337">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="08d27-1338">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="08d27-1339">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="08d27-1340">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="08d27-1341">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="08d27-1342">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-1342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="08d27-1343">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="08d27-1344">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="08d27-1345">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="08d27-1345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="08d27-1346">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="08d27-1346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="08d27-1347">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="08d27-1348">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="08d27-1349">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="08d27-1350">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08d27-1351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-1351">Az.OperationalInsights</span></span>
* <span data-ttu-id="08d27-1352">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1353">Az.Resources</span></span>
* <span data-ttu-id="08d27-1354">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="08d27-1354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="08d27-1355">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="08d27-1356">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="08d27-1357">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08d27-1358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d27-1358">Az.ServiceFabric</span></span>
* <span data-ttu-id="08d27-1359">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1360">Az.Sql</span></span>
* <span data-ttu-id="08d27-1361">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="08d27-1362">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="08d27-1363">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="08d27-1364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="08d27-1364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="08d27-1365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="08d27-1365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="08d27-1366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="08d27-1366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="08d27-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="08d27-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="08d27-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="08d27-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-1369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-1369">Az.Storage</span></span>
* <span data-ttu-id="08d27-1370">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="08d27-1370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="08d27-1371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-1371">New-AzStorageAccount</span></span>
* <span data-ttu-id="08d27-1372">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="08d27-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="08d27-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-1374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-1374">Az.Websites</span></span>
* <span data-ttu-id="08d27-1375">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="08d27-1375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="08d27-1376">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="08d27-1376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="08d27-1377">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="08d27-1378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08d27-1378">Az.Cdn</span></span>
* <span data-ttu-id="08d27-1379">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1380">Az.Compute</span></span>
* <span data-ttu-id="08d27-1381">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="08d27-1382">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="08d27-1382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08d27-1383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08d27-1383">Az.EventHub</span></span>
* <span data-ttu-id="08d27-1384">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="08d27-1384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="08d27-1385">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="08d27-1385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-1386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-1386">Az.Network</span></span>
* <span data-ttu-id="08d27-1387">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="08d27-1388">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08d27-1389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-1389">Az.PolicyInsights</span></span>
* <span data-ttu-id="08d27-1390">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-1391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1391">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-1392">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08d27-1393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08d27-1393">Az.ServiceBus</span></span>
* <span data-ttu-id="08d27-1394">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="08d27-1394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08d27-1395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d27-1395">Az.ServiceFabric</span></span>
* <span data-ttu-id="08d27-1396">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="08d27-1397">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1398">Az.Sql</span></span>
* <span data-ttu-id="08d27-1399">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="08d27-1400">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-1400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="08d27-1401">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-1401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="08d27-1402">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-1403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-1403">Az.Websites</span></span>
* <span data-ttu-id="08d27-1404">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="08d27-1405">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="08d27-1406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08d27-1406">Az.ApiManagement</span></span>
* <span data-ttu-id="08d27-1407">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-1407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="08d27-1408">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="08d27-1408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="08d27-1409">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="08d27-1409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="08d27-1410">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="08d27-1410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="08d27-1411">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="08d27-1411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="08d27-1412">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="08d27-1412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="08d27-1413">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="08d27-1413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="08d27-1414">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="08d27-1414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="08d27-1415">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-1415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="08d27-1416">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="08d27-1416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="08d27-1417">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="08d27-1417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="08d27-1418">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="08d27-1418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="08d27-1419">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="08d27-1419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="08d27-1420">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-1420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="08d27-1421">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="08d27-1421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="08d27-1422">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="08d27-1422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="08d27-1423">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="08d27-1423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="08d27-1424">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="08d27-1424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="08d27-1425">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="08d27-1425">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="08d27-1426">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="08d27-1426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="08d27-1427">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-1427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="08d27-1428">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="08d27-1428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="08d27-1429">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="08d27-1429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="08d27-1430">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="08d27-1431">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="08d27-1432">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="08d27-1433">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="08d27-1433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="08d27-1434">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="08d27-1434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="08d27-1435">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="08d27-1436">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="08d27-1437">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1437">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="08d27-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="08d27-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="08d27-1439">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="08d27-1440">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="08d27-1441">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="08d27-1441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="08d27-1442">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="08d27-1442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="08d27-1443">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="08d27-1443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="08d27-1444">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="08d27-1445">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="08d27-1446">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1446">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="08d27-1447">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="08d27-1447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="08d27-1448">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="08d27-1448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="08d27-1449">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="08d27-1449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="08d27-1450">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="08d27-1450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="08d27-1451">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="08d27-1452">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="08d27-1452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="08d27-1453">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="08d27-1453">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="08d27-1454">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="08d27-1454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="08d27-1455">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="08d27-1456">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="08d27-1456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="08d27-1457">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="08d27-1457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="08d27-1458">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="08d27-1458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="08d27-1459">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="08d27-1459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="08d27-1460">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="08d27-1461">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="08d27-1461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="08d27-1462">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="08d27-1462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="08d27-1463">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="08d27-1464">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="08d27-1464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="08d27-1465">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="08d27-1465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="08d27-1466">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="08d27-1467">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="08d27-1468">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="08d27-1468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="08d27-1469">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="08d27-1469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="08d27-1470">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="08d27-1471">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="08d27-1472">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="08d27-1472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="08d27-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="08d27-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="08d27-1474">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="08d27-1474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="08d27-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="08d27-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="08d27-1476">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="08d27-1476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="08d27-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="08d27-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="08d27-1478">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="08d27-1478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="08d27-1479">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="08d27-1479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="08d27-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="08d27-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="08d27-1481">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="08d27-1481">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="08d27-1482">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="08d27-1482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="08d27-1483">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="08d27-1483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d27-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d27-1484">Az.Automation</span></span>
* <span data-ttu-id="08d27-1485">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="08d27-1486">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="08d27-1487">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="08d27-1488">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="08d27-1489">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="08d27-1490">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="08d27-1491">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-1491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1492">Az.Compute</span></span>
* <span data-ttu-id="08d27-1493">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="08d27-1494">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="08d27-1494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-1495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-1495">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-1496">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d27-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-1497">Az.Monitor</span></span>
* <span data-ttu-id="08d27-1498">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-1499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-1499">Az.Network</span></span>
* <span data-ttu-id="08d27-1500">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="08d27-1501">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="08d27-1501">Updated cmdlet:</span></span>
        - <span data-ttu-id="08d27-1502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="08d27-1502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="08d27-1503">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1504">Az.Resources</span></span>
* <span data-ttu-id="08d27-1505">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1506">Az.Sql</span></span>
* <span data-ttu-id="08d27-1507">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="08d27-1507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="08d27-1508">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-1509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1509">Az.Accounts</span></span>
* <span data-ttu-id="08d27-1510">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="08d27-1510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08d27-1511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1511">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d27-1512">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="08d27-1512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="08d27-1513">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="08d27-1513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1514">Az.Compute</span></span>
* <span data-ttu-id="08d27-1515">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="08d27-1515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="08d27-1516">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="08d27-1516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="08d27-1517">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-1517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="08d27-1518">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="08d27-1519">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="08d27-1519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="08d27-1520">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="08d27-1521">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="08d27-1521">Breaking changes</span></span>
    - <span data-ttu-id="08d27-1522">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="08d27-1523">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="08d27-1524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="08d27-1524">Az.DeploymentManager</span></span>
* <span data-ttu-id="08d27-1525">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="08d27-1525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="08d27-1526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="08d27-1526">Az.Dns</span></span>
* <span data-ttu-id="08d27-1527">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="08d27-1527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="08d27-1528">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="08d27-1528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="08d27-1529">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="08d27-1529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08d27-1530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08d27-1530">Az.FrontDoor</span></span>
* <span data-ttu-id="08d27-1531">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="08d27-1531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="08d27-1532">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="08d27-1532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="08d27-1533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08d27-1533">Az.HDInsight</span></span>
* <span data-ttu-id="08d27-1534">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="08d27-1534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="08d27-1535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="08d27-1535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="08d27-1536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="08d27-1536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="08d27-1537">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="08d27-1538">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="08d27-1538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="08d27-1539">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="08d27-1539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="08d27-1540">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="08d27-1540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d27-1541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-1541">Az.Monitor</span></span>
* <span data-ttu-id="08d27-1542">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="08d27-1543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="08d27-1543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="08d27-1544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="08d27-1544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="08d27-1545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="08d27-1545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="08d27-1546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="08d27-1546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="08d27-1547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="08d27-1547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="08d27-1548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="08d27-1548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="08d27-1549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08d27-1549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08d27-1550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08d27-1550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08d27-1551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08d27-1551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08d27-1552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08d27-1552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08d27-1553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08d27-1553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08d27-1554">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="08d27-1554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="08d27-1555">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-1556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-1556">Az.Network</span></span>
* <span data-ttu-id="08d27-1557">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="08d27-1557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="08d27-1558">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1558">New cmdlets</span></span>
        - <span data-ttu-id="08d27-1559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="08d27-1559">New-AzNatGateway</span></span>
        - <span data-ttu-id="08d27-1560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="08d27-1560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="08d27-1561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="08d27-1561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="08d27-1562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="08d27-1562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="08d27-1563">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1563">Updated cmdlets</span></span>
        - <span data-ttu-id="08d27-1564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="08d27-1564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="08d27-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="08d27-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="08d27-1566">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="08d27-1566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="08d27-1567">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="08d27-1568">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08d27-1569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-1569">Az.PolicyInsights</span></span>
* <span data-ttu-id="08d27-1570">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-1570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="08d27-1571">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="08d27-1571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="08d27-1572">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="08d27-1572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-1573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1573">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-1574">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-1574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="08d27-1575">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="08d27-1575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="08d27-1576">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="08d27-1576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="08d27-1577">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="08d27-1577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="08d27-1578">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="08d27-1578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="08d27-1579">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="08d27-1579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="08d27-1580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="08d27-1580">Az.Relay</span></span>
* <span data-ttu-id="08d27-1581">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="08d27-1581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08d27-1582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08d27-1582">Az.ServiceBus</span></span>
* <span data-ttu-id="08d27-1583">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-1584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-1584">Az.Storage</span></span>
* <span data-ttu-id="08d27-1585">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="08d27-1585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="08d27-1586">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="08d27-1586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="08d27-1587">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="08d27-1587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="08d27-1588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-1588">New-AzStorageAccount</span></span>
* <span data-ttu-id="08d27-1589">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="08d27-1589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="08d27-1590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-1590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="08d27-1591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-1591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="08d27-1592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-1592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-1593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-1593">Az.Websites</span></span>
* <span data-ttu-id="08d27-1594">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="08d27-1594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="08d27-1595">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="08d27-1596">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08d27-1597">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="08d27-1597">Highlights since the last major release</span></span>
* <span data-ttu-id="08d27-1598">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-1598">General availability of `Az` module</span></span>
* <span data-ttu-id="08d27-1599">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="08d27-1599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="08d27-1600">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="08d27-1600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="08d27-1601">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="08d27-1602">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="08d27-1603">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="08d27-1604">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08d27-1605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1605">Az.Accounts</span></span>
* <span data-ttu-id="08d27-1606">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08d27-1607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08d27-1607">Az.Batch</span></span>
* <span data-ttu-id="08d27-1608">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08d27-1609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08d27-1609">Az.Cdn</span></span>
* <span data-ttu-id="08d27-1610">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08d27-1611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1611">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d27-1612">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1613">Az.Compute</span></span>
* <span data-ttu-id="08d27-1614">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="08d27-1615">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08d27-1616">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-1617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-1617">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-1618">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-1619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-1619">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-1620">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="08d27-1621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="08d27-1621">Az.EventGrid</span></span>
* <span data-ttu-id="08d27-1622">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08d27-1623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08d27-1623">Az.EventHub</span></span>
* <span data-ttu-id="08d27-1624">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1624">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08d27-1625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08d27-1625">Az.HDInsight</span></span>
* <span data-ttu-id="08d27-1626">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d27-1627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d27-1627">Az.IotHub</span></span>
* <span data-ttu-id="08d27-1628">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d27-1629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d27-1629">Az.KeyVault</span></span>
* <span data-ttu-id="08d27-1630">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08d27-1631">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="08d27-1632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="08d27-1632">Az.MachineLearning</span></span>
* <span data-ttu-id="08d27-1633">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="08d27-1634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="08d27-1634">Az.Media</span></span>
* <span data-ttu-id="08d27-1635">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d27-1636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-1636">Az.Monitor</span></span>
  * <span data-ttu-id="08d27-1637">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="08d27-1638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="08d27-1638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="08d27-1639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="08d27-1639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="08d27-1640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="08d27-1640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="08d27-1641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="08d27-1641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="08d27-1642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="08d27-1642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="08d27-1643">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-1644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-1644">Az.Network</span></span>
* <span data-ttu-id="08d27-1645">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08d27-1646">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="08d27-1647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="08d27-1647">Az.NotificationHubs</span></span>
* <span data-ttu-id="08d27-1648">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08d27-1649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-1649">Az.OperationalInsights</span></span>
* <span data-ttu-id="08d27-1650">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="08d27-1651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="08d27-1651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="08d27-1652">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-1653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1653">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-1654">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08d27-1655">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="08d27-1655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="08d27-1656">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="08d27-1657">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="08d27-1658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="08d27-1658">Az.RedisCache</span></span>
* <span data-ttu-id="08d27-1659">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1660">Az.Resources</span></span>
* <span data-ttu-id="08d27-1661">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1662">Az.Sql</span></span>
* <span data-ttu-id="08d27-1663">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="08d27-1664">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08d27-1665">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="08d27-1666">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="08d27-1667">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="08d27-1668">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-1668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="08d27-1669">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-1670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-1670">Az.Websites</span></span>
* <span data-ttu-id="08d27-1671">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="08d27-1672">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08d27-1673">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="08d27-1674">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="08d27-1674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="08d27-1675">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08d27-1676">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="08d27-1676">Highlights since the last major release</span></span>
* <span data-ttu-id="08d27-1677">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-1677">General availability of `Az` module</span></span>
* <span data-ttu-id="08d27-1678">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="08d27-1678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="08d27-1679">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="08d27-1679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="08d27-1680">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="08d27-1681">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="08d27-1682">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="08d27-1683">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08d27-1684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1684">Az.Accounts</span></span>
* <span data-ttu-id="08d27-1685">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="08d27-1686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1686">Az.AnalysisServices</span></span>
* <span data-ttu-id="08d27-1687">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="08d27-1687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="08d27-1688">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="08d27-1688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d27-1689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d27-1689">Az.Automation</span></span>
* <span data-ttu-id="08d27-1690">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="08d27-1691">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-1691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="08d27-1692">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="08d27-1692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1693">Az.Compute</span></span>
* <span data-ttu-id="08d27-1694">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="08d27-1695">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1695">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="08d27-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="08d27-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="08d27-1697">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-1698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-1698">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-1699">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="08d27-1700">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1701">Az.Resources</span></span>
* <span data-ttu-id="08d27-1702">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="08d27-1703">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="08d27-1704">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="08d27-1705">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="08d27-1705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="08d27-1706">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="08d27-1707">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="08d27-1707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1708">Az.Sql</span></span>
* <span data-ttu-id="08d27-1709">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-1709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-1710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-1710">Az.Storage</span></span>
* <span data-ttu-id="08d27-1711">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="08d27-1711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="08d27-1712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="08d27-1712">New-AzStorageContext</span></span>
* <span data-ttu-id="08d27-1713">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="08d27-1713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="08d27-1714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="08d27-1714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="08d27-1715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="08d27-1715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="08d27-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="08d27-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="08d27-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="08d27-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="08d27-1718">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="08d27-1718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="08d27-1719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="08d27-1719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="08d27-1720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="08d27-1720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="08d27-1721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="08d27-1721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="08d27-1722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="08d27-1722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="08d27-1723">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08d27-1724">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="08d27-1724">Highlights since the last major release</span></span>
* <span data-ttu-id="08d27-1725">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-1725">General availability of `Az` module</span></span>
* <span data-ttu-id="08d27-1726">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="08d27-1726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="08d27-1727">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="08d27-1727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="08d27-1728">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="08d27-1729">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="08d27-1730">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="08d27-1731">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d27-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d27-1732">Az.Automation</span></span>
* <span data-ttu-id="08d27-1733">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="08d27-1733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="08d27-1734">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="08d27-1734">Dynamic grouping</span></span>
    * <span data-ttu-id="08d27-1735">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="08d27-1735">Pre-Post script</span></span>
    * <span data-ttu-id="08d27-1736">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="08d27-1736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1737">Az.Compute</span></span>
* <span data-ttu-id="08d27-1738">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="08d27-1738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="08d27-1739">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d27-1740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d27-1740">Az.KeyVault</span></span>
* <span data-ttu-id="08d27-1741">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-1742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-1742">Az.Network</span></span>
* <span data-ttu-id="08d27-1743">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="08d27-1744">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-1745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1745">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-1746">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="08d27-1747">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1748">Az.Resources</span></span>
* <span data-ttu-id="08d27-1749">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="08d27-1750">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1751">Az.Sql</span></span>
* <span data-ttu-id="08d27-1752">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-1753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-1753">Az.Storage</span></span>
* <span data-ttu-id="08d27-1754">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="08d27-1754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="08d27-1755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="08d27-1755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="08d27-1756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="08d27-1756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="08d27-1757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="08d27-1757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="08d27-1758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="08d27-1758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="08d27-1759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="08d27-1759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="08d27-1760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="08d27-1760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-1761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-1761">Az.Websites</span></span>
* <span data-ttu-id="08d27-1762">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="08d27-1763">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-1764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1764">Az.Accounts</span></span>
* <span data-ttu-id="08d27-1765">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="08d27-1766">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d27-1767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d27-1767">Az.Automation</span></span>
* <span data-ttu-id="08d27-1768">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="08d27-1769">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="08d27-1770">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="08d27-1770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08d27-1771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08d27-1771">Az.Cdn</span></span>
* <span data-ttu-id="08d27-1772">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-1772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1773">Az.Compute</span></span>
* <span data-ttu-id="08d27-1774">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-1775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-1775">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-1776">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="08d27-1777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="08d27-1777">Az.LogicApp</span></span>
* <span data-ttu-id="08d27-1778">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="08d27-1778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-1779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-1779">Az.Network</span></span>
* <span data-ttu-id="08d27-1780">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-1781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1781">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-1782">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="08d27-1783">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="08d27-1783">SDK Update</span></span>
* <span data-ttu-id="08d27-1784">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-1784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="08d27-1785">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1786">Az.Resources</span></span>
* <span data-ttu-id="08d27-1787">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="08d27-1788">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="08d27-1788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="08d27-1789">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="08d27-1790">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="08d27-1790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="08d27-1791">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="08d27-1792">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="08d27-1792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1793">Az.Sql</span></span>
* <span data-ttu-id="08d27-1794">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-1794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="08d27-1795">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-1795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-1796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-1796">Az.Storage</span></span>
* <span data-ttu-id="08d27-1797">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d27-1797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="08d27-1798">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="08d27-1799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1799">Az.AnalysisServices</span></span>
* <span data-ttu-id="08d27-1800">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-1800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d27-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d27-1801">Az.Automation</span></span>
* <span data-ttu-id="08d27-1802">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="08d27-1803">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="08d27-1804">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08d27-1805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1805">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d27-1806">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1807">Az.Compute</span></span>
* <span data-ttu-id="08d27-1808">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="08d27-1809">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="08d27-1810">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="08d27-1811">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="08d27-1811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-1812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-1812">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-1813">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08d27-1814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08d27-1814">Az.EventHub</span></span>
* <span data-ttu-id="08d27-1815">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d27-1816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d27-1816">Az.KeyVault</span></span>
* <span data-ttu-id="08d27-1817">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="08d27-1818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="08d27-1818">Az.LogicApp</span></span>
* <span data-ttu-id="08d27-1819">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="08d27-1820">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="08d27-1821">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="08d27-1822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="08d27-1822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="08d27-1823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="08d27-1823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="08d27-1824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="08d27-1824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="08d27-1825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="08d27-1825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="08d27-1826">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="08d27-1826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="08d27-1827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d27-1827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="08d27-1828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d27-1828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="08d27-1829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d27-1829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="08d27-1830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d27-1830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="08d27-1831">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d27-1832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-1832">Az.Monitor</span></span>
* <span data-ttu-id="08d27-1833">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-1834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-1834">Az.Network</span></span>
* <span data-ttu-id="08d27-1835">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08d27-1836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-1836">Az.OperationalInsights</span></span>
* <span data-ttu-id="08d27-1837">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="08d27-1837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="08d27-1838">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="08d27-1839">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1840">Az.Resources</span></span>
* <span data-ttu-id="08d27-1841">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="08d27-1842">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="08d27-1843">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="08d27-1844">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1845">Az.Sql</span></span>
* <span data-ttu-id="08d27-1846">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="08d27-1847">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-1848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-1848">Az.Websites</span></span>
* <span data-ttu-id="08d27-1849">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="08d27-1850">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-1851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1851">Az.Accounts</span></span>
* <span data-ttu-id="08d27-1852">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="08d27-1852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="08d27-1853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1853">Az.AnalysisServices</span></span>
<span data-ttu-id="08d27-1854">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="08d27-1854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1855">Az.Compute</span></span>
* <span data-ttu-id="08d27-1856">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="08d27-1857">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="08d27-1858">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-1859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1859">Az.RecoveryServices</span></span>
<span data-ttu-id="08d27-1860">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="08d27-1860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1861">Az.Resources</span></span>
* <span data-ttu-id="08d27-1862">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1862">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="08d27-1863">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="08d27-1863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="08d27-1864">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="08d27-1865">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="08d27-1865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1866">Az.Sql</span></span>
* <span data-ttu-id="08d27-1867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="08d27-1867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="08d27-1868">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="08d27-1869">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="08d27-1870">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-1871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1871">Az.Accounts</span></span>
* <span data-ttu-id="08d27-1872">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="08d27-1872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="08d27-1873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1873">Az.AnalysisServices</span></span>
* <span data-ttu-id="08d27-1874">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="08d27-1874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-1875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-1875">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d27-1876">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="08d27-1876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="08d27-1877">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1878">Az.Accounts</span></span>
* <span data-ttu-id="08d27-1879">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="08d27-1880">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="08d27-1881">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="08d27-1882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="08d27-1882">Az.Aks</span></span>
* <span data-ttu-id="08d27-1883">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d27-1884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d27-1884">Az.Automation</span></span>
* <span data-ttu-id="08d27-1885">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="08d27-1886">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08d27-1887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08d27-1887">Az.Cdn</span></span>
* <span data-ttu-id="08d27-1888">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1889">Az.Compute</span></span>
* <span data-ttu-id="08d27-1890">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="08d27-1891">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="08d27-1892">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="08d27-1893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="08d27-1893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="08d27-1894">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d27-1895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d27-1895">Az.DataFactory</span></span>
* <span data-ttu-id="08d27-1896">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-1897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-1897">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-1898">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="08d27-1899">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="08d27-1899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="08d27-1900">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d27-1901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d27-1901">Az.IotHub</span></span>
* <span data-ttu-id="08d27-1902">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d27-1903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d27-1903">Az.KeyVault</span></span>
* <span data-ttu-id="08d27-1904">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-1905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-1905">Az.Network</span></span>
* <span data-ttu-id="08d27-1906">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1907">Az.Resources</span></span>
* <span data-ttu-id="08d27-1908">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="08d27-1909">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="08d27-1910">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="08d27-1911">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="08d27-1912">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="08d27-1913">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="08d27-1914">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="08d27-1914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08d27-1915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d27-1915">Az.ServiceFabric</span></span>
* <span data-ttu-id="08d27-1916">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="08d27-1916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="08d27-1917">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1917">Fix some error messages.</span></span>
* <span data-ttu-id="08d27-1918">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="08d27-1919">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="08d27-1920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="08d27-1920">Az.SignalR</span></span>
* <span data-ttu-id="08d27-1921">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1922">Az.Sql</span></span>
* <span data-ttu-id="08d27-1923">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="08d27-1924">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="08d27-1925">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="08d27-1926">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="08d27-1926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-1927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-1927">Az.Storage</span></span>
* <span data-ttu-id="08d27-1928">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="08d27-1929">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-1929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="08d27-1930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="08d27-1930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="08d27-1931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="08d27-1931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="08d27-1932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="08d27-1932">Az.TrafficManager</span></span>
* <span data-ttu-id="08d27-1933">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-1934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-1934">Az.Websites</span></span>
* <span data-ttu-id="08d27-1935">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="08d27-1936">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="08d27-1937">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="08d27-1938">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="08d27-1938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d27-1939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1939">Az.Accounts</span></span>
* <span data-ttu-id="08d27-1940">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-1940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-1941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-1941">Az.Compute</span></span>
* <span data-ttu-id="08d27-1942">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="08d27-1942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="08d27-1943">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="08d27-1944">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="08d27-1944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-1945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-1945">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-1946">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="08d27-1947">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="08d27-1948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="08d27-1948">Az.EventGrid</span></span>
* <span data-ttu-id="08d27-1949">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="08d27-1950">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="08d27-1951">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-1951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="08d27-1952">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="08d27-1952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="08d27-1953">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="08d27-1953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="08d27-1954">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="08d27-1954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="08d27-1955">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-1955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="08d27-1956">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="08d27-1956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="08d27-1957">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="08d27-1957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="08d27-1958">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="08d27-1958">Dead letter endpoint.</span></span>
* <span data-ttu-id="08d27-1959">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="08d27-1960">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-1960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d27-1961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d27-1961">Az.IotHub</span></span>
* <span data-ttu-id="08d27-1962">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="08d27-1963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="08d27-1963">Az.LogicApp</span></span>
* <span data-ttu-id="08d27-1964">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="08d27-1964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-1965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-1965">Az.Resources</span></span>
* <span data-ttu-id="08d27-1966">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="08d27-1967">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="08d27-1967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="08d27-1968">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="08d27-1969">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="08d27-1970">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="08d27-1971">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="08d27-1971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="08d27-1972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="08d27-1972">Az.SignalR</span></span>
* <span data-ttu-id="08d27-1973">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="08d27-1973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-1974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-1974">Az.Sql</span></span>
* <span data-ttu-id="08d27-1975">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="08d27-1975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d27-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-1976">Az.Storage</span></span>
* <span data-ttu-id="08d27-1977">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="08d27-1977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="08d27-1978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="08d27-1978">New-AzStorageContext</span></span>
* <span data-ttu-id="08d27-1979">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="08d27-1980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="08d27-1980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-1981">Az.Websites</span></span>
* <span data-ttu-id="08d27-1982">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="08d27-1983">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="08d27-1983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="08d27-1984">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="08d27-1984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="08d27-1985">Genel</span><span class="sxs-lookup"><span data-stu-id="08d27-1985">General</span></span>

- <span data-ttu-id="08d27-1986">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-1986">General Availability of Az Module</span></span>
- <span data-ttu-id="08d27-1987">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="08d27-1987">Online help for each module</span></span>
- <span data-ttu-id="08d27-1988">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="08d27-1988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="08d27-1989">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-1989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="08d27-1990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d27-1990">Az.Accounts</span></span>
- <span data-ttu-id="08d27-1991">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="08d27-1991">Changed from Az.Profile</span></span>
- <span data-ttu-id="08d27-1992">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-1992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="08d27-1993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08d27-1993">Az.ApiManagement</span></span>
- <span data-ttu-id="08d27-1994">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="08d27-1994">Fixes for #7002</span></span>
- <span data-ttu-id="08d27-1995">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-1995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="08d27-1996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08d27-1996">Az.Batch</span></span>
- <span data-ttu-id="08d27-1997">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-1997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="08d27-1998">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="08d27-1998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="08d27-1999">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-1999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="08d27-2000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="08d27-2000">Az.Billing</span></span>
- <span data-ttu-id="08d27-2001">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-2001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="08d27-2002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="08d27-2002">Az.CognitivServices</span></span>
- <span data-ttu-id="08d27-2003">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="08d27-2004">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-2004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="08d27-2005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="08d27-2005">Az.ContainerInstance</span></span>
- <span data-ttu-id="08d27-2006">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="08d27-2007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="08d27-2007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="08d27-2008">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-2008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="08d27-2009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-2009">Az.DataLakeStore</span></span>
- <span data-ttu-id="08d27-2010">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-2010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="08d27-2011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d27-2011">Az.Monitor</span></span>
- <span data-ttu-id="08d27-2012">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-2012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="08d27-2013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d27-2013">Az.KeyVault</span></span>
- <span data-ttu-id="08d27-2014">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-2014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="08d27-2015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="08d27-2015">Az.MachineLearning</span></span>
- <span data-ttu-id="08d27-2016">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="08d27-2017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="08d27-2017">Az.Media</span></span>
- <span data-ttu-id="08d27-2018">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="08d27-2018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="08d27-2019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-2019">Az.Network</span></span>
<span data-ttu-id="08d27-2020">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="08d27-2021">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="08d27-2021">New cmdlets added:</span></span>
        - <span data-ttu-id="08d27-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d27-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08d27-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d27-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08d27-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d27-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08d27-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d27-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08d27-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d27-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08d27-2027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="08d27-2027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="08d27-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="08d27-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="08d27-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d27-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="08d27-2030">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="08d27-2031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08d27-2031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="08d27-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="08d27-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="08d27-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="08d27-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="08d27-2034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-2034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="08d27-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="08d27-2036">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="08d27-2037">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="08d27-2038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="08d27-2038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="08d27-2039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="08d27-2039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="08d27-2040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="08d27-2040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="08d27-2041">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="08d27-2042">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-2042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="08d27-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-2043">Az.OperationalInsights</span></span>
- <span data-ttu-id="08d27-2044">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-2044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="08d27-2045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="08d27-2045">Az.Profile</span></span>
- <span data-ttu-id="08d27-2046">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-2047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-2047">Az.RecoveryServices</span></span>
- <span data-ttu-id="08d27-2048">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-2048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="08d27-2049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-2049">Az.Resources</span></span>
- <span data-ttu-id="08d27-2050">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-2050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="08d27-2051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d27-2051">Az.ServiceFabric</span></span>
- <span data-ttu-id="08d27-2052">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="08d27-2052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="08d27-2053">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-2053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="08d27-2054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="08d27-2054">Az.SIgnalR</span></span>
- <span data-ttu-id="08d27-2055">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="08d27-2055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="08d27-2056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-2056">Az.Sql</span></span>
- <span data-ttu-id="08d27-2057">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="08d27-2058">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="08d27-2059">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-2059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="08d27-2060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-2060">Az.Storage</span></span>
- <span data-ttu-id="08d27-2061">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-2061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="08d27-2062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-2062">Az.Websites</span></span>
- <span data-ttu-id="08d27-2063">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d27-2063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="08d27-2064">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="08d27-2064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="08d27-2065">Genel</span><span class="sxs-lookup"><span data-stu-id="08d27-2065">General</span></span>

* <span data-ttu-id="08d27-2066">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="08d27-2066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="08d27-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-2067">Az.Compute</span></span>

* <span data-ttu-id="08d27-2068">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="08d27-2069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-2069">Az.DataLakeStore</span></span>

* <span data-ttu-id="08d27-2070">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="08d27-2071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08d27-2071">Az.FrontDoor</span></span>

* <span data-ttu-id="08d27-2072">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2072">Fixed some broken links</span></span>
    - <span data-ttu-id="08d27-2073">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="08d27-2074">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="08d27-2075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d27-2075">Az.RecoveryServices</span></span>

* <span data-ttu-id="08d27-2076">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="08d27-2077">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="08d27-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-2078">Az.Resources</span></span>

* <span data-ttu-id="08d27-2079">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="08d27-2079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="08d27-2080">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="08d27-2081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-2081">Az.Sql</span></span>

* <span data-ttu-id="08d27-2082">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="08d27-2082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="08d27-2083">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="08d27-2084">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="08d27-2085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d27-2085">Az.Storage</span></span>

* <span data-ttu-id="08d27-2086">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="08d27-2087">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="08d27-2088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="08d27-2088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="08d27-2089">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2089">Support Static Website configuration</span></span>
    - <span data-ttu-id="08d27-2090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="08d27-2090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="08d27-2091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="08d27-2091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="08d27-2092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-2092">Az.Websites</span></span>

* <span data-ttu-id="08d27-2093">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08d27-2093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="08d27-2094">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="08d27-2095">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="08d27-2095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="08d27-2096">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="08d27-2096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="08d27-2097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08d27-2097">Az.ApiManagement</span></span>
* <span data-ttu-id="08d27-2098">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="08d27-2098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="08d27-2099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d27-2099">Az.Automation</span></span>
* <span data-ttu-id="08d27-2100">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="08d27-2100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="08d27-2101">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="08d27-2102">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="08d27-2103">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="08d27-2104">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="08d27-2105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-2105">Az.Compute</span></span>
* <span data-ttu-id="08d27-2106">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="08d27-2107">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="08d27-2107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="08d27-2108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="08d27-2108">Az.ContainerInstance</span></span>
* <span data-ttu-id="08d27-2109">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="08d27-2109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="08d27-2110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="08d27-2110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="08d27-2111">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="08d27-2112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-2112">Az.Network</span></span>
* <span data-ttu-id="08d27-2113">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="08d27-2114">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="08d27-2115">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="08d27-2116">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="08d27-2117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="08d27-2117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="08d27-2118">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="08d27-2119">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="08d27-2119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="08d27-2120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="08d27-2120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="08d27-2121">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="08d27-2122">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="08d27-2122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="08d27-2123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="08d27-2123">Az.Relay</span></span>
* <span data-ttu-id="08d27-2124">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="08d27-2125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-2125">Az.Resources</span></span>
* <span data-ttu-id="08d27-2126">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="08d27-2127">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="08d27-2128">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="08d27-2128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="08d27-2129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d27-2129">Az.ServiceFabric</span></span>
* <span data-ttu-id="08d27-2130">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="08d27-2131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-2131">Az.Sql</span></span>
* <span data-ttu-id="08d27-2132">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="08d27-2133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08d27-2133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="08d27-2134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08d27-2134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="08d27-2135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08d27-2135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="08d27-2136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08d27-2136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="08d27-2137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="08d27-2137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="08d27-2138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="08d27-2138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="08d27-2139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="08d27-2139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="08d27-2140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="08d27-2140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="08d27-2141">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="08d27-2142">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="08d27-2143">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="08d27-2144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="08d27-2144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="08d27-2145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="08d27-2145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="08d27-2146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="08d27-2146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="08d27-2147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="08d27-2147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="08d27-2148">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="08d27-2149">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="08d27-2149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="08d27-2150">Genel</span><span class="sxs-lookup"><span data-stu-id="08d27-2150">General</span></span>
* <span data-ttu-id="08d27-2151">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="08d27-2151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="08d27-2152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="08d27-2152">Az.Profile</span></span>
* <span data-ttu-id="08d27-2153">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="08d27-2154">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="08d27-2155">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="08d27-2156">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="08d27-2157">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="08d27-2158">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="08d27-2159">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="08d27-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d27-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d27-2161">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-2162">Az.Compute</span></span>
* <span data-ttu-id="08d27-2163">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="08d27-2164">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="08d27-2164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="08d27-2165">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-2166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-2166">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-2167">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="08d27-2168">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="08d27-2169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="08d27-2169">Az.Insights</span></span>
* <span data-ttu-id="08d27-2170">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="08d27-2171">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="08d27-2171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="08d27-2172">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="08d27-2173">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="08d27-2173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-2174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-2174">Az.Network</span></span>
* <span data-ttu-id="08d27-2175">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="08d27-2175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="08d27-2176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="08d27-2176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="08d27-2177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="08d27-2177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="08d27-2178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="08d27-2178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="08d27-2179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="08d27-2179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="08d27-2180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="08d27-2180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="08d27-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="08d27-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08d27-2182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08d27-2182">Az.PolicyInsights</span></span>
* <span data-ttu-id="08d27-2183">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-2184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-2184">Az.Resources</span></span>
* <span data-ttu-id="08d27-2185">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="08d27-2185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="08d27-2186">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="08d27-2186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08d27-2187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08d27-2187">Az.ServiceBus</span></span>
* <span data-ttu-id="08d27-2188">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08d27-2189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d27-2189">Az.ServiceFabric</span></span>
* <span data-ttu-id="08d27-2190">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="08d27-2191">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="08d27-2192">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="08d27-2192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="08d27-2193">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="08d27-2193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="08d27-2194">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="08d27-2195">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="08d27-2195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="08d27-2196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="08d27-2196">Az.Profile</span></span>
* <span data-ttu-id="08d27-2197">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="08d27-2197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="08d27-2198">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-2199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-2199">Az.Compute</span></span>
* <span data-ttu-id="08d27-2200">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="08d27-2201">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d27-2202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d27-2202">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d27-2203">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="08d27-2203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="08d27-2204">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="08d27-2204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="08d27-2205">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="08d27-2205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="08d27-2206">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="08d27-2206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="08d27-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="08d27-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-2208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-2208">Az.Network</span></span>
* <span data-ttu-id="08d27-2209">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-2209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="08d27-2210">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-2211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-2211">Az.Resources</span></span>
* <span data-ttu-id="08d27-2212">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="08d27-2213">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="08d27-2213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="08d27-2214">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="08d27-2214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="08d27-2215">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="08d27-2215">Azure.Storage</span></span>
* <span data-ttu-id="08d27-2216">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="08d27-2216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="08d27-2217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="08d27-2217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="08d27-2218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="08d27-2218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="08d27-2219">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="08d27-2219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="08d27-2220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="08d27-2220">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08d27-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d27-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d27-2222">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="08d27-2222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d27-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d27-2223">Az.Compute</span></span>
* <span data-ttu-id="08d27-2224">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="08d27-2225">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="08d27-2226">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="08d27-2227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="08d27-2227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="08d27-2228">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d27-2229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d27-2229">Az.Network</span></span>
* <span data-ttu-id="08d27-2230">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="08d27-2230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="08d27-2231">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2231">new cmdlets added</span></span>
    - <span data-ttu-id="08d27-2232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="08d27-2232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="08d27-2233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="08d27-2233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="08d27-2234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="08d27-2234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="08d27-2235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="08d27-2235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="08d27-2236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-2236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="08d27-2237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="08d27-2237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="08d27-2238">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="08d27-2239">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="08d27-2240">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="08d27-2241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="08d27-2241">Az.RedisCache</span></span>
* <span data-ttu-id="08d27-2242">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="08d27-2242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="08d27-2243">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d27-2244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d27-2244">Az.Resources</span></span>
* <span data-ttu-id="08d27-2245">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="08d27-2245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="08d27-2246">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d27-2247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d27-2247">Az.Sql</span></span>
* <span data-ttu-id="08d27-2248">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="08d27-2248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d27-2249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d27-2249">Az.Websites</span></span>
* <span data-ttu-id="08d27-2250">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="08d27-2250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="08d27-2251">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="08d27-2251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="08d27-2252">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="08d27-2252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="08d27-2253">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="08d27-2253">Initial Release</span></span>
