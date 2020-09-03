---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: c0f322fb0905bae96f89f41949bcc43ad81056c7
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239987"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="0448c-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="0448c-103">Azure PowerShell release notes</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="0448c-104">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="0448c-104">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="0448c-105">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0448c-105">Highlights since the last release</span></span>
* <span data-ttu-id="0448c-106">Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="0448c-106">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0448c-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-107">Az.Accounts</span></span>
* <span data-ttu-id="0448c-108">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="0448c-108">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0448c-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0448c-109">Az.ApiManagement</span></span>
* <span data-ttu-id="0448c-110">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-110">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="0448c-111">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-111">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0448c-112">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0448c-112">Az.Cdn</span></span>
* <span data-ttu-id="0448c-113">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-113">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0448c-114">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0448c-114">Az.CognitiveServices</span></span>
* <span data-ttu-id="0448c-115">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="0448c-115">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-116">Az.Compute</span></span>
* <span data-ttu-id="0448c-117">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-117">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="0448c-118">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-118">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0448c-119">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0448c-119">Az.IotHub</span></span>
* <span data-ttu-id="0448c-120">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0448c-120">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="0448c-121">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="0448c-121">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="0448c-122">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="0448c-122">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="0448c-123">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-123">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="0448c-124">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0448c-124">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="0448c-125">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="0448c-125">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="0448c-126">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="0448c-126">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="0448c-127">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="0448c-127">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="0448c-128">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0448c-128">New cmdlets are:</span></span>
    - <span data-ttu-id="0448c-129">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="0448c-129">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="0448c-130">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="0448c-130">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="0448c-131">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="0448c-131">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="0448c-132">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="0448c-132">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="0448c-133">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-133">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0448c-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0448c-134">Az.KeyVault</span></span>
* <span data-ttu-id="0448c-135">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-135">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="0448c-136">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="0448c-136">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="0448c-137">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="0448c-137">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="0448c-138">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-138">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="0448c-139">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="0448c-139">Az.Maintenance</span></span>
* <span data-ttu-id="0448c-140">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="0448c-140">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0448c-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-141">Az.Monitor</span></span>
* <span data-ttu-id="0448c-142">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-142">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="0448c-143">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="0448c-143">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="0448c-144">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="0448c-144">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="0448c-145">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="0448c-145">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="0448c-146">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="0448c-146">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="0448c-147">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="0448c-147">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="0448c-148">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="0448c-148">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="0448c-149">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="0448c-149">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-150">Az.Network</span></span>
* <span data-ttu-id="0448c-151">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-151">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="0448c-152">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="0448c-152">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="0448c-153">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="0448c-153">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="0448c-154">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="0448c-154">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="0448c-155">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="0448c-155">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="0448c-156">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-156">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="0448c-157">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="0448c-157">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="0448c-158">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="0448c-158">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="0448c-159">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-159">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="0448c-160">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-160">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="0448c-161">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="0448c-161">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="0448c-162">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-162">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="0448c-163">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-163">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="0448c-164">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-164">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="0448c-165">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-165">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="0448c-166">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-166">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0448c-167">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-167">Az.PolicyInsights</span></span>
* <span data-ttu-id="0448c-168">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-168">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="0448c-169">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-169">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0448c-170">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0448c-170">Az.ServiceFabric</span></span>
* <span data-ttu-id="0448c-171">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-171">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-172">Az.Sql</span></span>
* <span data-ttu-id="0448c-173">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-173">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="0448c-174">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-174">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-175">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-175">Az.Storage</span></span>
* <span data-ttu-id="0448c-176">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-176">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="0448c-177">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-177">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="0448c-178">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0448c-178">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="0448c-179">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0448c-179">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="0448c-180">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-180">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="0448c-181">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="0448c-181">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="0448c-182">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="0448c-182">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="0448c-183">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="0448c-183">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="0448c-184">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="0448c-184">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="0448c-185">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="0448c-185">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="0448c-186">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="0448c-186">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="0448c-187">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="0448c-187">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="0448c-188">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="0448c-188">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="0448c-189">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="0448c-189">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="0448c-190">Genel</span><span class="sxs-lookup"><span data-stu-id="0448c-190">General</span></span>
* <span data-ttu-id="0448c-191">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0448c-191">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="0448c-192">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="0448c-192">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="0448c-193">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0448c-193">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="0448c-194">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="0448c-194">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="0448c-195">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0448c-195">Az.Billing</span></span>
  - <span data-ttu-id="0448c-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-196">Az.Compute</span></span>
  - <span data-ttu-id="0448c-197">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0448c-197">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="0448c-198">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0448c-198">Az.EventHub</span></span>
  - <span data-ttu-id="0448c-199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0448c-199">Az.IotHub</span></span>
  - <span data-ttu-id="0448c-200">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0448c-200">Az.KeyVault</span></span>
  - <span data-ttu-id="0448c-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-201">Az.Monitor</span></span>
  - <span data-ttu-id="0448c-202">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-202">Az.Network</span></span>
  - <span data-ttu-id="0448c-203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-203">Az.Resources</span></span>
  - <span data-ttu-id="0448c-204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-204">Az.Storage</span></span>
  - <span data-ttu-id="0448c-205">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-205">Az.Websites</span></span>
* <span data-ttu-id="0448c-206">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-206">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="0448c-207">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="0448c-207">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="0448c-208">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](https://aka.ms/InstallASHPowerShell) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="0448c-208">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="0448c-209">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="0448c-209">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0448c-210">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-210">Az.Accounts</span></span>
* <span data-ttu-id="0448c-211">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="0448c-211">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-212">Az.Compute</span></span>
* <span data-ttu-id="0448c-213">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-213">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="0448c-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="0448c-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="0448c-215">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-215">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="0448c-216">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-216">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="0448c-217">[#11354]</span><span class="sxs-lookup"><span data-stu-id="0448c-217">[#11354]</span></span>
* <span data-ttu-id="0448c-218">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-218">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="0448c-219">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="0448c-219">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="0448c-220">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="0448c-220">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="0448c-221">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="0448c-221">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="0448c-222">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="0448c-222">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="0448c-223">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-223">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="0448c-224">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-224">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="0448c-225">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-225">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="0448c-226">[#11257]</span><span class="sxs-lookup"><span data-stu-id="0448c-226">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-227">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-228">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-228">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="0448c-229">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-229">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-230">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-231">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-231">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="0448c-232">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-232">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0448c-233">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0448c-233">Az.HDInsight</span></span>
* <span data-ttu-id="0448c-234">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-234">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0448c-235">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0448c-235">Az.IotHub</span></span>
* <span data-ttu-id="0448c-236">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-236">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="0448c-237">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0448c-237">New Cmdlets are:</span></span>
    - <span data-ttu-id="0448c-238">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="0448c-238">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="0448c-239">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="0448c-239">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0448c-240">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0448c-240">Az.KeyVault</span></span>
* <span data-ttu-id="0448c-241">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-241">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0448c-242">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-242">Az.Monitor</span></span>
* <span data-ttu-id="0448c-243">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-243">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-244">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-244">Az.Network</span></span>
* <span data-ttu-id="0448c-245">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-245">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="0448c-246">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="0448c-246">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="0448c-247">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="0448c-247">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="0448c-248">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="0448c-248">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="0448c-249">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="0448c-249">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="0448c-250">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-250">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0448c-251">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-251">Az.PolicyInsights</span></span>
* <span data-ttu-id="0448c-252">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-252">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-254">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-254">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="0448c-255">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-255">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="0448c-256">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-256">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="0448c-257">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-257">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="0448c-258">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-258">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="0448c-259">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-259">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-260">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-260">Az.Resources</span></span>
* <span data-ttu-id="0448c-261">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="0448c-261">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="0448c-262">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-262">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="0448c-263">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-263">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="0448c-264">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-264">Added example.</span></span>
* <span data-ttu-id="0448c-265">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="0448c-265">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="0448c-266">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="0448c-266">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-267">Az.Sql</span></span>
* <span data-ttu-id="0448c-268">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-268">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="0448c-269">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-269">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="0448c-270">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-270">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="0448c-271">Az.Support</span><span class="sxs-lookup"><span data-stu-id="0448c-271">Az.Support</span></span>
* <span data-ttu-id="0448c-272">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-272">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-273">Az.Websites</span></span>
* <span data-ttu-id="0448c-274">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-274">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="0448c-275">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="0448c-275">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="0448c-276">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="0448c-276">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="0448c-277">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="0448c-277">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="0448c-278">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="0448c-278">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="0448c-279">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="0448c-279">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0448c-280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-280">Az.Accounts</span></span>
* <span data-ttu-id="0448c-281">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="0448c-281">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="0448c-282">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="0448c-282">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="0448c-283">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-283">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0448c-284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0448c-284">Az.ApiManagement</span></span>
* <span data-ttu-id="0448c-285">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="0448c-285">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="0448c-286">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="0448c-286">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="0448c-287">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-287">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="0448c-288">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="0448c-288">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-289">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-289">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-290">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-290">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0448c-291">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0448c-291">Az.IotHub</span></span>
* <span data-ttu-id="0448c-292">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-292">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="0448c-293">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0448c-293">New Cmdlets are:</span></span>
    - <span data-ttu-id="0448c-294">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0448c-294">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0448c-295">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0448c-295">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0448c-296">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0448c-296">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0448c-297">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0448c-297">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="0448c-298">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-298">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="0448c-299">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0448c-299">New Cmdlets are:</span></span>
    - <span data-ttu-id="0448c-300">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0448c-300">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="0448c-301">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0448c-301">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="0448c-302">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0448c-302">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="0448c-303">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0448c-303">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="0448c-304">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-304">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="0448c-305">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-305">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="0448c-306">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-306">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="0448c-307">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0448c-307">New Cmdlets are:</span></span>
    - <span data-ttu-id="0448c-308">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="0448c-308">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="0448c-309">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="0448c-309">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="0448c-310">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-310">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0448c-311">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-311">Az.Monitor</span></span>
* <span data-ttu-id="0448c-312">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="0448c-312">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-313">Az.Network</span></span>
* <span data-ttu-id="0448c-314">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-314">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="0448c-315">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-315">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="0448c-316">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-316">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="0448c-317">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-317">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-318">Az.Resources</span></span>
* <span data-ttu-id="0448c-319">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-319">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="0448c-320">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="0448c-320">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="0448c-321">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="0448c-321">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="0448c-322">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="0448c-322">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="0448c-323">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-323">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="0448c-324">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-324">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="0448c-325">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-325">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="0448c-326">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="0448c-326">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="0448c-327">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0448c-327">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="0448c-328">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0448c-328">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="0448c-329">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0448c-329">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="0448c-330">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-330">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="0448c-331">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0448c-331">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="0448c-332">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-332">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-333">Az.Sql</span></span>
* <span data-ttu-id="0448c-334">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-334">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="0448c-335">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-335">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="0448c-336">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="0448c-336">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="0448c-337">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="0448c-337">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="0448c-338">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="0448c-338">Remove an LTR backup</span></span>
    - <span data-ttu-id="0448c-339">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="0448c-339">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="0448c-340">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-340">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="0448c-341">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-341">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="0448c-342">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-342">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-343">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-343">Az.Storage</span></span>
* <span data-ttu-id="0448c-344">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-344">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="0448c-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="0448c-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="0448c-346">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-346">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="0448c-347">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="0448c-347">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="0448c-348">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="0448c-348">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-349">Az.Websites</span></span>
* <span data-ttu-id="0448c-350">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-350">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="0448c-351">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="0448c-351">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="0448c-352">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-352">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="0448c-353">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="0448c-353">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="0448c-354">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-354">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="0448c-355">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="0448c-355">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0448c-356">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0448c-356">Highlights since the last major release</span></span>
* <span data-ttu-id="0448c-357">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-357">Updated client side telemetry.</span></span>
* <span data-ttu-id="0448c-358">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-358">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="0448c-359">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-359">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0448c-360">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-360">Az.Accounts</span></span>
* <span data-ttu-id="0448c-361">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-361">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0448c-362">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0448c-362">Az.Automation</span></span>
* <span data-ttu-id="0448c-363">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-363">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0448c-364">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0448c-364">Az.CognitiveServices</span></span>
* <span data-ttu-id="0448c-365">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-365">Updated SDK to 7.0</span></span>
* <span data-ttu-id="0448c-366">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-366">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-367">Az.Compute</span></span>
* <span data-ttu-id="0448c-368">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="0448c-368">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0448c-369">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0448c-369">Az.FrontDoor</span></span>
* <span data-ttu-id="0448c-370">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-370">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0448c-371">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0448c-371">Az.IotHub</span></span>
* <span data-ttu-id="0448c-372">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-372">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="0448c-373">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0448c-373">New Cmdlets are:</span></span>
    - <span data-ttu-id="0448c-374">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0448c-374">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0448c-375">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0448c-375">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0448c-376">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0448c-376">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0448c-377">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0448c-377">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0448c-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0448c-378">Az.KeyVault</span></span>
* <span data-ttu-id="0448c-379">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-379">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0448c-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-380">Az.Monitor</span></span>
* <span data-ttu-id="0448c-381">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-381">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="0448c-382">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-382">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="0448c-383">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="0448c-383">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-384">Az.Network</span></span>
* <span data-ttu-id="0448c-385">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-385">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="0448c-386">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-386">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0448c-387">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-387">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0448c-388">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="0448c-388">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="0448c-389">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="0448c-389">No new cmdlets are added.</span></span> <span data-ttu-id="0448c-390">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="0448c-390">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-392">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-392">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-393">Az.Resources</span></span>
* <span data-ttu-id="0448c-394">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="0448c-394">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="0448c-395">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0448c-395">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="0448c-396">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0448c-396">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="0448c-397">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="0448c-397">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="0448c-398">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-398">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="0448c-399">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-399">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="0448c-400">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-400">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="0448c-401">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-401">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-402">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-402">Az.Sql</span></span>
* <span data-ttu-id="0448c-403">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-403">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="0448c-404">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-404">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="0448c-405">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="0448c-405">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0448c-406">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0448c-406">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0448c-407">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-407">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0448c-408">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0448c-408">Az.StorageSync</span></span>
* <span data-ttu-id="0448c-409">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-409">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="0448c-410">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="0448c-410">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0448c-411">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0448c-411">Highlights since the last major release</span></span>
* <span data-ttu-id="0448c-412">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="0448c-412">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="0448c-413">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-413">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0448c-414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-414">Az.Accounts</span></span>
* <span data-ttu-id="0448c-415">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="0448c-415">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="0448c-416">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-416">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0448c-417">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0448c-417">Az.ApiManagement</span></span>
* <span data-ttu-id="0448c-418">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="0448c-418">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="0448c-419">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="0448c-419">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="0448c-420">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-420">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="0448c-421">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-421">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-422">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-422">Az.Compute</span></span>
* <span data-ttu-id="0448c-423">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="0448c-423">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="0448c-424">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-424">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="0448c-425">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-425">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="0448c-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="0448c-427">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-427">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-428">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-428">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-429">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-429">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0448c-430">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0448c-430">Az.DeploymentManager</span></span>
* <span data-ttu-id="0448c-431">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="0448c-431">Adds LIST operations for resources</span></span>
* <span data-ttu-id="0448c-432">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="0448c-432">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0448c-433">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0448c-433">Az.HDInsight</span></span>
* <span data-ttu-id="0448c-434">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-434">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0448c-435">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0448c-435">Az.KeyVault</span></span>
* <span data-ttu-id="0448c-436">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-436">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-437">Az.Network</span></span>
* <span data-ttu-id="0448c-438">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-438">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="0448c-439">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="0448c-439">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="0448c-440">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-440">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0448c-441">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-441">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="0448c-442">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="0448c-442">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="0448c-443">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-443">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="0448c-444">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-444">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="0448c-445">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-445">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="0448c-446">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-446">New cmdlets added:</span></span>
        - <span data-ttu-id="0448c-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0448c-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="0448c-448">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-448">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="0448c-449">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0448c-449">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="0448c-450">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-450">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0448c-451">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-451">Az.PolicyInsights</span></span>
* <span data-ttu-id="0448c-452">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="0448c-452">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="0448c-453">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-453">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="0448c-454">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-454">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="0448c-455">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-455">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-456">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-457">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-457">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="0448c-458">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="0448c-458">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-459">Az.Resources</span></span>
* <span data-ttu-id="0448c-460">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-460">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="0448c-461">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-461">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-462">Az.Sql</span></span>
<span data-ttu-id="0448c-463">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-463">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-464">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-464">Az.Storage</span></span>
* <span data-ttu-id="0448c-465">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="0448c-465">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="0448c-466">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-466">New-AzStorageAccount</span></span>
* <span data-ttu-id="0448c-467">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="0448c-467">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="0448c-468">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-468">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-469">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-469">Az.Websites</span></span>
* <span data-ttu-id="0448c-470">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="0448c-470">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="0448c-471">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-471">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="0448c-472">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="0448c-472">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0448c-473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-473">Az.Accounts</span></span>
* <span data-ttu-id="0448c-474">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-474">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0448c-475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0448c-475">Az.Cdn</span></span>
* <span data-ttu-id="0448c-476">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="0448c-476">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-477">Az.Compute</span></span>
* <span data-ttu-id="0448c-478">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-478">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="0448c-479">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0448c-479">Az.ContainerInstance</span></span>
* <span data-ttu-id="0448c-480">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-480">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0448c-481">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0448c-481">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0448c-482">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-482">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0448c-483">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="0448c-483">Get the Edge Storage Container</span></span>
* <span data-ttu-id="0448c-484">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-484">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0448c-485">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0448c-485">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="0448c-486">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-486">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0448c-487">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0448c-487">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="0448c-488">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-488">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0448c-489">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="0448c-489">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="0448c-490">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-490">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0448c-491">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="0448c-491">Get the Edge Storage Account</span></span>
* <span data-ttu-id="0448c-492">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-492">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0448c-493">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="0448c-493">Create new Edge Storage Account</span></span>
* <span data-ttu-id="0448c-494">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-494">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0448c-495">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0448c-495">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="0448c-496">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="0448c-496">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="0448c-497">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="0448c-497">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="0448c-498">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-498">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="0448c-499">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="0448c-499">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-500">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-501">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-501">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="0448c-502">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-502">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="0448c-503">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-503">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="0448c-504">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="0448c-504">Az.DevTestLabs</span></span>
* <span data-ttu-id="0448c-505">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-505">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0448c-506">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0448c-506">Az.EventHub</span></span>
* <span data-ttu-id="0448c-507">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-507">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0448c-508">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0448c-508">Az.HDInsight</span></span>
* <span data-ttu-id="0448c-509">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-509">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0448c-510">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0448c-510">Az.MachineLearning</span></span>
* <span data-ttu-id="0448c-511">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-511">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="0448c-512">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0448c-512">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="0448c-513">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="0448c-513">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="0448c-514">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0448c-514">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="0448c-515">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0448c-515">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="0448c-516">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0448c-516">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="0448c-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="0448c-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="0448c-518">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="0448c-518">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-519">Az.Network</span></span>
* <span data-ttu-id="0448c-520">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-520">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-521">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-521">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-522">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-522">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="0448c-523">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-523">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0448c-524">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-524">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0448c-525">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-525">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-526">Az.Resources</span></span>
* <span data-ttu-id="0448c-527">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-527">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-528">Az.Sql</span></span>
* <span data-ttu-id="0448c-529">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-529">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="0448c-530">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-530">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0448c-531">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0448c-531">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0448c-532">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-532">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-533">Az.Storage</span></span>
* <span data-ttu-id="0448c-534">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-534">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="0448c-535">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0448c-535">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="0448c-536">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="0448c-536">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="0448c-537">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-537">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="0448c-538">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-538">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="0448c-539">Genel</span><span class="sxs-lookup"><span data-stu-id="0448c-539">General</span></span>
* <span data-ttu-id="0448c-540">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-540">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0448c-541">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-541">Az.Accounts</span></span>
* <span data-ttu-id="0448c-542">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="0448c-542">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="0448c-543">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="0448c-543">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0448c-544">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0448c-544">Az.Batch</span></span>
* <span data-ttu-id="0448c-545">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-545">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-546">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-547">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-547">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0448c-548">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0448c-548">Az.FrontDoor</span></span>
* <span data-ttu-id="0448c-549">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-549">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="0448c-550">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-550">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0448c-551">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0448c-551">Az.HealthcareApis</span></span>
* <span data-ttu-id="0448c-552">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="0448c-552">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0448c-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0448c-553">Az.KeyVault</span></span>
* <span data-ttu-id="0448c-554">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-554">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="0448c-555">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="0448c-555">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="0448c-556">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-556">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0448c-557">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-557">Az.Monitor</span></span>
* <span data-ttu-id="0448c-558">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-558">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="0448c-559">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="0448c-559">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="0448c-560">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="0448c-560">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-561">Az.Network</span></span>
* <span data-ttu-id="0448c-562">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-562">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-563">Az.Resources</span></span>
* <span data-ttu-id="0448c-564">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-564">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="0448c-565">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-565">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-566">Az.Sql</span></span>
* <span data-ttu-id="0448c-567">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-567">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-568">Az.Storage</span></span>
* <span data-ttu-id="0448c-569">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="0448c-569">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="0448c-570">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="0448c-570">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="0448c-571">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0448c-571">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="0448c-572">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="0448c-572">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="0448c-573">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="0448c-573">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="0448c-574">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-574">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="0448c-575">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-575">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="0448c-576">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0448c-576">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="0448c-577">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0448c-577">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="0448c-578">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-578">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="0448c-579">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="0448c-579">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="0448c-580">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-580">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="0448c-581">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="0448c-581">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="0448c-582">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-582">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0448c-583">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0448c-583">Highlights since the last major release</span></span>
* <span data-ttu-id="0448c-584">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="0448c-584">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="0448c-585">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="0448c-585">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-586">Az.Compute</span></span>
* <span data-ttu-id="0448c-587">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="0448c-587">VM Reapply feature</span></span>
    - <span data-ttu-id="0448c-588">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="0448c-588">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="0448c-589">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="0448c-589">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="0448c-590">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0448c-590">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="0448c-591">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="0448c-591">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="0448c-592">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-592">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0448c-593">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-593">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="0448c-594">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-594">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="0448c-595">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-595">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="0448c-596">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-596">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="0448c-597">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-597">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0448c-598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0448c-598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0448c-599">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-599">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0448c-600">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="0448c-600">Get the Order</span></span>
* <span data-ttu-id="0448c-601">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-601">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0448c-602">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="0448c-602">Create new Order</span></span>
* <span data-ttu-id="0448c-603">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-603">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0448c-604">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="0448c-604">Remove the Order</span></span>
* <span data-ttu-id="0448c-605">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="0448c-605">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="0448c-606">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="0448c-606">Now creates Local Share</span></span>
* <span data-ttu-id="0448c-607">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-607">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="0448c-608">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="0448c-608">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="0448c-609">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-609">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="0448c-610">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="0448c-610">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="0448c-611">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-611">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0448c-612">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="0448c-612">Gets the information about Triggers</span></span>
* <span data-ttu-id="0448c-613">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-613">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0448c-614">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="0448c-614">Create new Triggers</span></span>
* <span data-ttu-id="0448c-615">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-615">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0448c-616">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="0448c-616">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-617">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-618">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-618">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="0448c-619">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-619">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-620">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-620">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-621">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-621">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0448c-622">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0448c-622">Az.EventHub</span></span>
* <span data-ttu-id="0448c-623">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-623">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0448c-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0448c-624">Az.FrontDoor</span></span>
* <span data-ttu-id="0448c-625">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-625">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="0448c-626">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-626">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="0448c-627">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-627">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="0448c-628">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="0448c-628">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-629">Az.Network</span></span>
* <span data-ttu-id="0448c-630">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-630">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="0448c-631">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="0448c-631">Az.PrivateDns</span></span>
* <span data-ttu-id="0448c-632">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-632">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-633">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-633">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-634">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-634">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="0448c-635">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="0448c-635">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="0448c-636">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-636">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0448c-637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0448c-637">Az.RedisCache</span></span>
* <span data-ttu-id="0448c-638">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-638">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="0448c-639">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-639">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="0448c-640">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-640">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-641">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-641">Az.Resources</span></span>
- <span data-ttu-id="0448c-642">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-642">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="0448c-643">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-643">Updated create policy definition help example</span></span>
- <span data-ttu-id="0448c-644">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-644">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="0448c-645">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-645">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="0448c-646">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-646">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-647">Az.Sql</span></span>
* <span data-ttu-id="0448c-648">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-648">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="0448c-649">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-649">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="0448c-650">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-650">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="0448c-651">Genel</span><span class="sxs-lookup"><span data-stu-id="0448c-651">General</span></span>
* <span data-ttu-id="0448c-652">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="0448c-652">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0448c-653">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-653">Az.Accounts</span></span>
* <span data-ttu-id="0448c-654">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0448c-654">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0448c-655">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0448c-655">Az.Advisor</span></span>
* <span data-ttu-id="0448c-656">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-656">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0448c-657">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0448c-657">Az.Batch</span></span>
* <span data-ttu-id="0448c-658">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-658">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="0448c-659">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="0448c-659">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="0448c-660">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-660">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="0448c-661">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-661">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="0448c-662">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="0448c-662">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="0448c-663">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="0448c-663">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="0448c-664">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="0448c-664">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="0448c-665">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-665">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="0448c-666">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-666">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="0448c-667">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-667">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0448c-668">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="0448c-668">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="0448c-669">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="0448c-669">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="0448c-670">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-670">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0448c-671">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="0448c-671">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="0448c-672">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-672">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="0448c-673">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-673">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="0448c-674">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-674">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="0448c-675">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-675">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="0448c-676">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-676">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="0448c-677">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-677">This operation is no longer supported.</span></span>
* <span data-ttu-id="0448c-678">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-678">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0448c-679">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-679">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0448c-680">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-680">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="0448c-681">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-681">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="0448c-682">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-682">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="0448c-683">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-683">New non-verified images are also now returned.</span></span> <span data-ttu-id="0448c-684">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-684">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="0448c-685">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-685">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="0448c-686">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-686">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="0448c-687">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-687">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="0448c-688">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-688">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="0448c-689">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-689">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="0448c-690">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-690">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="0448c-691">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-691">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="0448c-692">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="0448c-692">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="0448c-693">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="0448c-693">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0448c-694">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0448c-694">Az.Cdn</span></span>
* <span data-ttu-id="0448c-695">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-695">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="0448c-696">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-696">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-697">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-697">Az.Compute</span></span>
* <span data-ttu-id="0448c-698">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="0448c-698">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="0448c-699">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0448c-699">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="0448c-700">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0448c-700">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="0448c-701">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-701">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0448c-702">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-702">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="0448c-703">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="0448c-703">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="0448c-704">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-704">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="0448c-705">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0448c-705">Breaking changes</span></span>
    - <span data-ttu-id="0448c-706">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="0448c-706">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="0448c-707">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="0448c-707">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-708">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-708">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-709">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-709">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-711">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="0448c-711">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="0448c-712">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="0448c-712">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="0448c-713">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="0448c-713">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="0448c-714">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="0448c-714">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="0448c-715">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="0448c-715">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="0448c-716">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="0448c-716">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0448c-717">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0448c-717">Az.FrontDoor</span></span>
* <span data-ttu-id="0448c-718">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-718">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0448c-719">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0448c-719">Az.HDInsight</span></span>
* <span data-ttu-id="0448c-720">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-720">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="0448c-721">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-721">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="0448c-722">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-722">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="0448c-723">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="0448c-723">Removed five cmdlets:</span></span>
    - <span data-ttu-id="0448c-724">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0448c-724">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0448c-725">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0448c-725">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0448c-726">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0448c-726">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0448c-727">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0448c-727">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="0448c-728">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0448c-728">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="0448c-729">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-729">Added three cmdlets:</span></span>
    - <span data-ttu-id="0448c-730">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="0448c-730">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0448c-731">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="0448c-731">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0448c-732">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="0448c-732">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="0448c-733">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-733">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="0448c-734">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-734">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="0448c-735">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-735">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="0448c-736">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-736">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="0448c-737">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-737">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="0448c-738">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-738">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="0448c-739">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-739">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="0448c-740">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-740">Added some scenario test cases.</span></span>
* <span data-ttu-id="0448c-741">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="0448c-741">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0448c-742">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0448c-742">Az.IotHub</span></span>
* <span data-ttu-id="0448c-743">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="0448c-743">Breaking changes:</span></span>
    - <span data-ttu-id="0448c-744">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="0448c-744">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0448c-745">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-745">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0448c-746">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="0448c-746">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0448c-747">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-747">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0448c-748">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-748">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="0448c-749">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-749">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="0448c-750">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-750">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="0448c-751">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-751">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="0448c-752">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="0448c-752">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0448c-753">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-753">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0448c-754">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="0448c-754">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0448c-755">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-755">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-756">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-756">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-757">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-757">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="0448c-758">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-758">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="0448c-759">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-759">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="0448c-760">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-760">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="0448c-761">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-761">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="0448c-762">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-762">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="0448c-763">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-763">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="0448c-764">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-764">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="0448c-765">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-765">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-766">Az.Resources</span></span>
* <span data-ttu-id="0448c-767">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-767">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-768">Az.Network</span></span>
* <span data-ttu-id="0448c-769">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-769">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="0448c-770">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-770">Updated cmdlet:</span></span>
        - <span data-ttu-id="0448c-771">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-771">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0448c-772">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-772">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0448c-773">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-773">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0448c-774">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-774">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0448c-775">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-775">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0448c-776">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-776">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="0448c-777">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0448c-777">New cmdlet:</span></span>
        - <span data-ttu-id="0448c-778">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0448c-778">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="0448c-779">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-779">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="0448c-780">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-780">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="0448c-781">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-781">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="0448c-782">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-782">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="0448c-783">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-783">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="0448c-784">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-784">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="0448c-785">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-785">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="0448c-786">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-786">New cmdlets added:</span></span>
        - <span data-ttu-id="0448c-787">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="0448c-787">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="0448c-788">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0448c-788">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0448c-789">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0448c-789">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0448c-790">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0448c-790">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0448c-791">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0448c-791">Set-AzVirtualHub</span></span>
* <span data-ttu-id="0448c-792">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-792">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="0448c-793">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0448c-794">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-794">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0448c-795">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-795">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0448c-796">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-796">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="0448c-797">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-797">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="0448c-798">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-798">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="0448c-799">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-799">New cmdlets added:</span></span>
        - <span data-ttu-id="0448c-800">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-800">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="0448c-801">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-801">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0448c-802">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-802">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0448c-803">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-803">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0448c-804">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-804">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0448c-805">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-805">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0448c-806">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-806">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="0448c-807">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-807">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="0448c-808">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-808">New cmdlets added:</span></span>
        - <span data-ttu-id="0448c-809">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="0448c-809">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="0448c-810">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="0448c-810">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="0448c-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="0448c-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="0448c-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="0448c-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="0448c-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="0448c-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="0448c-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="0448c-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="0448c-815">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-815">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0448c-816">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-816">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="0448c-817">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-817">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="0448c-818">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-818">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="0448c-819">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-819">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="0448c-820">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-820">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0448c-821">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-821">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="0448c-822">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-822">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="0448c-823">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-823">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="0448c-824">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="0448c-824">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="0448c-825">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-825">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="0448c-826">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-826">New cmdlets added:</span></span>
        - <span data-ttu-id="0448c-827">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0448c-827">New-AzIpGroup</span></span>
        - <span data-ttu-id="0448c-828">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0448c-828">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="0448c-829">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0448c-829">Get-AzIpGroup</span></span>
        - <span data-ttu-id="0448c-830">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0448c-830">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0448c-831">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0448c-831">Az.ServiceFabric</span></span>
* <span data-ttu-id="0448c-832">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-832">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-833">Az.Sql</span></span>
* <span data-ttu-id="0448c-834">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-834">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="0448c-835">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-835">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="0448c-836">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="0448c-836">Removed deprecated aliases:</span></span>
* <span data-ttu-id="0448c-837">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="0448c-837">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="0448c-838">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="0448c-838">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="0448c-839">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-839">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0448c-840">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-840">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="0448c-841">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-841">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="0448c-842">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-842">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-843">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-843">Az.Storage</span></span>
* <span data-ttu-id="0448c-844">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="0448c-844">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="0448c-845">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-845">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0448c-846">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-846">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0448c-847">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="0448c-847">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="0448c-848">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0448c-848">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="0448c-849">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0448c-849">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="0448c-850">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-850">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="0448c-851">Genel</span><span class="sxs-lookup"><span data-stu-id="0448c-851">General</span></span>
* <span data-ttu-id="0448c-852">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="0448c-852">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0448c-853">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-853">Az.Accounts</span></span>
* <span data-ttu-id="0448c-854">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-854">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0448c-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0448c-855">Az.ApiManagement</span></span>
* <span data-ttu-id="0448c-856">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-856">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="0448c-857">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-857">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0448c-858">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0448c-858">Az.Automation</span></span>
* <span data-ttu-id="0448c-859">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-859">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0448c-860">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0448c-860">Az.Batch</span></span>
* <span data-ttu-id="0448c-861">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="0448c-861">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-862">Az.Compute</span></span>
* <span data-ttu-id="0448c-863">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-863">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0448c-864">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-864">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="0448c-865">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-865">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="0448c-866">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-866">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-867">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-868">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="0448c-868">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="0448c-869">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="0448c-869">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="0448c-870">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-870">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-871">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-871">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-872">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-872">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0448c-873">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0448c-873">Az.HealthcareApis</span></span>
* <span data-ttu-id="0448c-874">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-874">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="0448c-875">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-875">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="0448c-876">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-876">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="0448c-877">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-877">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0448c-878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0448c-878">Az.IotHub</span></span>
* <span data-ttu-id="0448c-879">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="0448c-879">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="0448c-880">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="0448c-880">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0448c-881">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-881">Az.Monitor</span></span>
* <span data-ttu-id="0448c-882">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-882">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="0448c-883">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="0448c-883">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="0448c-884">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="0448c-884">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="0448c-885">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-885">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-886">Az.Network</span></span>
* <span data-ttu-id="0448c-887">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-887">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="0448c-888">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-888">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="0448c-889">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-889">New cmdlets added:</span></span>
        - <span data-ttu-id="0448c-890">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="0448c-890">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="0448c-891">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-891">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0448c-892">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-892">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="0448c-893">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-893">Updated cmdlets:</span></span>
        - <span data-ttu-id="0448c-894">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-894">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0448c-895">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-895">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0448c-896">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-896">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0448c-897">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-897">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="0448c-898">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="0448c-898">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="0448c-899">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="0448c-899">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="0448c-900">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="0448c-900">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0448c-901">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0448c-901">Az.RedisCache</span></span>
* <span data-ttu-id="0448c-902">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-902">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-903">Az.Sql</span></span>
* <span data-ttu-id="0448c-904">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-904">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-905">Az.Storage</span></span>
* <span data-ttu-id="0448c-906">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-906">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="0448c-907">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="0448c-907">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0448c-908">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0448c-908">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="0448c-909">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="0448c-909">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0448c-910">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-910">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0448c-911">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0448c-911">Az.StorageSync</span></span>
* <span data-ttu-id="0448c-912">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-912">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-913">Az.Websites</span></span>
* <span data-ttu-id="0448c-914">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="0448c-914">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="0448c-915">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-915">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0448c-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0448c-916">Az.ApiManagement</span></span>
* <span data-ttu-id="0448c-917">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-917">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="0448c-918">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-918">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="0448c-919">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="0448c-919">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0448c-920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0448c-920">Az.Automation</span></span>
* <span data-ttu-id="0448c-921">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-921">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="0448c-922">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-922">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="0448c-923">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-923">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-924">Az.Compute</span></span>
* <span data-ttu-id="0448c-925">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-925">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="0448c-926">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-926">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0448c-927">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-927">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="0448c-928">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-928">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="0448c-929">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-929">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="0448c-930">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-930">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="0448c-931">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-931">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="0448c-932">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-932">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="0448c-933">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-933">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-934">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-934">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-935">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="0448c-935">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="0448c-936">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-936">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0448c-937">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0448c-937">Az.HDInsight</span></span>
* <span data-ttu-id="0448c-938">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="0448c-938">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0448c-939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0448c-939">Az.IotHub</span></span>
* <span data-ttu-id="0448c-940">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-940">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="0448c-941">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-941">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="0448c-942">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0448c-942">New cmdlets are:</span></span>
    - <span data-ttu-id="0448c-943">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0448c-943">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0448c-944">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0448c-944">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0448c-945">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0448c-945">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0448c-946">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0448c-946">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0448c-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-947">Az.Monitor</span></span>
* <span data-ttu-id="0448c-948">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="0448c-948">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="0448c-949">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="0448c-949">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="0448c-950">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="0448c-950">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="0448c-951">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="0448c-951">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="0448c-952">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-952">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="0448c-953">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-953">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="0448c-954">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="0448c-954">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="0448c-955">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="0448c-955">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="0448c-956">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-956">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0448c-957">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="0448c-957">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="0448c-958">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-958">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0448c-959">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="0448c-959">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="0448c-960">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-960">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="0448c-961">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="0448c-961">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="0448c-962">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="0448c-962">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="0448c-963">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="0448c-963">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="0448c-964">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="0448c-964">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="0448c-965">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="0448c-965">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="0448c-966">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-966">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="0448c-967">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-967">Overall improved help files</span></span>
* <span data-ttu-id="0448c-968">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-968">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-969">Az.Network</span></span>
* <span data-ttu-id="0448c-970">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-970">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="0448c-971">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-971">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="0448c-972">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-972">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="0448c-973">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-973">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="0448c-974">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-974">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="0448c-975">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-975">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="0448c-976">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-976">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="0448c-977">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-977">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="0448c-978">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-978">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="0448c-979">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-979">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="0448c-980">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-980">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="0448c-981">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="0448c-981">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="0448c-982">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-982">New cmdlets</span></span>
        - <span data-ttu-id="0448c-983">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="0448c-983">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="0448c-984">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-984">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="0448c-985">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-985">Updated cmdlet:</span></span>
        - <span data-ttu-id="0448c-986">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0448c-986">New-VpnSite</span></span>
        - <span data-ttu-id="0448c-987">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0448c-987">Update-VpnSite</span></span>
        - <span data-ttu-id="0448c-988">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-988">New-VpnConnection</span></span>
        - <span data-ttu-id="0448c-989">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-989">Update-VpnConnection</span></span>
* <span data-ttu-id="0448c-990">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-990">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-992">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-992">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="0448c-993">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-993">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-994">Az.Resources</span></span>
* <span data-ttu-id="0448c-995">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-995">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0448c-996">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0448c-996">Az.ServiceFabric</span></span>
* <span data-ttu-id="0448c-997">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-997">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="0448c-998">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="0448c-998">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="0448c-999">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0448c-999">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0448c-1000">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0448c-1000">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0448c-1001">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0448c-1001">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0448c-1002">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0448c-1002">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="0448c-1003">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0448c-1003">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0448c-1004">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0448c-1004">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0448c-1005">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0448c-1005">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0448c-1006">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0448c-1006">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0448c-1007">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0448c-1007">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="0448c-1008">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0448c-1008">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0448c-1009">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0448c-1009">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0448c-1010">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0448c-1010">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0448c-1011">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="0448c-1011">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="0448c-1012">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1012">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0448c-1013">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0448c-1013">Az.SignalR</span></span>
* <span data-ttu-id="0448c-1014">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1014">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1015">Az.Sql</span></span>
* <span data-ttu-id="0448c-1016">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1016">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="0448c-1017">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1017">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="0448c-1018">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-1018">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="0448c-1019">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1019">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="0448c-1020">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1020">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-1021">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-1021">Az.Storage</span></span>
* <span data-ttu-id="0448c-1022">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1022">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="0448c-1023">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1023">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="0448c-1024">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0448c-1024">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="0448c-1025">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0448c-1025">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="0448c-1026">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1026">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="0448c-1027">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0448c-1027">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="0448c-1028">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1028">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="0448c-1029">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0448c-1029">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0448c-1030">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0448c-1030">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0448c-1031">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0448c-1031">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0448c-1032">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0448c-1032">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-1033">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-1033">Az.Websites</span></span>
* <span data-ttu-id="0448c-1034">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="0448c-1034">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="0448c-1035">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="0448c-1035">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="0448c-1036">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1036">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="0448c-1037">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1037">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="0448c-1038">Genel</span><span class="sxs-lookup"><span data-stu-id="0448c-1038">General</span></span>
* <span data-ttu-id="0448c-1039">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1039">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0448c-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-1040">Az.Accounts</span></span>
* <span data-ttu-id="0448c-1041">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="0448c-1041">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="0448c-1042">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0448c-1042">Az.Aks</span></span>
* <span data-ttu-id="0448c-1043">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1043">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="0448c-1044">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="0448c-1044">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0448c-1045">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0448c-1045">Az.ApiManagement</span></span>
* <span data-ttu-id="0448c-1046">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1046">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="0448c-1047">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1047">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="0448c-1048">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1048">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="0448c-1049">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="0448c-1049">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="0448c-1050">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1050">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0448c-1051">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0448c-1051">Az.Batch</span></span>
* <span data-ttu-id="0448c-1052">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1052">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0448c-1053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0448c-1053">Az.Cdn</span></span>
* <span data-ttu-id="0448c-1054">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1054">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1055">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1055">Az.Compute</span></span>
* <span data-ttu-id="0448c-1056">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1056">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="0448c-1057">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1057">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="0448c-1058">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1058">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="0448c-1059">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1059">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="0448c-1060">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="0448c-1060">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="0448c-1061">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1061">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="0448c-1062">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1062">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="0448c-1063">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1063">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-1064">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-1064">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-1065">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1065">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="0448c-1066">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1066">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="0448c-1067">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1067">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="0448c-1068">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1068">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-1069">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-1070">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1070">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0448c-1071">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0448c-1071">Az.EventHub</span></span>
* <span data-ttu-id="0448c-1072">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="0448c-1072">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="0448c-1073">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="0448c-1073">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="0448c-1074">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1074">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="0448c-1075">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="0448c-1075">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="0448c-1076">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0448c-1076">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0448c-1077">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1077">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0448c-1078">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-1078">Az.Monitor</span></span>
* <span data-ttu-id="0448c-1079">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1079">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-1080">Az.Network</span></span>
* <span data-ttu-id="0448c-1081">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1081">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="0448c-1082">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1082">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="0448c-1083">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1083">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="0448c-1084">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="0448c-1084">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="0448c-1085">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1085">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="0448c-1086">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1086">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="0448c-1087">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1087">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0448c-1088">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-1088">Az.OperationalInsights</span></span>
* <span data-ttu-id="0448c-1089">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1089">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="0448c-1090">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1090">Added example</span></span>
    - <span data-ttu-id="0448c-1091">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1091">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="0448c-1092">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1092">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="0448c-1093">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1093">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-1094">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1094">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-1095">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1095">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1096">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1096">Az.Resources</span></span>
* <span data-ttu-id="0448c-1097">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1097">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="0448c-1098">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1098">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="0448c-1099">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="0448c-1099">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="0448c-1100">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1100">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0448c-1101">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0448c-1101">Az.ServiceBus</span></span>
* <span data-ttu-id="0448c-1102">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="0448c-1102">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="0448c-1103">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="0448c-1103">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="0448c-1104">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1104">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0448c-1105">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0448c-1105">Az.ServiceFabric</span></span>
* <span data-ttu-id="0448c-1106">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-1106">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="0448c-1107">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="0448c-1107">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="0448c-1108">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="0448c-1108">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="0448c-1109">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1109">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="0448c-1110">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="0448c-1110">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="0448c-1111">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-1111">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1112">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1112">Az.Sql</span></span>
* <span data-ttu-id="0448c-1113">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1113">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-1114">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-1114">Az.Storage</span></span>
* <span data-ttu-id="0448c-1115">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1115">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="0448c-1116">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="0448c-1116">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="0448c-1117">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0448c-1117">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="0448c-1118">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0448c-1118">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="0448c-1119">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="0448c-1119">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="0448c-1120">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0448c-1120">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-1121">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-1121">Az.Websites</span></span>
* <span data-ttu-id="0448c-1122">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1122">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="0448c-1123">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1123">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0448c-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-1124">Az.Accounts</span></span>
* <span data-ttu-id="0448c-1125">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1125">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="0448c-1126">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-1126">Az.ApplicationInsights</span></span>
* <span data-ttu-id="0448c-1127">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1127">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0448c-1128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0448c-1128">Az.Automation</span></span>
* <span data-ttu-id="0448c-1129">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1129">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0448c-1130">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1130">Az.CognitiveServices</span></span>
* <span data-ttu-id="0448c-1131">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1131">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1132">Az.Compute</span></span>
* <span data-ttu-id="0448c-1133">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1133">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0448c-1134">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0448c-1134">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0448c-1135">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1135">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="0448c-1136">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="0448c-1136">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-1137">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-1137">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-1138">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1138">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="0448c-1139">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1139">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0448c-1140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0448c-1140">Az.EventHub</span></span>
* <span data-ttu-id="0448c-1141">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0448c-1141">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0448c-1142">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1142">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0448c-1143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0448c-1143">Az.KeyVault</span></span>
* <span data-ttu-id="0448c-1144">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1144">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0448c-1145">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0448c-1145">Az.LogicApp</span></span>
* <span data-ttu-id="0448c-1146">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="0448c-1146">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="0448c-1147">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1147">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="0448c-1148">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1148">Az.ManagedServices</span></span>
* <span data-ttu-id="0448c-1149">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="0448c-1149">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-1150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-1150">Az.Network</span></span>
* <span data-ttu-id="0448c-1151">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1151">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="0448c-1152">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1152">New cmdlets</span></span>
        - <span data-ttu-id="0448c-1153">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0448c-1153">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0448c-1154">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0448c-1154">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0448c-1155">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-1155">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0448c-1156">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-1156">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0448c-1157">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-1157">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0448c-1158">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-1158">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0448c-1159">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="0448c-1159">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="0448c-1160">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0448c-1160">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="0448c-1161">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="0448c-1161">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="0448c-1162">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1162">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="0448c-1163">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1163">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="0448c-1164">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1164">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="0448c-1165">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-1165">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="0448c-1166">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1166">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="0448c-1167">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1167">Updated cmdlets</span></span>
        - <span data-ttu-id="0448c-1168">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-1168">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0448c-1169">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-1169">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0448c-1170">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-1170">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0448c-1171">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1171">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0448c-1172">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1172">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="0448c-1173">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-1173">Updated cmdlet:</span></span>
        - <span data-ttu-id="0448c-1174">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-1174">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0448c-1175">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-1175">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0448c-1176">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-1176">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="0448c-1177">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1177">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="0448c-1178">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1178">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="0448c-1179">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="0448c-1179">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0448c-1180">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-1180">Az.OperationalInsights</span></span>
* <span data-ttu-id="0448c-1181">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1181">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="0448c-1182">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1182">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-1183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1183">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-1184">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1184">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0448c-1185">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1185">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="0448c-1186">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1186">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="0448c-1187">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1187">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0448c-1188">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1188">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="0448c-1189">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1189">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0448c-1190">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1190">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="0448c-1191">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1191">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0448c-1192">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1192">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="0448c-1193">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1193">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1194">Az.Resources</span></span>
- <span data-ttu-id="0448c-1195">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-1195">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="0448c-1196">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1196">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0448c-1197">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0448c-1197">Az.ServiceBus</span></span>
* <span data-ttu-id="0448c-1198">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0448c-1198">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0448c-1199">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1199">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1200">Az.Sql</span></span>
* <span data-ttu-id="0448c-1201">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1201">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="0448c-1202">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1202">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="0448c-1203">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1203">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-1204">Az.Storage</span></span>
* <span data-ttu-id="0448c-1205">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1205">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0448c-1206">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0448c-1206">Az.StorageSync</span></span>
* <span data-ttu-id="0448c-1207">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-1207">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="0448c-1208">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1208">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-1209">Az.Websites</span></span>
* <span data-ttu-id="0448c-1210">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1210">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="0448c-1211">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1211">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="0448c-1212">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1212">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="0448c-1213">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1213">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0448c-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-1214">Az.Accounts</span></span>
* <span data-ttu-id="0448c-1215">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1215">Add support for profile cmdlets</span></span>
* <span data-ttu-id="0448c-1216">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1216">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="0448c-1217">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1217">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0448c-1218">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0448c-1218">Az.Advisor</span></span>
* <span data-ttu-id="0448c-1219">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-1219">GA release of Az.Advisor</span></span>
* <span data-ttu-id="0448c-1220">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="0448c-1220">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0448c-1221">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0448c-1221">Az.ApiManagement</span></span>
* <span data-ttu-id="0448c-1222">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1222">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="0448c-1223">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0448c-1223">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="0448c-1224">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1224">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="0448c-1225">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="0448c-1225">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="0448c-1226">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="0448c-1226">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="0448c-1227">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0448c-1227">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="0448c-1228">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1228">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0448c-1229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0448c-1229">Az.Automation</span></span>
* <span data-ttu-id="0448c-1230">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1230">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1231">Az.Compute</span></span>
* <span data-ttu-id="0448c-1232">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1232">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-1233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-1233">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-1234">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-1234">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0448c-1235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0448c-1235">Az.EventGrid</span></span>
* <span data-ttu-id="0448c-1236">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1236">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0448c-1237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0448c-1237">Az.IotHub</span></span>
* <span data-ttu-id="0448c-1238">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1238">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-1239">Az.Network</span></span>
* <span data-ttu-id="0448c-1240">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1240">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="0448c-1241">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1241">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0448c-1242">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-1242">Az.PolicyInsights</span></span>
* <span data-ttu-id="0448c-1243">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1243">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="0448c-1244">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="0448c-1244">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0448c-1245">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-1245">Az.OperationalInsights</span></span>
* <span data-ttu-id="0448c-1246">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1246">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-1247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1247">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-1248">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0448c-1248">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1249">Az.Resources</span></span>
    - <span data-ttu-id="0448c-1250">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0448c-1250">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="0448c-1251">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1251">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="0448c-1252">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1252">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="0448c-1253">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1253">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0448c-1254">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0448c-1254">Az.ServiceBus</span></span>
* <span data-ttu-id="0448c-1255">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1255">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1256">Az.Sql</span></span>
* <span data-ttu-id="0448c-1257">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1257">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="0448c-1258">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-1258">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="0448c-1259">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0448c-1259">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0448c-1260">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0448c-1260">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0448c-1261">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0448c-1261">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0448c-1262">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0448c-1262">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0448c-1263">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0448c-1263">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0448c-1264">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0448c-1264">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="0448c-1265">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-1265">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-1266">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-1266">Az.Storage</span></span>
* <span data-ttu-id="0448c-1267">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-1267">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="0448c-1268">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0448c-1268">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="0448c-1269">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1269">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="0448c-1270">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="0448c-1270">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="0448c-1271">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1271">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="0448c-1272">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-1272">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0448c-1273">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-1273">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0448c-1274">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1274">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="0448c-1275">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0448c-1275">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="0448c-1276">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0448c-1276">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0448c-1277">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0448c-1277">Az.StorageSync</span></span>
* <span data-ttu-id="0448c-1278">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="0448c-1278">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="0448c-1279">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1279">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0448c-1280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-1280">Az.Accounts</span></span>
* <span data-ttu-id="0448c-1281">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1281">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="0448c-1282">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="0448c-1282">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="0448c-1283">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1283">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="0448c-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0448c-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="0448c-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="0448c-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1286">Az.Compute</span></span>
* <span data-ttu-id="0448c-1287">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-1287">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="0448c-1288">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1288">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="0448c-1289">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0448c-1289">Az.Dns</span></span>
* <span data-ttu-id="0448c-1290">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1290">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0448c-1291">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0448c-1291">Az.EventGrid</span></span>
* <span data-ttu-id="0448c-1292">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1292">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="0448c-1293">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="0448c-1293">New cmdlets:</span></span>
    - <span data-ttu-id="0448c-1294">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0448c-1294">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0448c-1295">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0448c-1295">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0448c-1296">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0448c-1296">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0448c-1297">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="0448c-1297">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="0448c-1298">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0448c-1298">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0448c-1299">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0448c-1299">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0448c-1300">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0448c-1300">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0448c-1301">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="0448c-1301">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0448c-1302">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0448c-1302">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0448c-1303">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0448c-1303">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="0448c-1304">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0448c-1304">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0448c-1305">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0448c-1305">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="0448c-1306">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0448c-1306">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="0448c-1307">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="0448c-1307">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="0448c-1308">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0448c-1308">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0448c-1309">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0448c-1309">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="0448c-1310">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-1310">Updated cmdlets:</span></span>
    - <span data-ttu-id="0448c-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="0448c-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="0448c-1312">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="0448c-1312">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0448c-1313">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="0448c-1313">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0448c-1314">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="0448c-1314">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="0448c-1315">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-1315">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="0448c-1316">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="0448c-1316">Event subscription expiration date,</span></span>
            - <span data-ttu-id="0448c-1317">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="0448c-1317">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="0448c-1318">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="0448c-1318">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="0448c-1319">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="0448c-1319">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="0448c-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="0448c-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="0448c-1321">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="0448c-1321">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="0448c-1322">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0448c-1322">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="0448c-1323">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="0448c-1323">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="0448c-1324">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="0448c-1324">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0448c-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0448c-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="0448c-1326">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0448c-1326">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="0448c-1327">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="0448c-1327">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="0448c-1328">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="0448c-1328">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="0448c-1329">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="0448c-1329">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-1330">Az.Network</span></span>
* <span data-ttu-id="0448c-1331">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="0448c-1331">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="0448c-1332">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1332">New cmdlets</span></span>
        - <span data-ttu-id="0448c-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="0448c-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="0448c-1334">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="0448c-1334">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="0448c-1335">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1335">New cmdlets</span></span>
        - <span data-ttu-id="0448c-1336">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0448c-1336">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="0448c-1337">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="0448c-1337">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="0448c-1338">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1338">New cmdlets</span></span>
        - <span data-ttu-id="0448c-1339">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0448c-1339">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0448c-1340">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0448c-1340">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0448c-1341">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0448c-1341">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0448c-1342">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-1342">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="0448c-1343">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-1343">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0448c-1344">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="0448c-1344">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="0448c-1345">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1345">New cmdlets</span></span>
        - <span data-ttu-id="0448c-1346">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0448c-1346">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0448c-1347">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0448c-1347">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0448c-1348">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0448c-1348">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0448c-1349">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0448c-1349">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="0448c-1350">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="0448c-1350">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="0448c-1351">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1351">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="0448c-1352">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1352">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="0448c-1353">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1353">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="0448c-1354">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1354">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="0448c-1355">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1355">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="0448c-1356">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1356">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="0448c-1357">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1357">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="0448c-1358">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1358">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="0448c-1359">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1359">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="0448c-1360">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1360">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="0448c-1361">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1361">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="0448c-1362">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1362">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="0448c-1363">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1363">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="0448c-1364">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-1364">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0448c-1365">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1365">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="0448c-1366">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1366">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="0448c-1367">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="0448c-1367">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="0448c-1368">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0448c-1368">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="0448c-1369">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1369">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="0448c-1370">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1370">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0448c-1371">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1371">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0448c-1372">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1372">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0448c-1373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-1373">Az.OperationalInsights</span></span>
* <span data-ttu-id="0448c-1374">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1374">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1375">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1375">Az.Resources</span></span>
* <span data-ttu-id="0448c-1376">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="0448c-1376">Support for additional Template Export options</span></span>
    - <span data-ttu-id="0448c-1377">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1377">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0448c-1378">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1378">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0448c-1379">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1379">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0448c-1380">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0448c-1380">Az.ServiceFabric</span></span>
* <span data-ttu-id="0448c-1381">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1381">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1382">Az.Sql</span></span>
* <span data-ttu-id="0448c-1383">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1383">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="0448c-1384">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1384">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="0448c-1385">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1385">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="0448c-1386">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0448c-1386">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0448c-1387">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0448c-1387">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0448c-1388">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0448c-1388">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0448c-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0448c-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="0448c-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0448c-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-1391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-1391">Az.Storage</span></span>
* <span data-ttu-id="0448c-1392">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="0448c-1392">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="0448c-1393">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-1393">New-AzStorageAccount</span></span>
* <span data-ttu-id="0448c-1394">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1394">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="0448c-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0448c-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-1396">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-1396">Az.Websites</span></span>
* <span data-ttu-id="0448c-1397">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="0448c-1397">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="0448c-1398">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="0448c-1398">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="0448c-1399">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1399">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="0448c-1400">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0448c-1400">Az.Cdn</span></span>
* <span data-ttu-id="0448c-1401">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1401">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1402">Az.Compute</span></span>
* <span data-ttu-id="0448c-1403">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1403">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="0448c-1404">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0448c-1404">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0448c-1405">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0448c-1405">Az.EventHub</span></span>
* <span data-ttu-id="0448c-1406">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0448c-1406">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="0448c-1407">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0448c-1407">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-1408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-1408">Az.Network</span></span>
* <span data-ttu-id="0448c-1409">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1409">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="0448c-1410">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1410">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0448c-1411">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-1411">Az.PolicyInsights</span></span>
* <span data-ttu-id="0448c-1412">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1412">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-1413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1413">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-1414">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1414">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0448c-1415">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0448c-1415">Az.ServiceBus</span></span>
* <span data-ttu-id="0448c-1416">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="0448c-1416">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0448c-1417">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0448c-1417">Az.ServiceFabric</span></span>
* <span data-ttu-id="0448c-1418">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1418">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="0448c-1419">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1419">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1420">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1420">Az.Sql</span></span>
* <span data-ttu-id="0448c-1421">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1421">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="0448c-1422">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-1422">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0448c-1423">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-1423">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="0448c-1424">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1424">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-1425">Az.Websites</span></span>
* <span data-ttu-id="0448c-1426">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1426">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="0448c-1427">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1427">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0448c-1428">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0448c-1428">Az.ApiManagement</span></span>
* <span data-ttu-id="0448c-1429">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-1429">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="0448c-1430">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="0448c-1430">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="0448c-1431">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="0448c-1431">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="0448c-1432">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="0448c-1432">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="0448c-1433">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0448c-1433">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="0448c-1434">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="0448c-1434">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="0448c-1435">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="0448c-1435">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="0448c-1436">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="0448c-1436">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="0448c-1437">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-1437">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="0448c-1438">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="0448c-1438">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="0448c-1439">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="0448c-1439">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="0448c-1440">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="0448c-1440">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="0448c-1441">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="0448c-1441">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="0448c-1442">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-1442">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="0448c-1443">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="0448c-1443">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="0448c-1444">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="0448c-1444">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="0448c-1445">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="0448c-1445">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="0448c-1446">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="0448c-1446">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="0448c-1447">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="0448c-1447">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="0448c-1448">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="0448c-1448">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="0448c-1449">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-1449">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="0448c-1450">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="0448c-1450">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="0448c-1451">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="0448c-1451">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="0448c-1452">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1452">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="0448c-1453">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1453">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="0448c-1454">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1454">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="0448c-1455">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0448c-1455">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="0448c-1456">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0448c-1456">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="0448c-1457">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1457">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="0448c-1458">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1458">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="0448c-1459">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1459">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="0448c-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="0448c-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="0448c-1461">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1461">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="0448c-1462">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1462">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0448c-1463">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="0448c-1463">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="0448c-1464">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="0448c-1464">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="0448c-1465">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="0448c-1465">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="0448c-1466">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1466">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="0448c-1467">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1467">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="0448c-1468">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1468">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0448c-1469">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="0448c-1469">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0448c-1470">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="0448c-1470">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="0448c-1471">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="0448c-1471">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="0448c-1472">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="0448c-1472">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="0448c-1473">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1473">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0448c-1474">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="0448c-1474">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0448c-1475">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="0448c-1475">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="0448c-1476">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="0448c-1476">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="0448c-1477">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1477">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="0448c-1478">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="0448c-1478">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="0448c-1479">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="0448c-1479">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="0448c-1480">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="0448c-1480">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="0448c-1481">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="0448c-1481">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="0448c-1482">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1482">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="0448c-1483">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="0448c-1483">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="0448c-1484">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="0448c-1484">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="0448c-1485">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1485">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0448c-1486">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="0448c-1486">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0448c-1487">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="0448c-1487">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0448c-1488">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1488">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0448c-1489">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1489">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0448c-1490">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="0448c-1490">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0448c-1491">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="0448c-1491">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0448c-1492">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1492">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0448c-1493">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1493">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="0448c-1494">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="0448c-1494">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="0448c-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="0448c-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="0448c-1496">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="0448c-1496">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="0448c-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="0448c-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="0448c-1498">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0448c-1498">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="0448c-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="0448c-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="0448c-1500">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="0448c-1500">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="0448c-1501">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="0448c-1501">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="0448c-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="0448c-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="0448c-1503">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="0448c-1503">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="0448c-1504">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0448c-1504">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="0448c-1505">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="0448c-1505">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0448c-1506">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0448c-1506">Az.Automation</span></span>
* <span data-ttu-id="0448c-1507">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1507">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="0448c-1508">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1508">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="0448c-1509">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1509">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="0448c-1510">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1510">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="0448c-1511">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1511">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="0448c-1512">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1512">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="0448c-1513">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-1513">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1514">Az.Compute</span></span>
* <span data-ttu-id="0448c-1515">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1515">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="0448c-1516">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="0448c-1516">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-1517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-1517">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-1518">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1518">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0448c-1519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-1519">Az.Monitor</span></span>
* <span data-ttu-id="0448c-1520">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1520">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-1521">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-1521">Az.Network</span></span>
* <span data-ttu-id="0448c-1522">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1522">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="0448c-1523">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0448c-1523">Updated cmdlet:</span></span>
        - <span data-ttu-id="0448c-1524">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="0448c-1524">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="0448c-1525">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1525">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1526">Az.Resources</span></span>
* <span data-ttu-id="0448c-1527">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1527">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1528">Az.Sql</span></span>
* <span data-ttu-id="0448c-1529">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0448c-1529">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="0448c-1530">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1530">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0448c-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-1531">Az.Accounts</span></span>
* <span data-ttu-id="0448c-1532">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="0448c-1532">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0448c-1533">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1533">Az.CognitiveServices</span></span>
* <span data-ttu-id="0448c-1534">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="0448c-1534">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="0448c-1535">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="0448c-1535">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1536">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1536">Az.Compute</span></span>
* <span data-ttu-id="0448c-1537">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="0448c-1537">Proximity placement group feature.</span></span>
    - <span data-ttu-id="0448c-1538">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0448c-1538">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="0448c-1539">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-1539">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="0448c-1540">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1540">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="0448c-1541">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="0448c-1541">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="0448c-1542">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1542">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="0448c-1543">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0448c-1543">Breaking changes</span></span>
    - <span data-ttu-id="0448c-1544">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1544">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="0448c-1545">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1545">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0448c-1546">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0448c-1546">Az.DeploymentManager</span></span>
* <span data-ttu-id="0448c-1547">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="0448c-1547">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="0448c-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0448c-1548">Az.Dns</span></span>
* <span data-ttu-id="0448c-1549">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="0448c-1549">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="0448c-1550">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="0448c-1550">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="0448c-1551">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="0448c-1551">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0448c-1552">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0448c-1552">Az.FrontDoor</span></span>
* <span data-ttu-id="0448c-1553">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="0448c-1553">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="0448c-1554">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="0448c-1554">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="0448c-1555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0448c-1555">Az.HDInsight</span></span>
* <span data-ttu-id="0448c-1556">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="0448c-1556">Removed two cmdlets:</span></span>
    - <span data-ttu-id="0448c-1557">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0448c-1557">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="0448c-1558">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0448c-1558">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0448c-1559">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1559">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0448c-1560">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="0448c-1560">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="0448c-1561">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="0448c-1561">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="0448c-1562">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="0448c-1562">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0448c-1563">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-1563">Az.Monitor</span></span>
* <span data-ttu-id="0448c-1564">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1564">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="0448c-1565">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="0448c-1565">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="0448c-1566">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="0448c-1566">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="0448c-1567">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="0448c-1567">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="0448c-1568">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="0448c-1568">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="0448c-1569">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="0448c-1569">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="0448c-1570">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="0448c-1570">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="0448c-1571">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0448c-1571">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0448c-1572">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0448c-1572">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0448c-1573">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0448c-1573">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0448c-1574">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0448c-1574">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0448c-1575">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0448c-1575">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0448c-1576">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="0448c-1576">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="0448c-1577">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1577">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-1578">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-1578">Az.Network</span></span>
* <span data-ttu-id="0448c-1579">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="0448c-1579">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="0448c-1580">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1580">New cmdlets</span></span>
        - <span data-ttu-id="0448c-1581">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0448c-1581">New-AzNatGateway</span></span>
        - <span data-ttu-id="0448c-1582">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0448c-1582">Get-AzNatGateway</span></span>
        - <span data-ttu-id="0448c-1583">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0448c-1583">Set-AzNatGateway</span></span>
        - <span data-ttu-id="0448c-1584">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0448c-1584">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="0448c-1585">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1585">Updated cmdlets</span></span>
        - <span data-ttu-id="0448c-1586">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0448c-1586">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="0448c-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0448c-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="0448c-1588">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="0448c-1588">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="0448c-1589">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1589">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="0448c-1590">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1590">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0448c-1591">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-1591">Az.PolicyInsights</span></span>
* <span data-ttu-id="0448c-1592">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-1592">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="0448c-1593">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0448c-1593">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="0448c-1594">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="0448c-1594">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-1595">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1595">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-1596">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-1596">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="0448c-1597">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="0448c-1597">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="0448c-1598">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="0448c-1598">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="0448c-1599">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="0448c-1599">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="0448c-1600">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="0448c-1600">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="0448c-1601">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="0448c-1601">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="0448c-1602">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0448c-1602">Az.Relay</span></span>
* <span data-ttu-id="0448c-1603">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="0448c-1603">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0448c-1604">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0448c-1604">Az.ServiceBus</span></span>
* <span data-ttu-id="0448c-1605">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1605">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-1606">Az.Storage</span></span>
* <span data-ttu-id="0448c-1607">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="0448c-1607">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="0448c-1608">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0448c-1608">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="0448c-1609">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="0448c-1609">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="0448c-1610">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-1610">New-AzStorageAccount</span></span>
* <span data-ttu-id="0448c-1611">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="0448c-1611">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="0448c-1612">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-1612">New-AzStorageAccount</span></span>
    - <span data-ttu-id="0448c-1613">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-1613">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="0448c-1614">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-1614">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-1615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-1615">Az.Websites</span></span>
* <span data-ttu-id="0448c-1616">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="0448c-1616">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="0448c-1617">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1617">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="0448c-1618">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1618">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0448c-1619">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0448c-1619">Highlights since the last major release</span></span>
* <span data-ttu-id="0448c-1620">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-1620">General availability of `Az` module</span></span>
* <span data-ttu-id="0448c-1621">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0448c-1621">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0448c-1622">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0448c-1622">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0448c-1623">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1623">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0448c-1624">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1624">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0448c-1625">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1625">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0448c-1626">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1626">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0448c-1627">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-1627">Az.Accounts</span></span>
* <span data-ttu-id="0448c-1628">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1628">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0448c-1629">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0448c-1629">Az.Batch</span></span>
* <span data-ttu-id="0448c-1630">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0448c-1631">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0448c-1631">Az.Cdn</span></span>
* <span data-ttu-id="0448c-1632">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0448c-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="0448c-1634">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1634">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1635">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1635">Az.Compute</span></span>
* <span data-ttu-id="0448c-1636">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1636">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="0448c-1637">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0448c-1638">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1638">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-1639">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-1639">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-1640">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1640">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-1641">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-1641">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-1642">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0448c-1643">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0448c-1643">Az.EventGrid</span></span>
* <span data-ttu-id="0448c-1644">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1644">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0448c-1645">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0448c-1645">Az.EventHub</span></span>
* <span data-ttu-id="0448c-1646">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1646">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0448c-1647">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0448c-1647">Az.HDInsight</span></span>
* <span data-ttu-id="0448c-1648">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0448c-1649">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0448c-1649">Az.IotHub</span></span>
* <span data-ttu-id="0448c-1650">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0448c-1651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0448c-1651">Az.KeyVault</span></span>
* <span data-ttu-id="0448c-1652">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0448c-1653">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1653">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0448c-1654">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0448c-1654">Az.MachineLearning</span></span>
* <span data-ttu-id="0448c-1655">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1655">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="0448c-1656">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0448c-1656">Az.Media</span></span>
* <span data-ttu-id="0448c-1657">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1657">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0448c-1658">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-1658">Az.Monitor</span></span>
  * <span data-ttu-id="0448c-1659">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1659">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="0448c-1660">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0448c-1660">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="0448c-1661">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0448c-1661">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="0448c-1662">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0448c-1662">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0448c-1663">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0448c-1663">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0448c-1664">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0448c-1664">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="0448c-1665">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1665">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-1666">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-1666">Az.Network</span></span>
* <span data-ttu-id="0448c-1667">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1667">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0448c-1668">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1668">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="0448c-1669">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0448c-1669">Az.NotificationHubs</span></span>
* <span data-ttu-id="0448c-1670">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1670">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0448c-1671">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-1671">Az.OperationalInsights</span></span>
* <span data-ttu-id="0448c-1672">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="0448c-1673">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0448c-1673">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="0448c-1674">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1674">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-1675">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1675">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-1676">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0448c-1677">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="0448c-1677">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="0448c-1678">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1678">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="0448c-1679">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1679">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0448c-1680">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0448c-1680">Az.RedisCache</span></span>
* <span data-ttu-id="0448c-1681">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1681">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1682">Az.Resources</span></span>
* <span data-ttu-id="0448c-1683">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1683">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1684">Az.Sql</span></span>
* <span data-ttu-id="0448c-1685">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1685">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="0448c-1686">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1686">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0448c-1687">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1687">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="0448c-1688">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1688">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="0448c-1689">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1689">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="0448c-1690">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-1690">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="0448c-1691">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1691">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-1692">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-1692">Az.Websites</span></span>
* <span data-ttu-id="0448c-1693">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1693">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="0448c-1694">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0448c-1695">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1695">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="0448c-1696">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0448c-1696">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="0448c-1697">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1697">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0448c-1698">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0448c-1698">Highlights since the last major release</span></span>
* <span data-ttu-id="0448c-1699">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-1699">General availability of `Az` module</span></span>
* <span data-ttu-id="0448c-1700">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0448c-1700">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0448c-1701">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0448c-1701">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0448c-1702">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1702">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0448c-1703">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1703">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0448c-1704">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1704">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0448c-1705">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1705">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0448c-1706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-1706">Az.Accounts</span></span>
* <span data-ttu-id="0448c-1707">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1707">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0448c-1708">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1708">Az.AnalysisServices</span></span>
* <span data-ttu-id="0448c-1709">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0448c-1709">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="0448c-1710">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="0448c-1710">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0448c-1711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0448c-1711">Az.Automation</span></span>
* <span data-ttu-id="0448c-1712">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1712">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="0448c-1713">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-1713">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="0448c-1714">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0448c-1714">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1715">Az.Compute</span></span>
* <span data-ttu-id="0448c-1716">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1716">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0448c-1717">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1717">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="0448c-1718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0448c-1718">Az.ContainerInstance</span></span>
* <span data-ttu-id="0448c-1719">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1719">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-1720">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-1720">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-1721">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1721">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="0448c-1722">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1722">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1723">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1723">Az.Resources</span></span>
* <span data-ttu-id="0448c-1724">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1724">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="0448c-1725">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1725">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="0448c-1726">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1726">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="0448c-1727">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0448c-1727">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="0448c-1728">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1728">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="0448c-1729">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0448c-1729">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1730">Az.Sql</span></span>
* <span data-ttu-id="0448c-1731">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-1731">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-1732">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-1732">Az.Storage</span></span>
* <span data-ttu-id="0448c-1733">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="0448c-1733">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="0448c-1734">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0448c-1734">New-AzStorageContext</span></span>
* <span data-ttu-id="0448c-1735">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="0448c-1735">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="0448c-1736">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0448c-1736">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0448c-1737">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0448c-1737">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0448c-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0448c-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="0448c-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0448c-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="0448c-1740">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="0448c-1740">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="0448c-1741">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0448c-1741">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0448c-1742">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0448c-1742">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0448c-1743">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0448c-1743">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="0448c-1744">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0448c-1744">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="0448c-1745">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1745">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0448c-1746">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0448c-1746">Highlights since the last major release</span></span>
* <span data-ttu-id="0448c-1747">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-1747">General availability of `Az` module</span></span>
* <span data-ttu-id="0448c-1748">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0448c-1748">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0448c-1749">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0448c-1749">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0448c-1750">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1750">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0448c-1751">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1751">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0448c-1752">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1752">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0448c-1753">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1753">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0448c-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0448c-1754">Az.Automation</span></span>
* <span data-ttu-id="0448c-1755">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="0448c-1755">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="0448c-1756">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="0448c-1756">Dynamic grouping</span></span>
    * <span data-ttu-id="0448c-1757">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="0448c-1757">Pre-Post script</span></span>
    * <span data-ttu-id="0448c-1758">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="0448c-1758">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1759">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1759">Az.Compute</span></span>
* <span data-ttu-id="0448c-1760">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="0448c-1760">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="0448c-1761">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1761">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0448c-1762">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0448c-1762">Az.KeyVault</span></span>
* <span data-ttu-id="0448c-1763">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1763">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-1764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-1764">Az.Network</span></span>
* <span data-ttu-id="0448c-1765">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1765">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="0448c-1766">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1766">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-1767">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1767">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-1768">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1768">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="0448c-1769">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1769">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1770">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1770">Az.Resources</span></span>
* <span data-ttu-id="0448c-1771">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1771">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="0448c-1772">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1772">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1773">Az.Sql</span></span>
* <span data-ttu-id="0448c-1774">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1774">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-1775">Az.Storage</span></span>
* <span data-ttu-id="0448c-1776">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="0448c-1776">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="0448c-1777">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0448c-1777">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0448c-1778">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0448c-1778">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0448c-1779">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0448c-1779">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0448c-1780">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0448c-1780">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="0448c-1781">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="0448c-1781">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="0448c-1782">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0448c-1782">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-1783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-1783">Az.Websites</span></span>
* <span data-ttu-id="0448c-1784">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1784">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="0448c-1785">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1785">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0448c-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-1786">Az.Accounts</span></span>
* <span data-ttu-id="0448c-1787">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1787">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="0448c-1788">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1788">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0448c-1789">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0448c-1789">Az.Automation</span></span>
* <span data-ttu-id="0448c-1790">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1790">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="0448c-1791">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1791">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="0448c-1792">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="0448c-1792">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0448c-1793">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0448c-1793">Az.Cdn</span></span>
* <span data-ttu-id="0448c-1794">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-1794">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1795">Az.Compute</span></span>
* <span data-ttu-id="0448c-1796">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1796">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-1797">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-1797">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-1798">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1798">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0448c-1799">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0448c-1799">Az.LogicApp</span></span>
* <span data-ttu-id="0448c-1800">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="0448c-1800">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-1801">Az.Network</span></span>
* <span data-ttu-id="0448c-1802">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1802">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-1803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1803">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-1804">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1804">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="0448c-1805">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="0448c-1805">SDK Update</span></span>
* <span data-ttu-id="0448c-1806">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-1806">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="0448c-1807">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1807">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1808">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1808">Az.Resources</span></span>
* <span data-ttu-id="0448c-1809">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1809">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="0448c-1810">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="0448c-1810">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="0448c-1811">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1811">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="0448c-1812">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="0448c-1812">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="0448c-1813">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1813">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="0448c-1814">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="0448c-1814">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1815">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1815">Az.Sql</span></span>
* <span data-ttu-id="0448c-1816">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-1816">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="0448c-1817">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-1817">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-1818">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-1818">Az.Storage</span></span>
* <span data-ttu-id="0448c-1819">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0448c-1819">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="0448c-1820">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1820">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="0448c-1821">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1821">Az.AnalysisServices</span></span>
* <span data-ttu-id="0448c-1822">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-1822">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0448c-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0448c-1823">Az.Automation</span></span>
* <span data-ttu-id="0448c-1824">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1824">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="0448c-1825">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1825">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="0448c-1826">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1826">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0448c-1827">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1827">Az.CognitiveServices</span></span>
* <span data-ttu-id="0448c-1828">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1828">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1829">Az.Compute</span></span>
* <span data-ttu-id="0448c-1830">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1830">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="0448c-1831">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1831">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="0448c-1832">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1832">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="0448c-1833">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="0448c-1833">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-1834">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-1834">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-1835">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1835">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0448c-1836">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0448c-1836">Az.EventHub</span></span>
* <span data-ttu-id="0448c-1837">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1837">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0448c-1838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0448c-1838">Az.KeyVault</span></span>
* <span data-ttu-id="0448c-1839">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1839">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0448c-1840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0448c-1840">Az.LogicApp</span></span>
* <span data-ttu-id="0448c-1841">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1841">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="0448c-1842">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1842">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="0448c-1843">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1843">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="0448c-1844">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0448c-1844">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0448c-1845">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0448c-1845">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0448c-1846">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0448c-1846">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0448c-1847">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0448c-1847">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="0448c-1848">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0448c-1848">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="0448c-1849">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0448c-1849">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0448c-1850">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0448c-1850">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0448c-1851">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0448c-1851">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0448c-1852">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0448c-1852">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="0448c-1853">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1853">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0448c-1854">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-1854">Az.Monitor</span></span>
* <span data-ttu-id="0448c-1855">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1855">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-1856">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-1856">Az.Network</span></span>
* <span data-ttu-id="0448c-1857">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1857">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0448c-1858">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-1858">Az.OperationalInsights</span></span>
* <span data-ttu-id="0448c-1859">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="0448c-1859">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="0448c-1860">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1860">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="0448c-1861">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1861">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1862">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1862">Az.Resources</span></span>
* <span data-ttu-id="0448c-1863">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1863">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0448c-1864">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1864">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="0448c-1865">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1865">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="0448c-1866">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1866">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1867">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1867">Az.Sql</span></span>
* <span data-ttu-id="0448c-1868">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1868">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="0448c-1869">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1869">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-1870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-1870">Az.Websites</span></span>
* <span data-ttu-id="0448c-1871">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1871">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="0448c-1872">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1872">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0448c-1873">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-1873">Az.Accounts</span></span>
* <span data-ttu-id="0448c-1874">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0448c-1874">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0448c-1875">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1875">Az.AnalysisServices</span></span>
<span data-ttu-id="0448c-1876">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="0448c-1876">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1877">Az.Compute</span></span>
* <span data-ttu-id="0448c-1878">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1878">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="0448c-1879">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1879">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="0448c-1880">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1880">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-1881">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1881">Az.RecoveryServices</span></span>
<span data-ttu-id="0448c-1882">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="0448c-1882">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1883">Az.Resources</span></span>
* <span data-ttu-id="0448c-1884">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1884">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="0448c-1885">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0448c-1885">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0448c-1886">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1886">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="0448c-1887">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0448c-1887">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1888">Az.Sql</span></span>
* <span data-ttu-id="0448c-1889">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0448c-1889">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="0448c-1890">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1890">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="0448c-1891">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1891">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="0448c-1892">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1892">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0448c-1893">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-1893">Az.Accounts</span></span>
* <span data-ttu-id="0448c-1894">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="0448c-1894">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0448c-1895">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1895">Az.AnalysisServices</span></span>
* <span data-ttu-id="0448c-1896">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="0448c-1896">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-1897">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-1897">Az.RecoveryServices</span></span>
* <span data-ttu-id="0448c-1898">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="0448c-1898">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="0448c-1899">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1899">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0448c-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-1900">Az.Accounts</span></span>
* <span data-ttu-id="0448c-1901">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1901">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0448c-1902">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1902">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0448c-1903">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1903">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="0448c-1904">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0448c-1904">Az.Aks</span></span>
* <span data-ttu-id="0448c-1905">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1905">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0448c-1906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0448c-1906">Az.Automation</span></span>
* <span data-ttu-id="0448c-1907">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1907">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="0448c-1908">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1908">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0448c-1909">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0448c-1909">Az.Cdn</span></span>
* <span data-ttu-id="0448c-1910">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1910">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1911">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1911">Az.Compute</span></span>
* <span data-ttu-id="0448c-1912">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1912">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="0448c-1913">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1913">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="0448c-1914">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1914">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0448c-1915">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0448c-1915">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0448c-1916">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1916">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0448c-1917">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0448c-1917">Az.DataFactory</span></span>
* <span data-ttu-id="0448c-1918">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1918">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-1920">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1920">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="0448c-1921">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="0448c-1921">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="0448c-1922">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1922">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0448c-1923">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0448c-1923">Az.IotHub</span></span>
* <span data-ttu-id="0448c-1924">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1924">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0448c-1925">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0448c-1925">Az.KeyVault</span></span>
* <span data-ttu-id="0448c-1926">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1926">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-1927">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-1927">Az.Network</span></span>
* <span data-ttu-id="0448c-1928">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1928">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1929">Az.Resources</span></span>
* <span data-ttu-id="0448c-1930">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1930">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="0448c-1931">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1931">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="0448c-1932">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1932">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="0448c-1933">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1933">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="0448c-1934">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1934">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="0448c-1935">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1935">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="0448c-1936">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="0448c-1936">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0448c-1937">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0448c-1937">Az.ServiceFabric</span></span>
* <span data-ttu-id="0448c-1938">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="0448c-1938">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="0448c-1939">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1939">Fix some error messages.</span></span>
* <span data-ttu-id="0448c-1940">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1940">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="0448c-1941">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1941">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0448c-1942">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0448c-1942">Az.SignalR</span></span>
* <span data-ttu-id="0448c-1943">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1943">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1944">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1944">Az.Sql</span></span>
* <span data-ttu-id="0448c-1945">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1945">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0448c-1946">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1946">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="0448c-1947">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1947">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="0448c-1948">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="0448c-1948">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-1949">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-1949">Az.Storage</span></span>
* <span data-ttu-id="0448c-1950">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1950">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0448c-1951">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-1951">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="0448c-1952">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="0448c-1952">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="0448c-1953">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0448c-1953">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="0448c-1954">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0448c-1954">Az.TrafficManager</span></span>
* <span data-ttu-id="0448c-1955">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1955">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-1956">Az.Websites</span></span>
* <span data-ttu-id="0448c-1957">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1957">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0448c-1958">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1958">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="0448c-1959">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1959">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="0448c-1960">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="0448c-1960">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0448c-1961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-1961">Az.Accounts</span></span>
* <span data-ttu-id="0448c-1962">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-1962">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-1963">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-1963">Az.Compute</span></span>
* <span data-ttu-id="0448c-1964">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="0448c-1964">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="0448c-1965">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1965">Updated the description of ID in help files</span></span>
* <span data-ttu-id="0448c-1966">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="0448c-1966">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-1967">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-1967">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-1968">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1968">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="0448c-1969">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1969">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0448c-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0448c-1970">Az.EventGrid</span></span>
* <span data-ttu-id="0448c-1971">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1971">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="0448c-1972">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1972">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="0448c-1973">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-1973">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0448c-1974">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="0448c-1974">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0448c-1975">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="0448c-1975">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0448c-1976">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="0448c-1976">Dead letter endpoint.</span></span>
    - <span data-ttu-id="0448c-1977">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-1977">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0448c-1978">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="0448c-1978">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0448c-1979">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="0448c-1979">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0448c-1980">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="0448c-1980">Dead letter endpoint.</span></span>
* <span data-ttu-id="0448c-1981">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-1981">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="0448c-1982">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-1982">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0448c-1983">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0448c-1983">Az.IotHub</span></span>
* <span data-ttu-id="0448c-1984">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1984">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0448c-1985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0448c-1985">Az.LogicApp</span></span>
* <span data-ttu-id="0448c-1986">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="0448c-1986">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-1987">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-1987">Az.Resources</span></span>
* <span data-ttu-id="0448c-1988">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1988">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="0448c-1989">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="0448c-1989">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="0448c-1990">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1990">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0448c-1991">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1991">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="0448c-1992">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-1992">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="0448c-1993">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="0448c-1993">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0448c-1994">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0448c-1994">Az.SignalR</span></span>
* <span data-ttu-id="0448c-1995">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="0448c-1995">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-1996">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-1996">Az.Sql</span></span>
* <span data-ttu-id="0448c-1997">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="0448c-1997">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0448c-1998">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-1998">Az.Storage</span></span>
* <span data-ttu-id="0448c-1999">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="0448c-1999">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="0448c-2000">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0448c-2000">New-AzStorageContext</span></span>
* <span data-ttu-id="0448c-2001">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2001">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="0448c-2002">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0448c-2002">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-2003">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-2003">Az.Websites</span></span>
* <span data-ttu-id="0448c-2004">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2004">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="0448c-2005">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="0448c-2005">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="0448c-2006">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="0448c-2006">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="0448c-2007">Genel</span><span class="sxs-lookup"><span data-stu-id="0448c-2007">General</span></span>

- <span data-ttu-id="0448c-2008">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-2008">General Availability of Az Module</span></span>
- <span data-ttu-id="0448c-2009">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="0448c-2009">Online help for each module</span></span>
- <span data-ttu-id="0448c-2010">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="0448c-2010">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="0448c-2011">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2011">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="0448c-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0448c-2012">Az.Accounts</span></span>
- <span data-ttu-id="0448c-2013">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0448c-2013">Changed from Az.Profile</span></span>
- <span data-ttu-id="0448c-2014">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2014">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0448c-2015">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0448c-2015">Az.ApiManagement</span></span>
- <span data-ttu-id="0448c-2016">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="0448c-2016">Fixes for #7002</span></span>
- <span data-ttu-id="0448c-2017">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2017">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="0448c-2018">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0448c-2018">Az.Batch</span></span>
- <span data-ttu-id="0448c-2019">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2019">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="0448c-2020">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="0448c-2020">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="0448c-2021">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="0448c-2022">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0448c-2022">Az.Billing</span></span>
- <span data-ttu-id="0448c-2023">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2023">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="0448c-2024">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="0448c-2024">Az.CognitivServices</span></span>
- <span data-ttu-id="0448c-2025">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2025">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="0448c-2026">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-2026">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0448c-2027">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0448c-2027">Az.ContainerInstance</span></span>
- <span data-ttu-id="0448c-2028">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2028">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="0448c-2029">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0448c-2029">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="0448c-2030">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2030">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0448c-2031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-2031">Az.DataLakeStore</span></span>
- <span data-ttu-id="0448c-2032">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2032">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="0448c-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0448c-2033">Az.Monitor</span></span>
- <span data-ttu-id="0448c-2034">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2034">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="0448c-2035">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0448c-2035">Az.KeyVault</span></span>
- <span data-ttu-id="0448c-2036">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-2036">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="0448c-2037">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0448c-2037">Az.MachineLearning</span></span>
- <span data-ttu-id="0448c-2038">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2038">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="0448c-2039">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0448c-2039">Az.Media</span></span>
- <span data-ttu-id="0448c-2040">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0448c-2040">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0448c-2041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-2041">Az.Network</span></span>
<span data-ttu-id="0448c-2042">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2042">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="0448c-2043">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0448c-2043">New cmdlets added:</span></span>
        - <span data-ttu-id="0448c-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0448c-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0448c-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0448c-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0448c-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0448c-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0448c-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0448c-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0448c-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0448c-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0448c-2049">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0448c-2049">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="0448c-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0448c-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="0448c-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0448c-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="0448c-2052">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2052">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="0448c-2053">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0448c-2053">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="0448c-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0448c-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0448c-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0448c-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0448c-2056">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-2056">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="0448c-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="0448c-2058">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="0448c-2059">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2059">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="0448c-2060">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0448c-2060">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0448c-2061">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0448c-2061">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0448c-2062">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0448c-2062">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="0448c-2063">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2063">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="0448c-2064">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2064">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="0448c-2065">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-2065">Az.OperationalInsights</span></span>
- <span data-ttu-id="0448c-2066">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2066">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="0448c-2067">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0448c-2067">Az.Profile</span></span>
- <span data-ttu-id="0448c-2068">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2068">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-2069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-2069">Az.RecoveryServices</span></span>
- <span data-ttu-id="0448c-2070">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2070">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="0448c-2071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-2071">Az.Resources</span></span>
- <span data-ttu-id="0448c-2072">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2072">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0448c-2073">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0448c-2073">Az.ServiceFabric</span></span>
- <span data-ttu-id="0448c-2074">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="0448c-2074">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="0448c-2075">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2075">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="0448c-2076">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0448c-2076">Az.SIgnalR</span></span>
- <span data-ttu-id="0448c-2077">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="0448c-2077">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="0448c-2078">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-2078">Az.Sql</span></span>
- <span data-ttu-id="0448c-2079">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2079">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="0448c-2080">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2080">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="0448c-2081">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="0448c-2082">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-2082">Az.Storage</span></span>
- <span data-ttu-id="0448c-2083">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2083">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0448c-2084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-2084">Az.Websites</span></span>
- <span data-ttu-id="0448c-2085">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0448c-2085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="0448c-2086">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="0448c-2086">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="0448c-2087">Genel</span><span class="sxs-lookup"><span data-stu-id="0448c-2087">General</span></span>

* <span data-ttu-id="0448c-2088">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0448c-2088">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="0448c-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-2089">Az.Compute</span></span>

* <span data-ttu-id="0448c-2090">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2090">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0448c-2091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-2091">Az.DataLakeStore</span></span>

* <span data-ttu-id="0448c-2092">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2092">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="0448c-2093">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0448c-2093">Az.FrontDoor</span></span>

* <span data-ttu-id="0448c-2094">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2094">Fixed some broken links</span></span>
    - <span data-ttu-id="0448c-2095">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2095">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="0448c-2096">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2096">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0448c-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0448c-2097">Az.RecoveryServices</span></span>

* <span data-ttu-id="0448c-2098">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2098">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="0448c-2099">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2099">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="0448c-2100">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-2100">Az.Resources</span></span>

* <span data-ttu-id="0448c-2101">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0448c-2101">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="0448c-2102">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2102">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="0448c-2103">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-2103">Az.Sql</span></span>

* <span data-ttu-id="0448c-2104">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0448c-2104">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="0448c-2105">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2105">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="0448c-2106">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2106">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="0448c-2107">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0448c-2107">Az.Storage</span></span>

* <span data-ttu-id="0448c-2108">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2108">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="0448c-2109">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2109">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="0448c-2110">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0448c-2110">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0448c-2111">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2111">Support Static Website configuration</span></span>
    - <span data-ttu-id="0448c-2112">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0448c-2112">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="0448c-2113">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0448c-2113">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0448c-2114">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-2114">Az.Websites</span></span>

* <span data-ttu-id="0448c-2115">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0448c-2115">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="0448c-2116">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2116">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="0448c-2117">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="0448c-2117">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="0448c-2118">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="0448c-2118">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0448c-2119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0448c-2119">Az.ApiManagement</span></span>
* <span data-ttu-id="0448c-2120">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="0448c-2120">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="0448c-2121">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0448c-2121">Az.Automation</span></span>
* <span data-ttu-id="0448c-2122">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="0448c-2122">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="0448c-2123">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2123">Added Update Management cmdlets</span></span>
* <span data-ttu-id="0448c-2124">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2124">Added Source Control cmdlets</span></span>
* <span data-ttu-id="0448c-2125">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2125">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="0448c-2126">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2126">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="0448c-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-2127">Az.Compute</span></span>
* <span data-ttu-id="0448c-2128">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2128">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="0448c-2129">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="0448c-2129">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0448c-2130">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0448c-2130">Az.ContainerInstance</span></span>
* <span data-ttu-id="0448c-2131">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="0448c-2131">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="0448c-2132">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0448c-2132">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0448c-2133">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2133">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0448c-2134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-2134">Az.Network</span></span>
* <span data-ttu-id="0448c-2135">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2135">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="0448c-2136">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2136">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="0448c-2137">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2137">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="0448c-2138">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2138">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="0448c-2139">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0448c-2139">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0448c-2140">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2140">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="0448c-2141">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="0448c-2141">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="0448c-2142">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0448c-2142">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0448c-2143">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2143">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="0448c-2144">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="0448c-2144">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="0448c-2145">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0448c-2145">Az.Relay</span></span>
* <span data-ttu-id="0448c-2146">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2146">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="0448c-2147">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-2147">Az.Resources</span></span>
* <span data-ttu-id="0448c-2148">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2148">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="0448c-2149">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2149">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="0448c-2150">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="0448c-2150">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0448c-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0448c-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="0448c-2152">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2152">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="0448c-2153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-2153">Az.Sql</span></span>
* <span data-ttu-id="0448c-2154">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2154">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="0448c-2155">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0448c-2155">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0448c-2156">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0448c-2156">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0448c-2157">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0448c-2157">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0448c-2158">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0448c-2158">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0448c-2159">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0448c-2159">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0448c-2160">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0448c-2160">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0448c-2161">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0448c-2161">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0448c-2162">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0448c-2162">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="0448c-2163">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2163">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="0448c-2164">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2164">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="0448c-2165">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2165">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="0448c-2166">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0448c-2166">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0448c-2167">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0448c-2167">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0448c-2168">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0448c-2168">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="0448c-2169">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0448c-2169">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="0448c-2170">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2170">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="0448c-2171">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="0448c-2171">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0448c-2172">Genel</span><span class="sxs-lookup"><span data-stu-id="0448c-2172">General</span></span>
* <span data-ttu-id="0448c-2173">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="0448c-2173">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="0448c-2174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0448c-2174">Az.Profile</span></span>
* <span data-ttu-id="0448c-2175">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2175">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="0448c-2176">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2176">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="0448c-2177">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2177">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="0448c-2178">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2178">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="0448c-2179">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2179">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="0448c-2180">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2180">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="0448c-2181">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2181">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="0448c-2182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0448c-2182">Az.CognitiveServices</span></span>
* <span data-ttu-id="0448c-2183">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2183">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-2184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-2184">Az.Compute</span></span>
* <span data-ttu-id="0448c-2185">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2185">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="0448c-2186">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="0448c-2186">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="0448c-2187">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2187">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-2188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-2188">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-2189">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2189">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="0448c-2190">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2190">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="0448c-2191">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="0448c-2191">Az.Insights</span></span>
* <span data-ttu-id="0448c-2192">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2192">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="0448c-2193">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="0448c-2193">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="0448c-2194">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2194">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="0448c-2195">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="0448c-2195">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-2196">Az.Network</span></span>
* <span data-ttu-id="0448c-2197">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="0448c-2197">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="0448c-2198">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0448c-2198">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="0448c-2199">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0448c-2199">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="0448c-2200">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0448c-2200">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="0448c-2201">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0448c-2201">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0448c-2202">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0448c-2202">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0448c-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0448c-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0448c-2204">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0448c-2204">Az.PolicyInsights</span></span>
* <span data-ttu-id="0448c-2205">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2205">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-2206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-2206">Az.Resources</span></span>
* <span data-ttu-id="0448c-2207">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0448c-2207">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="0448c-2208">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="0448c-2208">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0448c-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0448c-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="0448c-2210">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2210">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0448c-2211">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0448c-2211">Az.ServiceFabric</span></span>
* <span data-ttu-id="0448c-2212">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2212">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="0448c-2213">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2213">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="0448c-2214">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="0448c-2214">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="0448c-2215">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="0448c-2215">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="0448c-2216">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2216">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="0448c-2217">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="0448c-2217">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="0448c-2218">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0448c-2218">Az.Profile</span></span>
* <span data-ttu-id="0448c-2219">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="0448c-2219">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="0448c-2220">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2220">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-2221">Az.Compute</span></span>
* <span data-ttu-id="0448c-2222">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2222">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="0448c-2223">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2223">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0448c-2224">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0448c-2224">Az.DataLakeStore</span></span>
* <span data-ttu-id="0448c-2225">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="0448c-2225">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="0448c-2226">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="0448c-2226">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="0448c-2227">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="0448c-2227">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0448c-2228">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0448c-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0448c-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="0448c-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-2230">Az.Network</span></span>
* <span data-ttu-id="0448c-2231">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-2231">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="0448c-2232">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2232">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-2233">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-2233">Az.Resources</span></span>
* <span data-ttu-id="0448c-2234">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2234">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="0448c-2235">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="0448c-2235">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="0448c-2236">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="0448c-2236">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="0448c-2237">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="0448c-2237">Azure.Storage</span></span>
* <span data-ttu-id="0448c-2238">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="0448c-2238">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="0448c-2239">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0448c-2239">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="0448c-2240">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0448c-2240">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0448c-2241">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="0448c-2241">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="0448c-2242">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="0448c-2242">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0448c-2243">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0448c-2243">Az.CognitiveServices</span></span>
* <span data-ttu-id="0448c-2244">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="0448c-2244">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0448c-2245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0448c-2245">Az.Compute</span></span>
* <span data-ttu-id="0448c-2246">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2246">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="0448c-2247">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2247">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="0448c-2248">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2248">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="0448c-2249">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0448c-2249">Az.DataFactoryV2</span></span>
* <span data-ttu-id="0448c-2250">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2250">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0448c-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0448c-2251">Az.Network</span></span>
* <span data-ttu-id="0448c-2252">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0448c-2252">Added NetworkProfile functionality.</span></span> <span data-ttu-id="0448c-2253">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2253">new cmdlets added</span></span>
    - <span data-ttu-id="0448c-2254">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0448c-2254">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="0448c-2255">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0448c-2255">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="0448c-2256">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0448c-2256">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="0448c-2257">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0448c-2257">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="0448c-2258">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-2258">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="0448c-2259">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="0448c-2259">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="0448c-2260">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2260">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="0448c-2261">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2261">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="0448c-2262">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2262">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0448c-2263">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0448c-2263">Az.RedisCache</span></span>
* <span data-ttu-id="0448c-2264">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="0448c-2264">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="0448c-2265">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2265">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="0448c-2266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0448c-2266">Az.Resources</span></span>
* <span data-ttu-id="0448c-2267">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0448c-2267">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0448c-2268">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2268">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="0448c-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0448c-2269">Az.Sql</span></span>
* <span data-ttu-id="0448c-2270">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0448c-2270">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0448c-2271">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0448c-2271">Az.Websites</span></span>
* <span data-ttu-id="0448c-2272">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="0448c-2272">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="0448c-2273">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="0448c-2273">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="0448c-2274">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="0448c-2274">0.2.0 - September 2018</span></span>
 <span data-ttu-id="0448c-2275">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="0448c-2275">Initial Release</span></span>
