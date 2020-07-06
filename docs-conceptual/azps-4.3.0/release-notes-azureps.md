---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a9ec7589ab155553da29612096a607d82a078321
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85268370"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="36215-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="36215-103">Azure PowerShell release notes</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="36215-104">4.3.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="36215-104">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-105">Az.Accounts</span></span>
* <span data-ttu-id="36215-106">Ortam ayarını varsayılan olarak bulma ve 'Add-AzEnvironment' aracılığıyla ortam ekleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-106">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="36215-107">Önceden yüklenmiş bütünleştirilmiş kodlar güncelleştirildi [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="36215-107">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="36215-108">Azure.Core bütünleştirilmiş kodu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-108">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="36215-109">'Connect-AzAccount' cmdlet’inin çok iş parçacıklı yürütmede başarısız olmasına neden olabilen bir sorun düzeltildi [#11201]</span><span class="sxs-lookup"><span data-stu-id="36215-109">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="36215-110">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="36215-110">Az.Aks</span></span>
* <span data-ttu-id="36215-111">Eski [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)’sinin kullanımı [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) ve [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API’lerine yönelik çağrılarla değiştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-111">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36215-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36215-112">Az.Batch</span></span>
* <span data-ttu-id="36215-113">Az.Batch, 'Microsoft.Azure.Management.Batch' SDK sürüm 11.0.0 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-113">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="36215-114">BatchAccount.Identity özelliğini 'New-AzBatchAccount' cmdlet’ine ayarlama özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-114">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36215-115">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36215-115">Az.CognitiveServices</span></span>
* <span data-ttu-id="36215-116">Hesap özelliklerini görüntüleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-116">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="36215-117">PublicNetworkAccess özelliğinin değiştirilmesi desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-117">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-118">Az.Compute</span></span>
* <span data-ttu-id="36215-119">Set-AzVM ve Set-AzVmssVM cmdlet’lerine SimulateEviction parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-119">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="36215-120">New-AzGalleryImageVersion cmdlet’i için StorageAccountType parametresinin bağımsız değişken tamamlayıcısına 'Premium_LRS' eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-120">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="36215-121">VMCustomScriptExtension için Alt Durumlar eklendi [#11297]</span><span class="sxs-lookup"><span data-stu-id="36215-121">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="36215-122">New-AzVM ve New-AzVMConfig cmdlet’leri için EvictionPolicy parametresinin bağımsız değişken tamamlayıcısına 'Delete' eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-122">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="36215-123">SAP için yeni VM Uzantısı’nın adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-123">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-124">Az.DataFactory</span></span>
* <span data-ttu-id="36215-125">ADF .NET SDK’sı 4.9.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-125">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36215-126">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36215-126">Az.EventHub</span></span>
* <span data-ttu-id="36215-127">'New-AzEventHubNamespace' ve 'Set-AzEventHubNamespace' cmdlet’lerine Yönetilen Kimlik parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-127">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="36215-128">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="36215-128">Az.Functions</span></span>
* <span data-ttu-id="36215-129">PowerShell 7.0 ve Java 11 işlev uygulamaları oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-129">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36215-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36215-130">Az.HDInsight</span></span>
* <span data-ttu-id="36215-131">HDInsight kümesinin konaklarını listeleme ve belirli konaklarını yeniden başlatma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-131">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="36215-132">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="36215-132">Az.HealthcareApis</span></span>
* <span data-ttu-id="36215-133">SDK sürümü 1.1.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-133">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="36215-134">Dışarı aktarma ayarları ve Yönetilen Kimlik desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-134">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-135">Az.Monitor</span></span>
* <span data-ttu-id="36215-136">'Set-AzActivityLogAlert' için giriş nesnesi parametresi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-136">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="36215-137">'Set-AzActionGroup' için 'InputObject' parametresi düzeltildi [#10868]</span><span class="sxs-lookup"><span data-stu-id="36215-137">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-138">Az.Network</span></span>
* <span data-ttu-id="36215-139">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-139">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="36215-140">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-140">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="36215-141">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="36215-141">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="36215-142">Güvenlik Duvarı İlkesi için Ağ Kuralları’nda Hedef FQDN Desteği</span><span class="sxs-lookup"><span data-stu-id="36215-142">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="36215-143">Arka uç adres havuzu işlemlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-143">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="36215-144">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="36215-144">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="36215-145">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="36215-145">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="36215-146">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="36215-146">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="36215-147">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="36215-147">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="36215-148">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="36215-148">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="36215-149">'New-AzIpGroup' için ad doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-149">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="36215-150">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-150">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="36215-151">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="36215-151">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="36215-152">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde özel DNS sunucuları ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="36215-152">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="36215-153">New-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-153">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="36215-154">Update-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-154">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="36215-155">'Update-AzVpnGateway' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-155">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="36215-156">Müşterilerin özel BGP’lerini VpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-BgpPeeringAddress' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-156">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="36215-157">Bir VirtualHub kaynağının yönlendirme durumunu sıfırlamayı desteklemek amacıyla yeni cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-157">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="36215-158">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="36215-158">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="36215-159">Güvenlik Duvarı İlkesi’nde yapılan son Swagger değişikliğine göre aşağıdakiler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-159">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="36215-160">RuleGroup, RuleCollectionGroup ve RuleType adları değiştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-160">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="36215-161">Birden çok NAT Kural Koleksiyonu’nu desteklemek amacıyla Güvenlik Duvarı İlkesi NAT Kural Koleksiyonları’na yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-161">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="36215-162">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule' ve 'New-AzFirewallPolicyNetworkRule' için 'SourceIpGroup' zorunlu parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-162">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="36215-163">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-163">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="36215-164">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-164">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="36215-165">[Yeni Değişiklik] Şu zorunu parametreler kaldırıldı: 'New-AzFirewallPolicyNatRuleCollection' için 'TranslatedAddress', 'TranslatedPort'.</span><span class="sxs-lookup"><span data-stu-id="36215-165">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="36215-166">Application Gateway üzerinde PrivateLink’i destekleyecek yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-166">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="36215-167">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36215-167">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="36215-168">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36215-168">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="36215-169">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36215-169">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="36215-170">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36215-170">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="36215-171">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36215-171">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="36215-172">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36215-172">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="36215-173">VirtualHub’ın HubRouteTables alt kaynağı için yeni cmdlet’ler eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-173">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="36215-174">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="36215-174">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="36215-175">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="36215-175">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="36215-176">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="36215-176">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="36215-177">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="36215-177">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="36215-178">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="36215-178">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="36215-179">Mevcut cmdlet’ler VirtualWan’deki özel yönlendirmede isteğe bağlı RoutingConfiguration giriş parametresini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-179">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="36215-180">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="36215-180">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="36215-181">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="36215-181">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="36215-182">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="36215-182">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="36215-183">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="36215-183">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="36215-184">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="36215-184">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="36215-185">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="36215-185">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="36215-186">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="36215-186">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="36215-187">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="36215-187">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36215-188">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36215-188">Az.OperationalInsights</span></span>
* <span data-ttu-id="36215-189">PSWorkspace’in OperationalInsightsWorkspace’i uygulamamasıyla ilgili hata düzeltildi [#12135]</span><span class="sxs-lookup"><span data-stu-id="36215-189">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="36215-190">'Set-AzOperationalInsightsWorkspace' cmdlet’indeki 'Sku' parametresinin geçerli değer kümesine 'pergb2018' eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-190">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="36215-191">'FunctionParameter' parametresi için 'FunctionParameters' diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-191">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="36215-192">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="36215-192">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="36215-193">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="36215-193">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-194">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-194">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-195">Azure Backup’a MAB öğelerini getirme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-195">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="36215-196">Azure Site Recovery, 'StandardSSD_LRS' disk türünü destekler</span><span class="sxs-lookup"><span data-stu-id="36215-196">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-197">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-197">Az.Resources</span></span>
* <span data-ttu-id="36215-198">'PSADUser' değerine 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname' eklendi [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="36215-198">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="36215-199">'Get-AzADUser' üzerinde '-Mail' değerinin çalışmamasıyla ilgili sorun düzeltildi [#11981]</span><span class="sxs-lookup"><span data-stu-id="36215-199">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="36215-200">'Get-AzDeploymentWhatIfResult' ve 'Get-AzResourceGroupDeploymentWhatIfResult' cmdlet’lerine -ExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-200">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="36215-201">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' cmdlet’lerine '-WhatIfExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-201">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="36215-202">'Test-Az\*Deployment' cmdlet’leri daha iyi hata iletileri gösterecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-202">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="36215-203">deployment create ve What-If cmdlet’lerinin '-Name' parametresine yönelik yardım iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-203">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-204">Az.Sql</span></span>
* <span data-ttu-id="36215-205">SQL Server Azure Active Directory Yönetici cmdlet’ine hizmet sorumlusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-205">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="36215-206">Veri Sınıflandırma cmdlet’lerindeki eşitleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-206">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="36215-207">'Set-AzSqlServerActiveDirectoryAdministrator' üzerinde postaya göre kullanıcı arama desteği eklendi [#12192]</span><span class="sxs-lookup"><span data-stu-id="36215-207">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-208">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-208">Az.Storage</span></span>
* <span data-ttu-id="36215-209">RequireInfrastructureEncryption ile Depolama hesabı oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-209">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="36215-210">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36215-210">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="36215-211">Azure.Core yükleme mantığı Az.Accounts’a taşındı</span><span class="sxs-lookup"><span data-stu-id="36215-211">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-212">Az.Websites</span></span>
* <span data-ttu-id="36215-213">'Restore-AzDeletedWebApp' cmdlet’inde geri yüklemenin başarısız olması durumunda, oluşturulan web uygulamasının silinmesine yönelik koruma eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-213">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="36215-214">'New-AzWebApp' ve 'New-AzWebAppSlot' için SourceWebApp.Location' eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-214">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="36215-215">'Set-AzWebApp' ve 'Set-AzWebAppSlot' cmdlet’lerinde Kapsayıcı ayarlarının değiştirilmesini engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-215">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="36215-216">Get-AzWebApp için -Name verilmediğinde SiteConfig alınmasıyla ilgili hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-216">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="36215-217">Linux Uygulamaları için ASP oluşturmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-217">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="36215-218">Kaynak grupları arasında kopyalama için özel durumlar eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-218">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="36215-219">4.2.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="36215-219">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-220">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-220">Az.Accounts</span></span>
* <span data-ttu-id="36215-221">Azure Otomasyonu veya PowerShell işlerinde Az’nin günlükleri atlamasına neden olabilecek bir sorun düzeltildi [#11492]</span><span class="sxs-lookup"><span data-stu-id="36215-221">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="36215-222">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="36215-222">Az.AnalysisServices</span></span>
* <span data-ttu-id="36215-223">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-223">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36215-224">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36215-224">Az.ApiManagement</span></span>
* <span data-ttu-id="36215-225">Hizmet yönetimi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-225">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="36215-226">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="36215-226">Az.Billing</span></span>
* <span data-ttu-id="36215-227">Tüketim cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-227">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36215-228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36215-228">Az.CognitiveServices</span></span>
* <span data-ttu-id="36215-229">PrivateEndpoint ve PublicNetworkAccess denetimini destekler.</span><span class="sxs-lookup"><span data-stu-id="36215-229">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="36215-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-230">Az.DataFactory</span></span>
* <span data-ttu-id="36215-231">Veri fabrikası V2 cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-231">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="36215-232">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="36215-232">Az.DataShare</span></span>
* <span data-ttu-id="36215-233">''Az.DataShare'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-233">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="36215-234">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="36215-234">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="36215-235">''Az.DesktopVirtualization'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-235">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36215-236">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36215-236">Az.OperationalInsights</span></span>
* <span data-ttu-id="36215-237">SDK 0.21.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-237">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="36215-238">İsteğe bağlı aşağıdaki parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-238">Added optional parameters to</span></span> 
    - <span data-ttu-id="36215-239">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="36215-239">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="36215-240">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="36215-240">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36215-241">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36215-241">Az.PolicyInsights</span></span>
* <span data-ttu-id="36215-242">'Start-AzPolicyComplianceScan' için 3. örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-242">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="36215-243">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="36215-243">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="36215-244">PowerBI cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-244">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="36215-245">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="36215-245">Az.PrivateDns</span></span>
* <span data-ttu-id="36215-246">Remove-AzPrivateDnsRecordSet için ayrıntılı çıkış dizesi biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-246">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-248">XML girişinden bölgeler arasında çoğaltma için kurtarma planı oluşturmaya yönelik Azure Site Recovery desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-248">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="36215-249">SiteRecovery ve Backup cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-249">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-250">Az.Resources</span></span>
* <span data-ttu-id="36215-251">Get-AzDeploymentScriptLog ve Save-AzDeploymentScriptLog cmdlet’lerine Tail parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-251">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="36215-252">Çıkış özelliği biçimlendirildi ve Get-AzDeploymentScript cmdlet çıkışında gösterildi</span><span class="sxs-lookup"><span data-stu-id="36215-252">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="36215-253">-DeploymentScriptInputObject parametresinin adı -DeploymentScriptObject olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-253">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="36215-254">Cmdlet iletilerinde geçersiz dosya/hedef adı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-254">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="36215-255">Kaynak yöneticisi ve etiketler cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-255">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-256">Az.Sql</span></span>
* <span data-ttu-id="36215-257">'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine UsePrivateLinkConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-257">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="36215-258">'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine SyncMemberAzureDatabaseResourceId eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-258">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="36215-259">SQL Server Azure Active Directory Yönetici cmdlet’ine Konuk kullanıcı arama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-259">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-260">Az.Storage</span></span>
* <span data-ttu-id="36215-261">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-261">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="36215-262">4.1.0 - Mayıs 2020</span><span class="sxs-lookup"><span data-stu-id="36215-262">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="36215-263">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="36215-263">Highlights since the last release</span></span>
* <span data-ttu-id="36215-264">Desteklenen PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="36215-264">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="36215-265">Az.Functions genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-265">General availability of Az.Functions</span></span> 
* <span data-ttu-id="36215-266">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources ve Az.Storage için ana sürüm yayımlandı</span><span class="sxs-lookup"><span data-stu-id="36215-266">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36215-267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-267">Az.Accounts</span></span>
* <span data-ttu-id="36215-268">'Add-AzEnvironment' ve 'Set-AzEnvironment', 'AzureSynapseAnalyticsEndpointResourceId' ve 'AzureSynapseAnalyticsEndpointSuffix' parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-268">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="36215-269">Azure.Core ile ilgili bütünleştirilmiş kodlar Az.Accounts’a eklendi, desteklenen PowerShell platformları Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+ sürümlerini içerir</span><span class="sxs-lookup"><span data-stu-id="36215-269">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="36215-270">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="36215-270">Az.Aks</span></span>
* <span data-ttu-id="36215-271">API Sürümü 2019-10-01’e yükseltildi</span><span class="sxs-lookup"><span data-stu-id="36215-271">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="36215-272">Windows kapsayıcısı kullanılarak AKS oluşturma desteği sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-272">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="36215-273">Yeni cmdlet’ler sağlandı: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="36215-273">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36215-274">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36215-274">Az.ApiManagement</span></span>
* <span data-ttu-id="36215-275">'New-AzApiManagement' ve 'Set-AzApiManagement': [-AssignIdentity] parametresi [-SystemAssignedIdentity] olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-275">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="36215-276">'New-AzApiManagement' ve 'Set-AzApiManagement': Yeni parametre eklendi: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="36215-276">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="36215-277">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-277">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="36215-278">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-278">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="36215-279">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-279">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="36215-280">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-280">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="36215-281">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-281">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="36215-282">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-282">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="36215-283">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-283">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="36215-284">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-284">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="36215-285">Yeni 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementAuthorizationServer' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="36215-285">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="36215-286">Yeni 'Get-AzApiManagementNamedValueSecretValue' cmdlet’i eklendi. 'Get-AzApiManagementNamedValue' artık gizli dizi değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="36215-286">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="36215-287">Yeni 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementOpenIdConnectProvider' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="36215-287">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="36215-288">Yeni 'Get-AzApiManagementSubscriptionKey' cmdlet’i eklendi. 'Get-AzApiManagementSubscription' artık abonelik anahtarlarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="36215-288">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="36215-289">Yeni 'Get-AzApiManagementTenantAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="36215-289">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="36215-290">Yeni 'Get-AzApiManagementTenantGitAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantGitAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="36215-290">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="36215-291">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="36215-291">Az.ApplicationInsights</span></span>
* <span data-ttu-id="36215-292">Parametreler eklendi: 'New-AzApplicationInsights' için 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="36215-292">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="36215-293">'Update-AzApplicationInsights' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="36215-293">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="36215-294">Bağlı Depolama Hesapları için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="36215-294">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36215-295">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36215-295">Az.Batch</span></span>
* <span data-ttu-id="36215-296">Az.Batch, 'Microsoft.Azure.Batch' SDK sürüm 13.0.0 ve 'Microsoft.Azure.Management.Batch' SDK sürüm 9.0.0 kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-296">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="36215-297">'New-AzBatchCertificate' için yeni '-CertificateKind' parametresi kullanılarak eklenen sertifika türünü seçme yeteneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-297">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="36215-298">Önceden hep '' olan 'ApplicationPackages' özelliği 'PSApplication' öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-298">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="36215-299">Uygulamanın içindeki belirli paketler artık 'Get-AzBatchApplicationPackage' kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="36215-299">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="36215-300">Örneğin: 'Get-AzBatchApplication -AccountName hesabım -ResourceGroupName kaynakgrubum -ApplicationId uygulamam'.</span><span class="sxs-lookup"><span data-stu-id="36215-300">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="36215-301">'New-AzBatchPool' kullanılarak havuz oluşturulurken, 'PSImageReference' öğesinin 'VirtualMachineImageId' özelliği artık yalnızca bir Paylaşılan Görüntü Galerisi görüntüsüne başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="36215-301">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="36215-302">'New-AzBatchPool' kullanılarak havuz oluşturulurken, havuz 'PSNetworkConfiguration' öğesinin yeni 'PublicIPAddressConfiguration' özelliği kullanılarak genel IP olmadan sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="36215-302">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="36215-303">'PSNetworkConfiguration' öğesinin 'PublicIPs' özelliği de 'PSPublicIPAddressConfiguration' içine taşındı.</span><span class="sxs-lookup"><span data-stu-id="36215-303">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="36215-304">Bu özellik yalnızca 'IPAddressProvisioningType' değeri 'UserManaged' olduğunda belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="36215-304">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-305">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-305">Az.Compute</span></span>
* <span data-ttu-id="36215-306">'Update-AzVM' cmdlet’ine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-306">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="36215-307">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' ve 'Set-AzVmssOsProfile' cmdlet’leri için Yardım belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-307">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="36215-308">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="36215-308">Breaking changes</span></span>
    - <span data-ttu-id="36215-309">FilterExpression parametresi 'Get-AzVMImage' cmdlet’inden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-309">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="36215-310">AssignIdentity parametresi 'New-AzVmssConfig', 'New-AzVMConfig' ve 'Update-AzVM' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-310">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="36215-311">AutomaticRepairMaxInstanceRepairsPercent, 'New-AzVmssConfig' ve 'Update-AzVmss' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-311">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="36215-312">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus ve VirtualMachineScaleSetsColocationStatus özellikleri ProximityPlacementGroup öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-312">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="36215-313">MaxInstanceRepairsPercent özelliği AutomaticRepairsPolicy öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-313">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="36215-314">AvailabilitySets, VirtualMachines ve VirtualMachineScaleSets türleri IList<SubResource> türünden IList<SubResourceWithColocationStatus> türüne değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-314">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="36215-315">'Get-AzVM' cmdlet’inin açıklaması, cmdlet’i daha iyi açıklayacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-315">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="36215-316">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-316">Az.DataFactory</span></span>
* <span data-ttu-id="36215-317">Yönetilen IR içinde veri akışı çalışma zamanı özelliklerinin CRUD’si desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-317">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36215-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36215-318">Az.FrontDoor</span></span>
* <span data-ttu-id="36215-319">Front Door Kural Altyapısı nesnesini oluşturmak, güncelleştirmek, almak ve silmek için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-319">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="36215-320">Front Door Kural Altyapısı nesnesini oluşturmak için yardımcı cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-320">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="36215-321">Front Door Yönlendirme Kuralı nesnesine Kural Altyapısı başvurusu eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-321">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="36215-322">Front Door Arka Uç nesnesine Özel Bağlantı parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-322">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="36215-323">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="36215-323">Az.Functions</span></span>
* <span data-ttu-id="36215-324">''Az.Functions'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-324">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36215-325">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36215-325">Az.HDInsight</span></span>
* <span data-ttu-id="36215-326">Müşteri tarafından yönetilen anahtar disk şifrelemesi desteği sunuldu.</span><span class="sxs-lookup"><span data-stu-id="36215-326">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="36215-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="36215-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="36215-328">Erişim ilkeleri artık varsayılan olarak geçerli sorumluyu kullanmıyor</span><span class="sxs-lookup"><span data-stu-id="36215-328">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36215-329">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-329">Az.IotHub</span></span>
* <span data-ttu-id="36215-330">SQL benzeri bir dil kullanarak bilgi almak üzere bir IoT hub’ında sorgu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-330">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="36215-331">'Add-AzIotHubDevice' cmdlet’inin alt cihaz olmadan Uç Özellikli Cihaz oluşturamaması sorunu düzeltildi [#11597]</span><span class="sxs-lookup"><span data-stu-id="36215-331">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="36215-332">IoT hub’ı, cihaz veya modül için SAS belirteci oluşturmak üzere cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-332">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="36215-333">Yapılandırma ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-333">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="36215-334">IoT Edge otomatik dağıtımını büyük ölçekte yönetin.</span><span class="sxs-lookup"><span data-stu-id="36215-334">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="36215-335">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="36215-335">New cmdlets are:</span></span>
    - <span data-ttu-id="36215-336">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="36215-336">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="36215-337">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="36215-337">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="36215-338">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="36215-338">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="36215-339">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="36215-339">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="36215-340">IoT Edge dağıtım ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-340">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="36215-341">Yapılandırma içeriğini belirtilen uç cihaza uygulamak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-341">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36215-342">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-342">Az.KeyVault</span></span>
* <span data-ttu-id="36215-343">İki diğer ad kaldırıldı: 'New-AzKeyVaultCertificateAdministratorDetails' ve 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="36215-343">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="36215-344">Anahtar kasası oluştururken varsayılan olarak geçici silme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-344">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="36215-345">Ağ kuralları, bir anahtar kasası oluştururken belirli ağ konumlarından erişilebilirliği yönetecek şekilde ayarlanabilir</span><span class="sxs-lookup"><span data-stu-id="36215-345">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="36215-346">Kendi anahtarını getir (BYOK) desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-346">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="36215-347">'Add-AzKeyVaultKey' anahtar değişim anahtarı oluşturmayı destekler</span><span class="sxs-lookup"><span data-stu-id="36215-347">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="36215-348">'Get-AzKeyVaultKey' genel bir anahtarı PEM biçiminde indirmeyi destekler</span><span class="sxs-lookup"><span data-stu-id="36215-348">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="36215-349">'Add-AzKeyVaultKey' yardım belgesinin 'KeyOps' bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-349">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-350">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-350">Az.Monitor</span></span>
* <span data-ttu-id="36215-351">'Set-AzDiagnosticSettings' için saklama ilkesinin tüm kategorilere uygulanmadığı hata düzeltildi [#11589]</span><span class="sxs-lookup"><span data-stu-id="36215-351">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="36215-352">Ölçüm uyarısı V2 için WebTest kullanılabilirlik ölçütleri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-352">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="36215-353">'New-AzMetricAlertRuleV2Criteria': Web testi kullanılabilirlik ölçütü oluşturma seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-353">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="36215-354">'Add-AzMetricAlertRuleV2': Yeni web testi kullanılabilirlik ölçütünü destekler</span><span class="sxs-lookup"><span data-stu-id="36215-354">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="36215-355">PSLogProfile içinde RetentionPolicy için gereksiz tanım kaldırıldı [#7608]</span><span class="sxs-lookup"><span data-stu-id="36215-355">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="36215-356">PSEventData içinde tanımlanan gereksiz özellikler kaldırıldı [#11353]</span><span class="sxs-lookup"><span data-stu-id="36215-356">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="36215-357">'Get-AzLog', 'Get-AzActivityLog' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-357">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-358">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-358">Az.Network</span></span>
* <span data-ttu-id="36215-359">Bölge varsayılan davranışının değiştirileceğini bildirmek için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-359">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="36215-360">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="36215-360">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="36215-361">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="36215-361">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="36215-362">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="36215-362">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="36215-363">Yeni üst düzey SecurityPartnerProvider kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-363">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="36215-364">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-364">New cmdlets added:</span></span>
        - <span data-ttu-id="36215-365">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="36215-365">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="36215-366">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="36215-366">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="36215-367">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="36215-367">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="36215-368">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="36215-368">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="36215-369">'PSPrivateLinkResource' üzerinde 'RequiredZoneNames' ve 'PSPrivateEndpointConnection' üzerinde 'GroupId' eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-369">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="36215-370">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject için SuccessThresholdRoundTripTimeMs parametresinin hatalı türü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-370">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="36215-371">VirtualWan cmdlet’leri AllowVnetToVnetTraffic bağımsız değişkeninin varsayılan değerini True olarak ayarlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-371">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="36215-372">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="36215-372">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="36215-373">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="36215-373">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="36215-374">Özel uç nokta için DNS bölgesi grubunu desteklemek amacıyla yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-374">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="36215-375">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="36215-375">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="36215-376">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="36215-376">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="36215-377">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="36215-377">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="36215-378">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="36215-378">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="36215-379">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="36215-379">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="36215-380">'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' ve 'DNSServers' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-380">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="36215-381">'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' ve 'DnsServer' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-381">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="36215-382">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-382">Updated cmdlet:</span></span>
        - <span data-ttu-id="36215-383">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="36215-383">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36215-384">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36215-384">Az.OperationalInsights</span></span>
* <span data-ttu-id="36215-385">Yeni oluşturulan SDK’yı uygulamak için eski kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-385">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="36215-386">Kullanımdan kaldırılan API’ler nedeniyle silinen cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-386">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="36215-387">'Get-AzOperationalInsightsSavedSearchResult' (diğer adı 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="36215-387">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="36215-388">'Get-AzOperationalInsightsSearchResult' (diğer adı 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="36215-388">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="36215-389">'Get-AzOperationalInsightsLinkTarget' (diğer adı 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="36215-389">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="36215-390">'Set-AzOperationalInsightsWorkspace' ve 'New-AzOperationalInsightsWorkspace' için parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-390">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="36215-391">Bağlı Depolama Hesabı için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="36215-391">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="36215-392">Kümeler ve Bağlı Hizmet için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="36215-392">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-393">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-393">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-394">Azure Site Recovery’de Azure’dan Azure’a sağlayıcı için yakın yerleştirilen grup sanal makinelerini korumak üzere destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-394">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="36215-395">Azure Site Recovery’de bölgeden bölgeye çoğaltma için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-395">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="36215-396">Azure Backup’ta Azure Dosya Paylaşımı Kurtarma Noktaları için uzun süreli saklama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-396">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="36215-397">Azure Backup’ta 'Get-AzRecoveryServicesBackupItem' cmdlet’inin çıkışına disk hariç tutma özellikleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-397">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="36215-398">Site Recovery hizmeti için Kasa kimlik bilgilerine yönelik özel uç noktalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-398">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-399">Az.Resources</span></span>
* <span data-ttu-id="36215-400">Yeni bir Rol Tanımı oluşturulurken görüntüleme gecikmesi hakkında ileti uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-400">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="36215-401">Kesin tür belirtilmiş nesne çıkışı için ilke cmdlet’leri değiştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-401">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="36215-402">'Get-AzResourceLock' cmdlet’i üzerinde kullanılan '-TenantLevel' parametresi kaldırıldı [#11335]</span><span class="sxs-lookup"><span data-stu-id="36215-402">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="36215-403">'Remove-AzResourceGroup -Id ResourceId' düzeltildi [#9882]</span><span class="sxs-lookup"><span data-stu-id="36215-403">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="36215-404">Kaynak grubu kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="36215-404">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="36215-405">Abonelik kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="36215-405">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="36215-406">Diğer ad: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="36215-406">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="36215-407">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' için '-WhatIf' ve '-Confirm' parametreleri ARM şablonu Durum sonuçlarını kullanmak için geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="36215-407">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="36215-408">Dağıtım cmdlet’lerinde 'ApiVersion' parametresi için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-408">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="36215-409">Dağıtım hataları için iyileştirilmiş hata iletilerini gösterme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-409">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="36215-410">Dağıtım hataları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-410">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="36215-411">Dağıtım betiği çıkışına 'error' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-411">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="36215-412">NuGet Microsoft.Azure.Management.ResourceManager '3.7.1-preview' sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-412">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="36215-413">DeploymentValidateResult içindeki Error özelliği nuget 3.7.1-preview sürümünden itibaren salt okunur olarak değiştirildiğinden belirli test çalışmaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-413">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="36215-414">SDK ResourceManager 3.7.1-preview sürümünden GenericResourceExpanded öğesi getirildi</span><span class="sxs-lookup"><span data-stu-id="36215-414">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="36215-415">Dağıtım için tüm Get cmdlet’lerine yönelik etiket desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-415">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="36215-416">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="36215-416">'New-AzDeployment'</span></span>
    - <span data-ttu-id="36215-417">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="36215-417">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="36215-418">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="36215-418">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="36215-419">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="36215-419">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36215-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36215-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="36215-421">Yanlış sertifika parmak izini alan --SecretIdentifier parametresini kullanarak sertifika ekleme özelliğindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-421">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-422">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-422">Az.Sql</span></span>
* <span data-ttu-id="36215-423">Şunların performansı iyileştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-423">Enhance performance of:</span></span>
    - <span data-ttu-id="36215-424">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="36215-424">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="36215-425">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="36215-425">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="36215-426">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="36215-426">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="36215-427">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="36215-427">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="36215-428">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="36215-428">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="36215-429">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="36215-429">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="36215-430">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="36215-430">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="36215-431">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="36215-431">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="36215-432">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’inden 'RetentionDays' parametresinin istemci tarafı doğrulaması kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-432">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="36215-433">Sanal ağ içindeki bir depolama hesabına denetim yapılarak Depolama Blob Verileri Katkıda Bulunan rolünün oluşturulması sırasında karşılaşılan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-433">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-434">Az.Storage</span></span>
* <span data-ttu-id="36215-435">'Get-AzStorageAccount' hesap alma/listeleme cmdlet’ine '-AsJob' eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-435">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="36215-436">Anahtar otomatik döndürmesini desteklemek için Depolama hesabı KeyvaultEncryption ile güncelleştirilirken KeyVersion isteğe bağlı hale getirildi</span><span class="sxs-lookup"><span data-stu-id="36215-436">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="36215-437">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36215-437">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="36215-438">İşlem hattıyla Azure Dosya Dizinini kaldırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-438">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="36215-439">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="36215-439">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="36215-440">Düzeltildi [#9880]: NetWorkRule DefaultAction değer tanımı swagger ile uyumlu olacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-440">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="36215-441">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="36215-441">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="36215-442">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="36215-442">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="36215-443">Düzeltildi [#11624]: Sunucu hatasından kaçınmak için NetworkRules eklenirken yinelenen kuralları atla</span><span class="sxs-lookup"><span data-stu-id="36215-443">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="36215-444">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="36215-444">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="36215-445">Microsoft.Azure.Cosmos.Table SDK 1.0.7 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="36215-445">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="36215-446">DataLake 2. Nesil Öğeleri listesinde yalnızca bazı öğeler döndürüldüğünde kullanıcıya ContinuationToken ile yeniden listelemesini anımsatmak için uyarı iletisi eklendi,</span><span class="sxs-lookup"><span data-stu-id="36215-446">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="36215-447">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="36215-447">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="36215-448">Azure Dosyalar Active Directory Domain Services Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-448">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="36215-449">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36215-449">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="36215-450">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36215-450">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="36215-451">Depolama hesabının Kerberos anahtarlarını yeni oluşturma veya listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-451">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="36215-452">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="36215-452">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="36215-453">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="36215-453">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="36215-454">Yük devretme Depolama hesabı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-454">Supported failover Storage account</span></span>
    - <span data-ttu-id="36215-455">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="36215-455">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="36215-456">'Get-AzStorageBlobCopyState' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-456">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="36215-457">'Get-AzStorageFileCopyState' ve 'Start-AzStorageBlobCopy' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-457">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="36215-458">Depolama istemci kitaplığı v12, Kuyruk ve Dosya cmdlet’leriyle tümleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-458">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="36215-459">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="36215-459">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="36215-460">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="36215-460">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="36215-461">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="36215-461">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="36215-462">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="36215-462">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="36215-463">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="36215-463">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="36215-464">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="36215-464">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="36215-465">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="36215-465">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="36215-466">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="36215-466">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="36215-467">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="36215-467">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="36215-468">CloudFileShare olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="36215-468">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="36215-469">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="36215-469">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="36215-470">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="36215-470">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="36215-471">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="36215-471">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="36215-472">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="36215-472">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="36215-473">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="36215-473">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="36215-474">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="36215-474">Az.TrafficManager</span></span>
* <span data-ttu-id="36215-475">'DisableAzureTrafficManagerEndpoint' ayrıntılı çıkışındaki hatalı profil adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-475">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-476">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-476">Az.Websites</span></span>
* <span data-ttu-id="36215-477">'Update-AzWebAppAccessRestrictionConfig' yardımındaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-477">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="36215-478">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="36215-478">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="36215-479">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="36215-479">Highlights since the last release</span></span>
* <span data-ttu-id="36215-480">Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="36215-480">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36215-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-481">Az.Accounts</span></span>
* <span data-ttu-id="36215-482">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="36215-482">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36215-483">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36215-483">Az.ApiManagement</span></span>
* <span data-ttu-id="36215-484">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-484">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="36215-485">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-485">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36215-486">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36215-486">Az.Cdn</span></span>
* <span data-ttu-id="36215-487">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-487">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36215-488">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36215-488">Az.CognitiveServices</span></span>
* <span data-ttu-id="36215-489">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="36215-489">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-490">Az.Compute</span></span>
* <span data-ttu-id="36215-491">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-491">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="36215-492">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="36215-492">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36215-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-493">Az.IotHub</span></span>
* <span data-ttu-id="36215-494">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="36215-494">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="36215-495">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="36215-495">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="36215-496">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="36215-496">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="36215-497">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-497">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="36215-498">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="36215-498">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="36215-499">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="36215-499">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="36215-500">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="36215-500">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="36215-501">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="36215-501">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="36215-502">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="36215-502">New cmdlets are:</span></span>
    - <span data-ttu-id="36215-503">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36215-503">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="36215-504">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36215-504">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="36215-505">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36215-505">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="36215-506">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="36215-506">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="36215-507">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-507">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36215-508">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-508">Az.KeyVault</span></span>
* <span data-ttu-id="36215-509">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-509">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="36215-510">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="36215-510">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="36215-511">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="36215-511">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="36215-512">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-512">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="36215-513">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="36215-513">Az.Maintenance</span></span>
* <span data-ttu-id="36215-514">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="36215-514">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-515">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-515">Az.Monitor</span></span>
* <span data-ttu-id="36215-516">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-516">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="36215-517">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="36215-517">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="36215-518">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="36215-518">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="36215-519">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="36215-519">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="36215-520">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="36215-520">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="36215-521">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="36215-521">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="36215-522">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="36215-522">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="36215-523">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="36215-523">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-524">Az.Network</span></span>
* <span data-ttu-id="36215-525">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-525">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="36215-526">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="36215-526">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="36215-527">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="36215-527">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="36215-528">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="36215-528">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="36215-529">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="36215-529">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="36215-530">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-530">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="36215-531">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="36215-531">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="36215-532">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="36215-532">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="36215-533">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-533">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="36215-534">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-534">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="36215-535">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="36215-535">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="36215-536">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-536">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="36215-537">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-537">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="36215-538">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-538">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="36215-539">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="36215-539">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="36215-540">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="36215-540">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36215-541">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36215-541">Az.PolicyInsights</span></span>
* <span data-ttu-id="36215-542">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-542">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="36215-543">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-543">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36215-544">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36215-544">Az.ServiceFabric</span></span>
* <span data-ttu-id="36215-545">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-545">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-546">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-546">Az.Sql</span></span>
* <span data-ttu-id="36215-547">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-547">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="36215-548">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-548">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-549">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-549">Az.Storage</span></span>
* <span data-ttu-id="36215-550">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-550">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="36215-551">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-551">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="36215-552">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36215-552">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="36215-553">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="36215-553">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="36215-554">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="36215-554">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="36215-555">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="36215-555">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="36215-556">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="36215-556">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="36215-557">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="36215-557">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="36215-558">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="36215-558">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="36215-559">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="36215-559">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="36215-560">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="36215-560">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="36215-561">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="36215-561">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="36215-562">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="36215-562">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="36215-563">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="36215-563">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="36215-564">Genel</span><span class="sxs-lookup"><span data-stu-id="36215-564">General</span></span>
* <span data-ttu-id="36215-565">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="36215-565">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="36215-566">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="36215-566">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="36215-567">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="36215-567">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="36215-568">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="36215-568">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="36215-569">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="36215-569">Az.Billing</span></span>
  - <span data-ttu-id="36215-570">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-570">Az.Compute</span></span>
  - <span data-ttu-id="36215-571">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="36215-571">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="36215-572">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36215-572">Az.EventHub</span></span>
  - <span data-ttu-id="36215-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-573">Az.IotHub</span></span>
  - <span data-ttu-id="36215-574">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-574">Az.KeyVault</span></span>
  - <span data-ttu-id="36215-575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-575">Az.Monitor</span></span>
  - <span data-ttu-id="36215-576">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-576">Az.Network</span></span>
  - <span data-ttu-id="36215-577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-577">Az.Resources</span></span>
  - <span data-ttu-id="36215-578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-578">Az.Storage</span></span>
  - <span data-ttu-id="36215-579">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-579">Az.Websites</span></span>
* <span data-ttu-id="36215-580">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-580">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="36215-581">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="36215-581">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="36215-582">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](https://aka.ms/InstallASHPowerShell) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="36215-582">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="36215-583">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="36215-583">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-584">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-584">Az.Accounts</span></span>
* <span data-ttu-id="36215-585">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="36215-585">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-586">Az.Compute</span></span>
* <span data-ttu-id="36215-587">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-587">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="36215-588">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="36215-588">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="36215-589">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="36215-589">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="36215-590">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-590">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="36215-591">[#11354]</span><span class="sxs-lookup"><span data-stu-id="36215-591">[#11354]</span></span>
* <span data-ttu-id="36215-592">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-592">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="36215-593">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="36215-593">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="36215-594">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="36215-594">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="36215-595">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="36215-595">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="36215-596">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="36215-596">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="36215-597">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-597">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="36215-598">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="36215-598">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="36215-599">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-599">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="36215-600">[#11257]</span><span class="sxs-lookup"><span data-stu-id="36215-600">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-601">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-601">Az.DataFactory</span></span>
* <span data-ttu-id="36215-602">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-602">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="36215-603">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-603">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-604">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-604">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-605">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-605">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="36215-606">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-606">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36215-607">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36215-607">Az.HDInsight</span></span>
* <span data-ttu-id="36215-608">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-608">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36215-609">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-609">Az.IotHub</span></span>
* <span data-ttu-id="36215-610">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-610">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="36215-611">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="36215-611">New Cmdlets are:</span></span>
    - <span data-ttu-id="36215-612">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="36215-612">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="36215-613">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="36215-613">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36215-614">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-614">Az.KeyVault</span></span>
* <span data-ttu-id="36215-615">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-615">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-616">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-616">Az.Monitor</span></span>
* <span data-ttu-id="36215-617">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-617">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-618">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-618">Az.Network</span></span>
* <span data-ttu-id="36215-619">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-619">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="36215-620">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="36215-620">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="36215-621">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="36215-621">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="36215-622">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="36215-622">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="36215-623">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="36215-623">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="36215-624">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-624">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36215-625">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36215-625">Az.PolicyInsights</span></span>
* <span data-ttu-id="36215-626">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-626">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-627">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-627">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-628">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-628">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="36215-629">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-629">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="36215-630">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-630">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="36215-631">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-631">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="36215-632">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-632">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="36215-633">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-633">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-634">Az.Resources</span></span>
* <span data-ttu-id="36215-635">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="36215-635">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="36215-636">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-636">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="36215-637">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-637">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="36215-638">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-638">Added example.</span></span>
* <span data-ttu-id="36215-639">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="36215-639">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="36215-640">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="36215-640">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-641">Az.Sql</span></span>
* <span data-ttu-id="36215-642">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-642">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="36215-643">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-643">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="36215-644">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="36215-644">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="36215-645">Az.Support</span><span class="sxs-lookup"><span data-stu-id="36215-645">Az.Support</span></span>
* <span data-ttu-id="36215-646">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-646">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-647">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-647">Az.Websites</span></span>
* <span data-ttu-id="36215-648">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-648">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="36215-649">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="36215-649">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="36215-650">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="36215-650">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="36215-651">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="36215-651">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="36215-652">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="36215-652">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="36215-653">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="36215-653">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-654">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-654">Az.Accounts</span></span>
* <span data-ttu-id="36215-655">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="36215-655">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="36215-656">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="36215-656">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="36215-657">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-657">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36215-658">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36215-658">Az.ApiManagement</span></span>
* <span data-ttu-id="36215-659">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="36215-659">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="36215-660">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="36215-660">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="36215-661">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-661">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="36215-662">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="36215-662">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-663">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-663">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-664">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-664">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36215-665">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-665">Az.IotHub</span></span>
* <span data-ttu-id="36215-666">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-666">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="36215-667">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="36215-667">New Cmdlets are:</span></span>
    - <span data-ttu-id="36215-668">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36215-668">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="36215-669">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36215-669">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="36215-670">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36215-670">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="36215-671">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36215-671">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="36215-672">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-672">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="36215-673">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="36215-673">New Cmdlets are:</span></span>
    - <span data-ttu-id="36215-674">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="36215-674">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="36215-675">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="36215-675">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="36215-676">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="36215-676">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="36215-677">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="36215-677">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="36215-678">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-678">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="36215-679">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-679">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="36215-680">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-680">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="36215-681">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="36215-681">New Cmdlets are:</span></span>
    - <span data-ttu-id="36215-682">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="36215-682">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="36215-683">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="36215-683">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="36215-684">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-684">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-685">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-685">Az.Monitor</span></span>
* <span data-ttu-id="36215-686">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="36215-686">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-687">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-687">Az.Network</span></span>
* <span data-ttu-id="36215-688">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-688">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="36215-689">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-689">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="36215-690">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="36215-690">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="36215-691">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-691">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-692">Az.Resources</span></span>
* <span data-ttu-id="36215-693">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-693">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="36215-694">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="36215-694">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="36215-695">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="36215-695">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="36215-696">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="36215-696">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="36215-697">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-697">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="36215-698">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-698">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="36215-699">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-699">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="36215-700">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="36215-700">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="36215-701">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="36215-701">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="36215-702">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="36215-702">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="36215-703">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="36215-703">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="36215-704">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-704">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="36215-705">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="36215-705">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="36215-706">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="36215-706">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-707">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-707">Az.Sql</span></span>
* <span data-ttu-id="36215-708">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-708">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="36215-709">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-709">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="36215-710">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="36215-710">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="36215-711">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="36215-711">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="36215-712">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="36215-712">Remove an LTR backup</span></span>
    - <span data-ttu-id="36215-713">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="36215-713">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="36215-714">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-714">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="36215-715">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-715">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="36215-716">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-716">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-717">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-717">Az.Storage</span></span>
* <span data-ttu-id="36215-718">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-718">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="36215-719">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="36215-719">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="36215-720">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-720">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="36215-721">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="36215-721">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="36215-722">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="36215-722">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-723">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-723">Az.Websites</span></span>
* <span data-ttu-id="36215-724">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-724">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="36215-725">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="36215-725">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="36215-726">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-726">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="36215-727">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="36215-727">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="36215-728">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-728">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="36215-729">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="36215-729">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="36215-730">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="36215-730">Highlights since the last major release</span></span>
* <span data-ttu-id="36215-731">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-731">Updated client side telemetry.</span></span>
* <span data-ttu-id="36215-732">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-732">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="36215-733">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-733">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36215-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-734">Az.Accounts</span></span>
* <span data-ttu-id="36215-735">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-735">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36215-736">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36215-736">Az.Automation</span></span>
* <span data-ttu-id="36215-737">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-737">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36215-738">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36215-738">Az.CognitiveServices</span></span>
* <span data-ttu-id="36215-739">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-739">Updated SDK to 7.0</span></span>
* <span data-ttu-id="36215-740">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-740">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-741">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-741">Az.Compute</span></span>
* <span data-ttu-id="36215-742">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="36215-742">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36215-743">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36215-743">Az.FrontDoor</span></span>
* <span data-ttu-id="36215-744">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-744">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36215-745">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-745">Az.IotHub</span></span>
* <span data-ttu-id="36215-746">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-746">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="36215-747">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="36215-747">New Cmdlets are:</span></span>
    - <span data-ttu-id="36215-748">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36215-748">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="36215-749">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36215-749">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="36215-750">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36215-750">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="36215-751">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="36215-751">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36215-752">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-752">Az.KeyVault</span></span>
* <span data-ttu-id="36215-753">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-753">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-754">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-754">Az.Monitor</span></span>
* <span data-ttu-id="36215-755">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-755">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="36215-756">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-756">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="36215-757">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="36215-757">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-758">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-758">Az.Network</span></span>
* <span data-ttu-id="36215-759">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-759">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="36215-760">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-760">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="36215-761">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-761">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="36215-762">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="36215-762">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="36215-763">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="36215-763">No new cmdlets are added.</span></span> <span data-ttu-id="36215-764">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="36215-764">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-765">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-765">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-766">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-766">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-767">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-767">Az.Resources</span></span>
* <span data-ttu-id="36215-768">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="36215-768">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="36215-769">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="36215-769">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="36215-770">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="36215-770">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="36215-771">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="36215-771">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="36215-772">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="36215-772">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="36215-773">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-773">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="36215-774">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-774">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="36215-775">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="36215-775">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-776">Az.Sql</span></span>
* <span data-ttu-id="36215-777">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-777">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="36215-778">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-778">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="36215-779">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="36215-779">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="36215-780">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="36215-780">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="36215-781">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-781">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="36215-782">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="36215-782">Az.StorageSync</span></span>
* <span data-ttu-id="36215-783">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-783">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="36215-784">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="36215-784">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="36215-785">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="36215-785">Highlights since the last major release</span></span>
* <span data-ttu-id="36215-786">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="36215-786">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="36215-787">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-787">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36215-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-788">Az.Accounts</span></span>
* <span data-ttu-id="36215-789">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="36215-789">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="36215-790">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-790">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36215-791">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36215-791">Az.ApiManagement</span></span>
* <span data-ttu-id="36215-792">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="36215-792">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="36215-793">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="36215-793">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="36215-794">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-794">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="36215-795">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-795">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-796">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-796">Az.Compute</span></span>
* <span data-ttu-id="36215-797">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="36215-797">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="36215-798">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-798">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="36215-799">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-799">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="36215-800">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="36215-800">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="36215-801">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-801">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-802">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-802">Az.DataFactory</span></span>
* <span data-ttu-id="36215-803">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-803">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="36215-804">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="36215-804">Az.DeploymentManager</span></span>
* <span data-ttu-id="36215-805">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="36215-805">Adds LIST operations for resources</span></span>
* <span data-ttu-id="36215-806">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="36215-806">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36215-807">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36215-807">Az.HDInsight</span></span>
* <span data-ttu-id="36215-808">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-808">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36215-809">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-809">Az.KeyVault</span></span>
* <span data-ttu-id="36215-810">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-810">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-811">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-811">Az.Network</span></span>
* <span data-ttu-id="36215-812">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-812">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="36215-813">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="36215-813">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="36215-814">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-814">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="36215-815">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-815">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="36215-816">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="36215-816">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="36215-817">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-817">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="36215-818">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-818">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="36215-819">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-819">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="36215-820">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-820">New cmdlets added:</span></span>
        - <span data-ttu-id="36215-821">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="36215-821">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="36215-822">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-822">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="36215-823">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="36215-823">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="36215-824">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-824">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36215-825">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36215-825">Az.PolicyInsights</span></span>
* <span data-ttu-id="36215-826">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="36215-826">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="36215-827">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-827">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="36215-828">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-828">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="36215-829">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-829">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-830">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-830">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-831">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-831">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="36215-832">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="36215-832">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-833">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-833">Az.Resources</span></span>
* <span data-ttu-id="36215-834">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="36215-834">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="36215-835">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-835">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-836">Az.Sql</span></span>
<span data-ttu-id="36215-837">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-837">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-838">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-838">Az.Storage</span></span>
* <span data-ttu-id="36215-839">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="36215-839">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="36215-840">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-840">New-AzStorageAccount</span></span>
* <span data-ttu-id="36215-841">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="36215-841">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="36215-842">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-842">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-843">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-843">Az.Websites</span></span>
* <span data-ttu-id="36215-844">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="36215-844">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="36215-845">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-845">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="36215-846">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="36215-846">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-847">Az.Accounts</span></span>
* <span data-ttu-id="36215-848">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-848">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36215-849">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36215-849">Az.Cdn</span></span>
* <span data-ttu-id="36215-850">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="36215-850">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-851">Az.Compute</span></span>
* <span data-ttu-id="36215-852">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-852">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="36215-853">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="36215-853">Az.ContainerInstance</span></span>
* <span data-ttu-id="36215-854">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-854">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="36215-855">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="36215-855">Az.DataBoxEdge</span></span>
* <span data-ttu-id="36215-856">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-856">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="36215-857">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="36215-857">Get the Edge Storage Container</span></span>
* <span data-ttu-id="36215-858">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-858">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="36215-859">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="36215-859">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="36215-860">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-860">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="36215-861">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="36215-861">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="36215-862">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-862">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="36215-863">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="36215-863">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="36215-864">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-864">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="36215-865">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="36215-865">Get the Edge Storage Account</span></span>
* <span data-ttu-id="36215-866">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-866">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="36215-867">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="36215-867">Create new Edge Storage Account</span></span>
* <span data-ttu-id="36215-868">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-868">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="36215-869">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="36215-869">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="36215-870">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="36215-870">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="36215-871">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="36215-871">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="36215-872">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-872">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="36215-873">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="36215-873">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-874">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-874">Az.DataFactory</span></span>
* <span data-ttu-id="36215-875">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-875">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="36215-876">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-876">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="36215-877">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-877">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="36215-878">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="36215-878">Az.DevTestLabs</span></span>
* <span data-ttu-id="36215-879">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-879">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36215-880">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36215-880">Az.EventHub</span></span>
* <span data-ttu-id="36215-881">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-881">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36215-882">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36215-882">Az.HDInsight</span></span>
* <span data-ttu-id="36215-883">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-883">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="36215-884">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="36215-884">Az.MachineLearning</span></span>
* <span data-ttu-id="36215-885">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-885">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="36215-886">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="36215-886">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="36215-887">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="36215-887">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="36215-888">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="36215-888">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="36215-889">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="36215-889">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="36215-890">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="36215-890">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="36215-891">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="36215-891">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="36215-892">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="36215-892">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-893">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-893">Az.Network</span></span>
* <span data-ttu-id="36215-894">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="36215-894">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-895">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-895">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-896">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-896">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="36215-897">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-897">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="36215-898">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-898">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="36215-899">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-899">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-900">Az.Resources</span></span>
* <span data-ttu-id="36215-901">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-901">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-902">Az.Sql</span></span>
* <span data-ttu-id="36215-903">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-903">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="36215-904">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-904">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="36215-905">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="36215-905">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="36215-906">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-906">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-907">Az.Storage</span></span>
* <span data-ttu-id="36215-908">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-908">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="36215-909">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="36215-909">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="36215-910">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="36215-910">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="36215-911">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-911">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="36215-912">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="36215-912">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="36215-913">Genel</span><span class="sxs-lookup"><span data-stu-id="36215-913">General</span></span>
* <span data-ttu-id="36215-914">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-914">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36215-915">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-915">Az.Accounts</span></span>
* <span data-ttu-id="36215-916">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="36215-916">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="36215-917">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="36215-917">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36215-918">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36215-918">Az.Batch</span></span>
* <span data-ttu-id="36215-919">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-919">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-920">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-920">Az.DataFactory</span></span>
* <span data-ttu-id="36215-921">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-921">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36215-922">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36215-922">Az.FrontDoor</span></span>
* <span data-ttu-id="36215-923">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-923">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="36215-924">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-924">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="36215-925">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="36215-925">Az.HealthcareApis</span></span>
* <span data-ttu-id="36215-926">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="36215-926">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36215-927">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-927">Az.KeyVault</span></span>
* <span data-ttu-id="36215-928">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-928">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="36215-929">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="36215-929">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="36215-930">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-930">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-931">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-931">Az.Monitor</span></span>
* <span data-ttu-id="36215-932">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-932">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="36215-933">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="36215-933">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="36215-934">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="36215-934">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-935">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-935">Az.Network</span></span>
* <span data-ttu-id="36215-936">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-936">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-937">Az.Resources</span></span>
* <span data-ttu-id="36215-938">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-938">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="36215-939">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-939">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-940">Az.Sql</span></span>
* <span data-ttu-id="36215-941">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="36215-941">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-942">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-942">Az.Storage</span></span>
* <span data-ttu-id="36215-943">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="36215-943">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="36215-944">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="36215-944">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="36215-945">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="36215-945">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="36215-946">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="36215-946">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="36215-947">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="36215-947">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="36215-948">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-948">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="36215-949">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-949">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="36215-950">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36215-950">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="36215-951">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36215-951">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="36215-952">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-952">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="36215-953">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="36215-953">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="36215-954">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-954">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="36215-955">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="36215-955">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="36215-956">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="36215-956">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="36215-957">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="36215-957">Highlights since the last major release</span></span>
* <span data-ttu-id="36215-958">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="36215-958">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="36215-959">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="36215-959">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-960">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-960">Az.Compute</span></span>
* <span data-ttu-id="36215-961">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="36215-961">VM Reapply feature</span></span>
    - <span data-ttu-id="36215-962">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="36215-962">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="36215-963">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="36215-963">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="36215-964">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36215-964">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="36215-965">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="36215-965">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="36215-966">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-966">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="36215-967">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-967">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="36215-968">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-968">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="36215-969">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-969">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="36215-970">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-970">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="36215-971">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-971">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="36215-972">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="36215-972">Az.DataBoxEdge</span></span>
* <span data-ttu-id="36215-973">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-973">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="36215-974">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="36215-974">Get the Order</span></span>
* <span data-ttu-id="36215-975">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-975">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="36215-976">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="36215-976">Create new Order</span></span>
* <span data-ttu-id="36215-977">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-977">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="36215-978">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="36215-978">Remove the Order</span></span>
* <span data-ttu-id="36215-979">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="36215-979">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="36215-980">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="36215-980">Now creates Local Share</span></span>
* <span data-ttu-id="36215-981">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-981">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="36215-982">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="36215-982">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="36215-983">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-983">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="36215-984">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="36215-984">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="36215-985">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-985">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="36215-986">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="36215-986">Gets the information about Triggers</span></span>
* <span data-ttu-id="36215-987">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-987">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="36215-988">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="36215-988">Create new Triggers</span></span>
* <span data-ttu-id="36215-989">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-989">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="36215-990">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="36215-990">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-991">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-991">Az.DataFactory</span></span>
* <span data-ttu-id="36215-992">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-992">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="36215-993">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-993">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-994">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-994">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-995">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-995">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36215-996">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36215-996">Az.EventHub</span></span>
* <span data-ttu-id="36215-997">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-997">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36215-998">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36215-998">Az.FrontDoor</span></span>
* <span data-ttu-id="36215-999">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-999">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="36215-1000">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1000">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="36215-1001">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1001">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="36215-1002">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="36215-1002">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-1003">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-1003">Az.Network</span></span>
* <span data-ttu-id="36215-1004">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1004">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="36215-1005">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="36215-1005">Az.PrivateDns</span></span>
* <span data-ttu-id="36215-1006">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1006">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-1007">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-1007">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-1008">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1008">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="36215-1009">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="36215-1009">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="36215-1010">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1010">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="36215-1011">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="36215-1011">Az.RedisCache</span></span>
* <span data-ttu-id="36215-1012">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1012">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="36215-1013">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1013">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="36215-1014">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1014">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-1015">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-1015">Az.Resources</span></span>
- <span data-ttu-id="36215-1016">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1016">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="36215-1017">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1017">Updated create policy definition help example</span></span>
- <span data-ttu-id="36215-1018">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1018">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="36215-1019">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1019">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="36215-1020">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1020">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-1021">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-1021">Az.Sql</span></span>
* <span data-ttu-id="36215-1022">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1022">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="36215-1023">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1023">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="36215-1024">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="36215-1024">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="36215-1025">Genel</span><span class="sxs-lookup"><span data-stu-id="36215-1025">General</span></span>
* <span data-ttu-id="36215-1026">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="36215-1026">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36215-1027">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-1027">Az.Accounts</span></span>
* <span data-ttu-id="36215-1028">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="36215-1028">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="36215-1029">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="36215-1029">Az.Advisor</span></span>
* <span data-ttu-id="36215-1030">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1030">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36215-1031">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36215-1031">Az.Batch</span></span>
* <span data-ttu-id="36215-1032">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1032">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="36215-1033">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="36215-1033">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="36215-1034">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1034">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="36215-1035">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1035">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="36215-1036">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="36215-1036">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="36215-1037">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="36215-1037">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="36215-1038">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="36215-1038">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="36215-1039">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1039">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="36215-1040">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1040">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="36215-1041">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1041">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="36215-1042">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="36215-1042">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="36215-1043">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="36215-1043">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="36215-1044">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1044">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="36215-1045">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="36215-1045">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="36215-1046">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1046">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="36215-1047">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1047">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="36215-1048">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1048">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="36215-1049">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1049">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="36215-1050">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1050">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="36215-1051">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1051">This operation is no longer supported.</span></span>
* <span data-ttu-id="36215-1052">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1052">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="36215-1053">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1053">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="36215-1054">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1054">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="36215-1055">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1055">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="36215-1056">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1056">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="36215-1057">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1057">New non-verified images are also now returned.</span></span> <span data-ttu-id="36215-1058">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1058">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="36215-1059">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1059">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="36215-1060">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1060">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="36215-1061">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1061">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="36215-1062">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1062">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="36215-1063">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1063">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="36215-1064">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1064">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="36215-1065">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1065">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="36215-1066">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="36215-1066">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="36215-1067">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="36215-1067">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36215-1068">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36215-1068">Az.Cdn</span></span>
* <span data-ttu-id="36215-1069">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1069">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="36215-1070">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1070">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-1071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-1071">Az.Compute</span></span>
* <span data-ttu-id="36215-1072">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="36215-1072">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="36215-1073">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="36215-1073">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="36215-1074">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="36215-1074">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="36215-1075">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="36215-1075">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="36215-1076">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1076">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="36215-1077">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="36215-1077">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="36215-1078">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1078">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="36215-1079">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="36215-1079">Breaking changes</span></span>
    - <span data-ttu-id="36215-1080">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="36215-1080">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="36215-1081">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="36215-1081">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-1082">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-1082">Az.DataFactory</span></span>
* <span data-ttu-id="36215-1083">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1083">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-1084">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-1084">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-1085">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="36215-1085">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="36215-1086">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="36215-1086">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="36215-1087">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="36215-1087">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="36215-1088">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="36215-1088">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="36215-1089">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="36215-1089">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="36215-1090">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="36215-1090">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36215-1091">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36215-1091">Az.FrontDoor</span></span>
* <span data-ttu-id="36215-1092">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1092">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36215-1093">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36215-1093">Az.HDInsight</span></span>
* <span data-ttu-id="36215-1094">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1094">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="36215-1095">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1095">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="36215-1096">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1096">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="36215-1097">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="36215-1097">Removed five cmdlets:</span></span>
    - <span data-ttu-id="36215-1098">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="36215-1098">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="36215-1099">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="36215-1099">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="36215-1100">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="36215-1100">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="36215-1101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="36215-1101">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="36215-1102">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="36215-1102">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="36215-1103">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-1103">Added three cmdlets:</span></span>
    - <span data-ttu-id="36215-1104">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="36215-1104">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="36215-1105">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="36215-1105">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="36215-1106">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="36215-1106">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="36215-1107">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1107">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="36215-1108">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1108">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="36215-1109">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1109">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="36215-1110">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1110">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="36215-1111">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1111">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="36215-1112">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1112">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="36215-1113">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1113">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="36215-1114">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1114">Added some scenario test cases.</span></span>
* <span data-ttu-id="36215-1115">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="36215-1115">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36215-1116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-1116">Az.IotHub</span></span>
* <span data-ttu-id="36215-1117">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="36215-1117">Breaking changes:</span></span>
    - <span data-ttu-id="36215-1118">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="36215-1118">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="36215-1119">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1119">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="36215-1120">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="36215-1120">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="36215-1121">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1121">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="36215-1122">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1122">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="36215-1123">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1123">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="36215-1124">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1124">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="36215-1125">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1125">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="36215-1126">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="36215-1126">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="36215-1127">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1127">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="36215-1128">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="36215-1128">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="36215-1129">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1129">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-1130">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-1130">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-1131">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1131">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="36215-1132">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1132">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="36215-1133">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1133">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="36215-1134">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1134">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="36215-1135">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1135">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="36215-1136">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1136">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="36215-1137">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1137">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="36215-1138">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1138">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="36215-1139">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1139">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-1140">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-1140">Az.Resources</span></span>
* <span data-ttu-id="36215-1141">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1141">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-1142">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-1142">Az.Network</span></span>
* <span data-ttu-id="36215-1143">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1143">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="36215-1144">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1144">Updated cmdlet:</span></span>
        - <span data-ttu-id="36215-1145">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1145">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36215-1146">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1146">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36215-1147">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1147">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36215-1148">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1148">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36215-1149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1149">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="36215-1150">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1150">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="36215-1151">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="36215-1151">New cmdlet:</span></span>
        - <span data-ttu-id="36215-1152">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="36215-1152">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="36215-1153">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1153">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="36215-1154">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1154">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="36215-1155">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1155">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="36215-1156">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1156">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="36215-1157">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1157">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="36215-1158">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1158">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="36215-1159">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1159">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="36215-1160">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-1160">New cmdlets added:</span></span>
        - <span data-ttu-id="36215-1161">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="36215-1161">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="36215-1162">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="36215-1162">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="36215-1163">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="36215-1163">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="36215-1164">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="36215-1164">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="36215-1165">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36215-1165">Set-AzVirtualHub</span></span>
* <span data-ttu-id="36215-1166">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1166">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="36215-1167">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1167">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="36215-1168">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1168">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="36215-1169">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1169">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="36215-1170">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1170">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="36215-1171">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1171">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="36215-1172">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1172">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="36215-1173">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-1173">New cmdlets added:</span></span>
        - <span data-ttu-id="36215-1174">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1174">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="36215-1175">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1175">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="36215-1176">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1176">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="36215-1177">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1177">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="36215-1178">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1178">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="36215-1179">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1179">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="36215-1180">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1180">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="36215-1181">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1181">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="36215-1182">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-1182">New cmdlets added:</span></span>
        - <span data-ttu-id="36215-1183">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="36215-1183">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="36215-1184">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="36215-1184">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="36215-1185">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="36215-1185">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="36215-1186">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="36215-1186">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="36215-1187">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="36215-1187">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="36215-1188">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="36215-1188">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="36215-1189">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1189">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="36215-1190">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1190">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="36215-1191">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1191">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="36215-1192">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1192">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="36215-1193">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1193">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="36215-1194">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1194">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="36215-1195">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1195">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="36215-1196">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1196">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="36215-1197">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1197">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="36215-1198">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="36215-1198">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="36215-1199">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1199">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="36215-1200">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-1200">New cmdlets added:</span></span>
        - <span data-ttu-id="36215-1201">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="36215-1201">New-AzIpGroup</span></span>
        - <span data-ttu-id="36215-1202">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="36215-1202">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="36215-1203">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="36215-1203">Get-AzIpGroup</span></span>
        - <span data-ttu-id="36215-1204">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="36215-1204">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36215-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36215-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="36215-1206">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1206">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-1207">Az.Sql</span></span>
* <span data-ttu-id="36215-1208">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1208">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="36215-1209">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1209">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="36215-1210">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="36215-1210">Removed deprecated aliases:</span></span>
* <span data-ttu-id="36215-1211">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="36215-1211">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="36215-1212">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="36215-1212">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="36215-1213">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-1213">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="36215-1214">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-1214">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="36215-1215">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="36215-1215">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="36215-1216">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1216">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-1217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-1217">Az.Storage</span></span>
* <span data-ttu-id="36215-1218">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="36215-1218">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="36215-1219">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-1219">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="36215-1220">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-1220">Set-AzStorageAccount</span></span>
* <span data-ttu-id="36215-1221">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="36215-1221">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="36215-1222">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="36215-1222">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="36215-1223">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="36215-1223">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="36215-1224">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="36215-1224">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="36215-1225">Genel</span><span class="sxs-lookup"><span data-stu-id="36215-1225">General</span></span>
* <span data-ttu-id="36215-1226">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="36215-1226">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36215-1227">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-1227">Az.Accounts</span></span>
* <span data-ttu-id="36215-1228">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1228">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36215-1229">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36215-1229">Az.ApiManagement</span></span>
* <span data-ttu-id="36215-1230">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1230">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="36215-1231">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1231">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36215-1232">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36215-1232">Az.Automation</span></span>
* <span data-ttu-id="36215-1233">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1233">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36215-1234">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36215-1234">Az.Batch</span></span>
* <span data-ttu-id="36215-1235">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="36215-1235">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-1236">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-1236">Az.Compute</span></span>
* <span data-ttu-id="36215-1237">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1237">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="36215-1238">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1238">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="36215-1239">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1239">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="36215-1240">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1240">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-1241">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-1241">Az.DataFactory</span></span>
* <span data-ttu-id="36215-1242">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="36215-1242">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="36215-1243">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="36215-1243">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="36215-1244">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1244">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-1245">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-1245">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-1246">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1246">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="36215-1247">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="36215-1247">Az.HealthcareApis</span></span>
* <span data-ttu-id="36215-1248">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1248">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="36215-1249">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1249">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="36215-1250">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1250">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="36215-1251">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1251">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36215-1252">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-1252">Az.IotHub</span></span>
* <span data-ttu-id="36215-1253">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="36215-1253">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="36215-1254">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="36215-1254">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-1255">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-1255">Az.Monitor</span></span>
* <span data-ttu-id="36215-1256">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1256">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="36215-1257">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="36215-1257">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="36215-1258">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="36215-1258">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="36215-1259">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1259">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-1260">Az.Network</span></span>
* <span data-ttu-id="36215-1261">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1261">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="36215-1262">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1262">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="36215-1263">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-1263">New cmdlets added:</span></span>
        - <span data-ttu-id="36215-1264">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="36215-1264">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="36215-1265">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1265">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="36215-1266">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1266">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="36215-1267">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1267">Updated cmdlets:</span></span>
        - <span data-ttu-id="36215-1268">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36215-1268">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="36215-1269">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36215-1269">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="36215-1270">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36215-1270">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="36215-1271">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1271">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="36215-1272">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="36215-1272">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="36215-1273">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="36215-1273">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="36215-1274">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="36215-1274">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="36215-1275">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="36215-1275">Az.RedisCache</span></span>
* <span data-ttu-id="36215-1276">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1276">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-1277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-1277">Az.Sql</span></span>
* <span data-ttu-id="36215-1278">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1278">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-1279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-1279">Az.Storage</span></span>
* <span data-ttu-id="36215-1280">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1280">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="36215-1281">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="36215-1281">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="36215-1282">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="36215-1282">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="36215-1283">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="36215-1283">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="36215-1284">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-1284">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="36215-1285">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="36215-1285">Az.StorageSync</span></span>
* <span data-ttu-id="36215-1286">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1286">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-1287">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-1287">Az.Websites</span></span>
* <span data-ttu-id="36215-1288">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="36215-1288">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="36215-1289">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="36215-1289">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="36215-1290">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36215-1290">Az.ApiManagement</span></span>
* <span data-ttu-id="36215-1291">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1291">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="36215-1292">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1292">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="36215-1293">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="36215-1293">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36215-1294">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36215-1294">Az.Automation</span></span>
* <span data-ttu-id="36215-1295">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1295">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="36215-1296">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1296">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="36215-1297">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1297">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-1298">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-1298">Az.Compute</span></span>
* <span data-ttu-id="36215-1299">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1299">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="36215-1300">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1300">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="36215-1301">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-1301">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="36215-1302">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1302">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="36215-1303">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1303">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="36215-1304">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1304">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="36215-1305">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1305">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="36215-1306">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1306">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="36215-1307">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1307">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-1308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-1308">Az.DataFactory</span></span>
* <span data-ttu-id="36215-1309">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="36215-1309">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="36215-1310">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1310">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36215-1311">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36215-1311">Az.HDInsight</span></span>
* <span data-ttu-id="36215-1312">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="36215-1312">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36215-1313">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-1313">Az.IotHub</span></span>
* <span data-ttu-id="36215-1314">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1314">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="36215-1315">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1315">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="36215-1316">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="36215-1316">New cmdlets are:</span></span>
    - <span data-ttu-id="36215-1317">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="36215-1317">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="36215-1318">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="36215-1318">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="36215-1319">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="36215-1319">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="36215-1320">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="36215-1320">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-1321">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-1321">Az.Monitor</span></span>
* <span data-ttu-id="36215-1322">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="36215-1322">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="36215-1323">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="36215-1323">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="36215-1324">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="36215-1324">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="36215-1325">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="36215-1325">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="36215-1326">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1326">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="36215-1327">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1327">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="36215-1328">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="36215-1328">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="36215-1329">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="36215-1329">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="36215-1330">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1330">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="36215-1331">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="36215-1331">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="36215-1332">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1332">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="36215-1333">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="36215-1333">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="36215-1334">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1334">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="36215-1335">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="36215-1335">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="36215-1336">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="36215-1336">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="36215-1337">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="36215-1337">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="36215-1338">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="36215-1338">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="36215-1339">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="36215-1339">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="36215-1340">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1340">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="36215-1341">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1341">Overall improved help files</span></span>
* <span data-ttu-id="36215-1342">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1342">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-1343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-1343">Az.Network</span></span>
* <span data-ttu-id="36215-1344">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1344">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="36215-1345">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1345">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="36215-1346">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1346">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="36215-1347">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1347">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="36215-1348">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1348">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="36215-1349">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1349">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="36215-1350">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1350">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="36215-1351">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1351">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="36215-1352">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1352">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="36215-1353">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1353">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="36215-1354">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1354">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="36215-1355">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="36215-1355">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="36215-1356">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-1356">New cmdlets</span></span>
        - <span data-ttu-id="36215-1357">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="36215-1357">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="36215-1358">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1358">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="36215-1359">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1359">Updated cmdlet:</span></span>
        - <span data-ttu-id="36215-1360">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="36215-1360">New-VpnSite</span></span>
        - <span data-ttu-id="36215-1361">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="36215-1361">Update-VpnSite</span></span>
        - <span data-ttu-id="36215-1362">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1362">New-VpnConnection</span></span>
        - <span data-ttu-id="36215-1363">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1363">Update-VpnConnection</span></span>
* <span data-ttu-id="36215-1364">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1364">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-1365">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-1365">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-1366">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1366">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="36215-1367">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1367">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-1368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-1368">Az.Resources</span></span>
* <span data-ttu-id="36215-1369">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1369">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36215-1370">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36215-1370">Az.ServiceFabric</span></span>
* <span data-ttu-id="36215-1371">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1371">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="36215-1372">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="36215-1372">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="36215-1373">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="36215-1373">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="36215-1374">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="36215-1374">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="36215-1375">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="36215-1375">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="36215-1376">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="36215-1376">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="36215-1377">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="36215-1377">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="36215-1378">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="36215-1378">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="36215-1379">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="36215-1379">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="36215-1380">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="36215-1380">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="36215-1381">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="36215-1381">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="36215-1382">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="36215-1382">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="36215-1383">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="36215-1383">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="36215-1384">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="36215-1384">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="36215-1385">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="36215-1385">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="36215-1386">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1386">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="36215-1387">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="36215-1387">Az.SignalR</span></span>
* <span data-ttu-id="36215-1388">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1388">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-1389">Az.Sql</span></span>
* <span data-ttu-id="36215-1390">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1390">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="36215-1391">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1391">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="36215-1392">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-1392">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="36215-1393">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1393">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="36215-1394">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1394">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-1395">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-1395">Az.Storage</span></span>
* <span data-ttu-id="36215-1396">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1396">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="36215-1397">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1397">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="36215-1398">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="36215-1398">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="36215-1399">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="36215-1399">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="36215-1400">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1400">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="36215-1401">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="36215-1401">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="36215-1402">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1402">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="36215-1403">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36215-1403">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="36215-1404">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36215-1404">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="36215-1405">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36215-1405">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="36215-1406">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="36215-1406">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-1407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-1407">Az.Websites</span></span>
* <span data-ttu-id="36215-1408">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="36215-1408">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="36215-1409">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="36215-1409">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="36215-1410">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1410">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="36215-1411">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="36215-1411">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="36215-1412">Genel</span><span class="sxs-lookup"><span data-stu-id="36215-1412">General</span></span>
* <span data-ttu-id="36215-1413">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1413">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36215-1414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-1414">Az.Accounts</span></span>
* <span data-ttu-id="36215-1415">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="36215-1415">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="36215-1416">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="36215-1416">Az.Aks</span></span>
* <span data-ttu-id="36215-1417">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1417">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="36215-1418">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="36215-1418">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36215-1419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36215-1419">Az.ApiManagement</span></span>
* <span data-ttu-id="36215-1420">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1420">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="36215-1421">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1421">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="36215-1422">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1422">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="36215-1423">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="36215-1423">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="36215-1424">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1424">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36215-1425">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36215-1425">Az.Batch</span></span>
* <span data-ttu-id="36215-1426">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1426">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36215-1427">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36215-1427">Az.Cdn</span></span>
* <span data-ttu-id="36215-1428">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1428">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-1429">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-1429">Az.Compute</span></span>
* <span data-ttu-id="36215-1430">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1430">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="36215-1431">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1431">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="36215-1432">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1432">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="36215-1433">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1433">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="36215-1434">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="36215-1434">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="36215-1435">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1435">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="36215-1436">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1436">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="36215-1437">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1437">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-1438">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-1438">Az.DataFactory</span></span>
* <span data-ttu-id="36215-1439">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1439">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="36215-1440">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1440">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="36215-1441">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1441">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="36215-1442">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1442">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-1444">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1444">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36215-1445">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36215-1445">Az.EventHub</span></span>
* <span data-ttu-id="36215-1446">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="36215-1446">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="36215-1447">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="36215-1447">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="36215-1448">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1448">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="36215-1449">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="36215-1449">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="36215-1450">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="36215-1450">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="36215-1451">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1451">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-1452">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-1452">Az.Monitor</span></span>
* <span data-ttu-id="36215-1453">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1453">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-1454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-1454">Az.Network</span></span>
* <span data-ttu-id="36215-1455">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1455">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="36215-1456">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-1456">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="36215-1457">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1457">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="36215-1458">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="36215-1458">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="36215-1459">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="36215-1459">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="36215-1460">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1460">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="36215-1461">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1461">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36215-1462">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36215-1462">Az.OperationalInsights</span></span>
* <span data-ttu-id="36215-1463">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1463">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="36215-1464">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1464">Added example</span></span>
    - <span data-ttu-id="36215-1465">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1465">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="36215-1466">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1466">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="36215-1467">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1467">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-1468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-1468">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-1469">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1469">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-1470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-1470">Az.Resources</span></span>
* <span data-ttu-id="36215-1471">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1471">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="36215-1472">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1472">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="36215-1473">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="36215-1473">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="36215-1474">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1474">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="36215-1475">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="36215-1475">Az.ServiceBus</span></span>
* <span data-ttu-id="36215-1476">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="36215-1476">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="36215-1477">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="36215-1477">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="36215-1478">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1478">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36215-1479">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36215-1479">Az.ServiceFabric</span></span>
* <span data-ttu-id="36215-1480">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1480">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="36215-1481">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="36215-1481">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="36215-1482">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="36215-1482">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="36215-1483">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1483">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="36215-1484">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="36215-1484">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="36215-1485">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-1485">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-1486">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-1486">Az.Sql</span></span>
* <span data-ttu-id="36215-1487">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1487">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-1488">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-1488">Az.Storage</span></span>
* <span data-ttu-id="36215-1489">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1489">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="36215-1490">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="36215-1490">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="36215-1491">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="36215-1491">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="36215-1492">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="36215-1492">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="36215-1493">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="36215-1493">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="36215-1494">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="36215-1494">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-1495">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-1495">Az.Websites</span></span>
* <span data-ttu-id="36215-1496">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1496">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="36215-1497">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="36215-1497">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-1498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-1498">Az.Accounts</span></span>
* <span data-ttu-id="36215-1499">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1499">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="36215-1500">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="36215-1500">Az.ApplicationInsights</span></span>
* <span data-ttu-id="36215-1501">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1501">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36215-1502">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36215-1502">Az.Automation</span></span>
* <span data-ttu-id="36215-1503">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1503">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36215-1504">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36215-1504">Az.CognitiveServices</span></span>
* <span data-ttu-id="36215-1505">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1505">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-1506">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-1506">Az.Compute</span></span>
* <span data-ttu-id="36215-1507">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1507">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="36215-1508">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="36215-1508">Az.ContainerRegistry</span></span>
* <span data-ttu-id="36215-1509">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1509">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="36215-1510">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="36215-1510">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-1511">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-1511">Az.DataFactory</span></span>
* <span data-ttu-id="36215-1512">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1512">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="36215-1513">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1513">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36215-1514">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36215-1514">Az.EventHub</span></span>
* <span data-ttu-id="36215-1515">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="36215-1515">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="36215-1516">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1516">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36215-1517">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-1517">Az.KeyVault</span></span>
* <span data-ttu-id="36215-1518">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1518">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="36215-1519">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="36215-1519">Az.LogicApp</span></span>
* <span data-ttu-id="36215-1520">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="36215-1520">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="36215-1521">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1521">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="36215-1522">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="36215-1522">Az.ManagedServices</span></span>
* <span data-ttu-id="36215-1523">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="36215-1523">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-1524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-1524">Az.Network</span></span>
* <span data-ttu-id="36215-1525">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1525">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="36215-1526">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-1526">New cmdlets</span></span>
        - <span data-ttu-id="36215-1527">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36215-1527">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="36215-1528">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="36215-1528">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="36215-1529">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1529">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36215-1530">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1530">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36215-1531">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1531">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36215-1532">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1532">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="36215-1533">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="36215-1533">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="36215-1534">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="36215-1534">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="36215-1535">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="36215-1535">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="36215-1536">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1536">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="36215-1537">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1537">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="36215-1538">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1538">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="36215-1539">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-1539">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="36215-1540">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1540">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="36215-1541">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1541">Updated cmdlets</span></span>
        - <span data-ttu-id="36215-1542">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36215-1542">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="36215-1543">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36215-1543">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="36215-1544">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36215-1544">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="36215-1545">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1545">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="36215-1546">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1546">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="36215-1547">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1547">Updated cmdlet:</span></span>
        - <span data-ttu-id="36215-1548">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="36215-1548">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="36215-1549">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="36215-1549">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="36215-1550">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="36215-1550">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="36215-1551">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1551">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="36215-1552">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1552">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="36215-1553">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="36215-1553">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36215-1554">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36215-1554">Az.OperationalInsights</span></span>
* <span data-ttu-id="36215-1555">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1555">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="36215-1556">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1556">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-1557">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-1557">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-1558">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1558">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="36215-1559">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1559">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="36215-1560">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1560">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="36215-1561">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1561">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="36215-1562">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1562">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="36215-1563">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1563">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="36215-1564">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1564">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="36215-1565">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1565">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="36215-1566">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1566">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="36215-1567">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1567">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-1568">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-1568">Az.Resources</span></span>
- <span data-ttu-id="36215-1569">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-1569">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="36215-1570">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1570">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="36215-1571">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="36215-1571">Az.ServiceBus</span></span>
* <span data-ttu-id="36215-1572">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="36215-1572">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="36215-1573">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1573">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-1574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-1574">Az.Sql</span></span>
* <span data-ttu-id="36215-1575">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1575">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="36215-1576">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1576">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="36215-1577">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1577">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-1578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-1578">Az.Storage</span></span>
* <span data-ttu-id="36215-1579">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1579">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="36215-1580">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="36215-1580">Az.StorageSync</span></span>
* <span data-ttu-id="36215-1581">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1581">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="36215-1582">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1582">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-1583">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-1583">Az.Websites</span></span>
* <span data-ttu-id="36215-1584">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1584">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="36215-1585">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1585">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="36215-1586">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1586">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="36215-1587">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="36215-1587">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-1588">Az.Accounts</span></span>
* <span data-ttu-id="36215-1589">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1589">Add support for profile cmdlets</span></span>
* <span data-ttu-id="36215-1590">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1590">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="36215-1591">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1591">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="36215-1592">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="36215-1592">Az.Advisor</span></span>
* <span data-ttu-id="36215-1593">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-1593">GA release of Az.Advisor</span></span>
* <span data-ttu-id="36215-1594">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="36215-1594">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="36215-1595">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36215-1595">Az.ApiManagement</span></span>
* <span data-ttu-id="36215-1596">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1596">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="36215-1597">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="36215-1597">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="36215-1598">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1598">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="36215-1599">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="36215-1599">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="36215-1600">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="36215-1600">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="36215-1601">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="36215-1601">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="36215-1602">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1602">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36215-1603">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36215-1603">Az.Automation</span></span>
* <span data-ttu-id="36215-1604">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1604">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-1605">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-1605">Az.Compute</span></span>
* <span data-ttu-id="36215-1606">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1606">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-1607">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-1607">Az.DataFactory</span></span>
* <span data-ttu-id="36215-1608">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1608">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="36215-1609">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="36215-1609">Az.EventGrid</span></span>
* <span data-ttu-id="36215-1610">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1610">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36215-1611">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-1611">Az.IotHub</span></span>
* <span data-ttu-id="36215-1612">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1612">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-1613">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-1613">Az.Network</span></span>
* <span data-ttu-id="36215-1614">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1614">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="36215-1615">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1615">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36215-1616">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36215-1616">Az.PolicyInsights</span></span>
* <span data-ttu-id="36215-1617">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1617">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="36215-1618">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="36215-1618">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36215-1619">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36215-1619">Az.OperationalInsights</span></span>
* <span data-ttu-id="36215-1620">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1620">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-1621">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-1621">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-1622">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="36215-1622">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-1623">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-1623">Az.Resources</span></span>
    - <span data-ttu-id="36215-1624">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="36215-1624">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="36215-1625">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1625">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="36215-1626">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1626">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="36215-1627">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1627">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="36215-1628">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="36215-1628">Az.ServiceBus</span></span>
* <span data-ttu-id="36215-1629">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1629">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-1630">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-1630">Az.Sql</span></span>
* <span data-ttu-id="36215-1631">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1631">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="36215-1632">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1632">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="36215-1633">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="36215-1633">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="36215-1634">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="36215-1634">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="36215-1635">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="36215-1635">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="36215-1636">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="36215-1636">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="36215-1637">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="36215-1637">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="36215-1638">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="36215-1638">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="36215-1639">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-1639">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-1640">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-1640">Az.Storage</span></span>
* <span data-ttu-id="36215-1641">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1641">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="36215-1642">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="36215-1642">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="36215-1643">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1643">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="36215-1644">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="36215-1644">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="36215-1645">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1645">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="36215-1646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-1646">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="36215-1647">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-1647">Set-AzStorageAccount</span></span>
* <span data-ttu-id="36215-1648">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1648">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="36215-1649">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="36215-1649">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="36215-1650">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="36215-1650">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="36215-1651">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="36215-1651">Az.StorageSync</span></span>
* <span data-ttu-id="36215-1652">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="36215-1652">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="36215-1653">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="36215-1653">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-1654">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-1654">Az.Accounts</span></span>
* <span data-ttu-id="36215-1655">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1655">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="36215-1656">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="36215-1656">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="36215-1657">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1657">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="36215-1658">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="36215-1658">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="36215-1659">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="36215-1659">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-1660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-1660">Az.Compute</span></span>
* <span data-ttu-id="36215-1661">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1661">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="36215-1662">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1662">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="36215-1663">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="36215-1663">Az.Dns</span></span>
* <span data-ttu-id="36215-1664">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1664">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="36215-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="36215-1665">Az.EventGrid</span></span>
* <span data-ttu-id="36215-1666">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1666">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="36215-1667">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="36215-1667">New cmdlets:</span></span>
    - <span data-ttu-id="36215-1668">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="36215-1668">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="36215-1669">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36215-1669">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="36215-1670">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="36215-1670">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="36215-1671">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="36215-1671">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="36215-1672">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="36215-1672">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="36215-1673">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36215-1673">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="36215-1674">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="36215-1674">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="36215-1675">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="36215-1675">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="36215-1676">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="36215-1676">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="36215-1677">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36215-1677">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="36215-1678">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="36215-1678">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="36215-1679">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36215-1679">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="36215-1680">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="36215-1680">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="36215-1681">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="36215-1681">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="36215-1682">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="36215-1682">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="36215-1683">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36215-1683">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="36215-1684">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1684">Updated cmdlets:</span></span>
    - <span data-ttu-id="36215-1685">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="36215-1685">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="36215-1686">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="36215-1686">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="36215-1687">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="36215-1687">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="36215-1688">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="36215-1688">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="36215-1689">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-1689">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="36215-1690">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="36215-1690">Event subscription expiration date,</span></span>
            - <span data-ttu-id="36215-1691">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="36215-1691">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="36215-1692">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="36215-1692">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="36215-1693">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="36215-1693">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="36215-1694">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="36215-1694">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="36215-1695">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="36215-1695">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="36215-1696">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="36215-1696">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="36215-1697">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="36215-1697">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="36215-1698">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="36215-1698">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36215-1699">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36215-1699">Az.FrontDoor</span></span>
* <span data-ttu-id="36215-1700">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="36215-1700">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="36215-1701">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="36215-1701">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="36215-1702">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="36215-1702">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="36215-1703">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="36215-1703">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-1704">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-1704">Az.Network</span></span>
* <span data-ttu-id="36215-1705">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="36215-1705">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="36215-1706">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-1706">New cmdlets</span></span>
        - <span data-ttu-id="36215-1707">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="36215-1707">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="36215-1708">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="36215-1708">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="36215-1709">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-1709">New cmdlets</span></span>
        - <span data-ttu-id="36215-1710">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="36215-1710">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="36215-1711">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="36215-1711">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="36215-1712">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-1712">New cmdlets</span></span>
        - <span data-ttu-id="36215-1713">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="36215-1713">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="36215-1714">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="36215-1714">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="36215-1715">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="36215-1715">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="36215-1716">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="36215-1716">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="36215-1717">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1717">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="36215-1718">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="36215-1718">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="36215-1719">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-1719">New cmdlets</span></span>
        - <span data-ttu-id="36215-1720">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36215-1720">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="36215-1721">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36215-1721">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="36215-1722">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36215-1722">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="36215-1723">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="36215-1723">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="36215-1724">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="36215-1724">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="36215-1725">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1725">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="36215-1726">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1726">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="36215-1727">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1727">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="36215-1728">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1728">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="36215-1729">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1729">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="36215-1730">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1730">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="36215-1731">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1731">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="36215-1732">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1732">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="36215-1733">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1733">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="36215-1734">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1734">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="36215-1735">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1735">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="36215-1736">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1736">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="36215-1737">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1737">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="36215-1738">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1738">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="36215-1739">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1739">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="36215-1740">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1740">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="36215-1741">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="36215-1741">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="36215-1742">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="36215-1742">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="36215-1743">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="36215-1743">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="36215-1744">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1744">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="36215-1745">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1745">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="36215-1746">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1746">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36215-1747">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36215-1747">Az.OperationalInsights</span></span>
* <span data-ttu-id="36215-1748">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1748">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-1749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-1749">Az.Resources</span></span>
* <span data-ttu-id="36215-1750">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="36215-1750">Support for additional Template Export options</span></span>
    - <span data-ttu-id="36215-1751">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1751">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="36215-1752">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1752">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="36215-1753">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1753">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36215-1754">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36215-1754">Az.ServiceFabric</span></span>
* <span data-ttu-id="36215-1755">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1755">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-1756">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-1756">Az.Sql</span></span>
* <span data-ttu-id="36215-1757">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1757">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="36215-1758">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1758">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="36215-1759">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-1759">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="36215-1760">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="36215-1760">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="36215-1761">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="36215-1761">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="36215-1762">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="36215-1762">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="36215-1763">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="36215-1763">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="36215-1764">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="36215-1764">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-1765">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-1765">Az.Storage</span></span>
* <span data-ttu-id="36215-1766">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="36215-1766">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="36215-1767">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-1767">New-AzStorageAccount</span></span>
* <span data-ttu-id="36215-1768">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1768">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="36215-1769">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="36215-1769">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-1770">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-1770">Az.Websites</span></span>
* <span data-ttu-id="36215-1771">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="36215-1771">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="36215-1772">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="36215-1772">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="36215-1773">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="36215-1773">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="36215-1774">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36215-1774">Az.Cdn</span></span>
* <span data-ttu-id="36215-1775">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1775">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-1776">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-1776">Az.Compute</span></span>
* <span data-ttu-id="36215-1777">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1777">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="36215-1778">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="36215-1778">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36215-1779">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36215-1779">Az.EventHub</span></span>
* <span data-ttu-id="36215-1780">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="36215-1780">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="36215-1781">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="36215-1781">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-1782">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-1782">Az.Network</span></span>
* <span data-ttu-id="36215-1783">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1783">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="36215-1784">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1784">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36215-1785">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36215-1785">Az.PolicyInsights</span></span>
* <span data-ttu-id="36215-1786">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1786">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-1787">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-1787">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-1788">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1788">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="36215-1789">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="36215-1789">Az.ServiceBus</span></span>
* <span data-ttu-id="36215-1790">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="36215-1790">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36215-1791">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36215-1791">Az.ServiceFabric</span></span>
* <span data-ttu-id="36215-1792">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1792">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="36215-1793">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1793">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-1794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-1794">Az.Sql</span></span>
* <span data-ttu-id="36215-1795">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1795">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="36215-1796">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="36215-1796">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="36215-1797">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-1797">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="36215-1798">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="36215-1798">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-1799">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-1799">Az.Websites</span></span>
* <span data-ttu-id="36215-1800">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="36215-1800">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="36215-1801">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="36215-1801">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="36215-1802">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36215-1802">Az.ApiManagement</span></span>
* <span data-ttu-id="36215-1803">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="36215-1803">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="36215-1804">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="36215-1804">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="36215-1805">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="36215-1805">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="36215-1806">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="36215-1806">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="36215-1807">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36215-1807">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="36215-1808">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="36215-1808">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="36215-1809">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="36215-1809">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="36215-1810">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="36215-1810">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="36215-1811">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="36215-1811">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="36215-1812">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="36215-1812">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="36215-1813">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="36215-1813">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="36215-1814">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="36215-1814">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="36215-1815">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="36215-1815">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="36215-1816">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="36215-1816">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="36215-1817">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="36215-1817">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="36215-1818">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="36215-1818">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="36215-1819">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="36215-1819">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="36215-1820">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="36215-1820">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="36215-1821">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="36215-1821">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="36215-1822">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="36215-1822">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="36215-1823">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="36215-1823">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="36215-1824">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="36215-1824">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="36215-1825">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="36215-1825">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="36215-1826">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1826">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="36215-1827">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1827">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="36215-1828">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1828">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="36215-1829">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="36215-1829">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="36215-1830">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="36215-1830">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="36215-1831">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1831">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="36215-1832">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1832">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="36215-1833">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1833">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="36215-1834">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="36215-1834">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="36215-1835">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1835">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="36215-1836">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1836">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="36215-1837">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="36215-1837">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="36215-1838">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="36215-1838">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="36215-1839">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="36215-1839">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="36215-1840">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1840">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="36215-1841">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1841">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="36215-1842">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1842">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="36215-1843">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="36215-1843">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="36215-1844">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="36215-1844">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="36215-1845">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="36215-1845">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="36215-1846">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="36215-1846">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="36215-1847">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1847">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="36215-1848">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="36215-1848">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="36215-1849">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="36215-1849">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="36215-1850">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="36215-1850">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="36215-1851">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1851">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="36215-1852">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="36215-1852">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="36215-1853">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="36215-1853">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="36215-1854">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="36215-1854">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="36215-1855">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="36215-1855">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="36215-1856">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1856">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="36215-1857">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="36215-1857">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="36215-1858">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="36215-1858">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="36215-1859">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1859">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="36215-1860">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="36215-1860">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="36215-1861">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="36215-1861">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="36215-1862">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1862">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="36215-1863">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1863">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="36215-1864">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="36215-1864">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="36215-1865">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="36215-1865">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="36215-1866">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1866">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="36215-1867">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1867">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="36215-1868">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="36215-1868">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="36215-1869">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="36215-1869">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="36215-1870">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="36215-1870">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="36215-1871">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="36215-1871">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="36215-1872">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="36215-1872">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="36215-1873">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="36215-1873">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="36215-1874">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="36215-1874">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="36215-1875">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="36215-1875">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="36215-1876">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="36215-1876">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="36215-1877">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="36215-1877">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="36215-1878">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="36215-1878">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="36215-1879">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="36215-1879">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36215-1880">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36215-1880">Az.Automation</span></span>
* <span data-ttu-id="36215-1881">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1881">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="36215-1882">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1882">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="36215-1883">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1883">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="36215-1884">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1884">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="36215-1885">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1885">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="36215-1886">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1886">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="36215-1887">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="36215-1887">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-1888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-1888">Az.Compute</span></span>
* <span data-ttu-id="36215-1889">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1889">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="36215-1890">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="36215-1890">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-1891">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-1891">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-1892">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1892">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-1893">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-1893">Az.Monitor</span></span>
* <span data-ttu-id="36215-1894">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1894">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-1895">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-1895">Az.Network</span></span>
* <span data-ttu-id="36215-1896">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1896">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="36215-1897">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="36215-1897">Updated cmdlet:</span></span>
        - <span data-ttu-id="36215-1898">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="36215-1898">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="36215-1899">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-1899">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-1900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-1900">Az.Resources</span></span>
* <span data-ttu-id="36215-1901">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1901">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-1902">Az.Sql</span></span>
* <span data-ttu-id="36215-1903">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="36215-1903">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="36215-1904">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="36215-1904">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-1905">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-1905">Az.Accounts</span></span>
* <span data-ttu-id="36215-1906">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="36215-1906">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36215-1907">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36215-1907">Az.CognitiveServices</span></span>
* <span data-ttu-id="36215-1908">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="36215-1908">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="36215-1909">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="36215-1909">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-1910">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-1910">Az.Compute</span></span>
* <span data-ttu-id="36215-1911">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="36215-1911">Proximity placement group feature.</span></span>
    - <span data-ttu-id="36215-1912">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="36215-1912">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="36215-1913">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="36215-1913">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="36215-1914">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1914">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="36215-1915">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="36215-1915">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="36215-1916">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1916">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="36215-1917">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="36215-1917">Breaking changes</span></span>
    - <span data-ttu-id="36215-1918">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1918">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="36215-1919">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-1919">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="36215-1920">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="36215-1920">Az.DeploymentManager</span></span>
* <span data-ttu-id="36215-1921">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="36215-1921">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="36215-1922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="36215-1922">Az.Dns</span></span>
* <span data-ttu-id="36215-1923">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="36215-1923">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="36215-1924">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="36215-1924">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="36215-1925">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="36215-1925">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="36215-1926">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36215-1926">Az.FrontDoor</span></span>
* <span data-ttu-id="36215-1927">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="36215-1927">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="36215-1928">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="36215-1928">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="36215-1929">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36215-1929">Az.HDInsight</span></span>
* <span data-ttu-id="36215-1930">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="36215-1930">Removed two cmdlets:</span></span>
    - <span data-ttu-id="36215-1931">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="36215-1931">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="36215-1932">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="36215-1932">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="36215-1933">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1933">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="36215-1934">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="36215-1934">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="36215-1935">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="36215-1935">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="36215-1936">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="36215-1936">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-1937">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-1937">Az.Monitor</span></span>
* <span data-ttu-id="36215-1938">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="36215-1938">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="36215-1939">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="36215-1939">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="36215-1940">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="36215-1940">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="36215-1941">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="36215-1941">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="36215-1942">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="36215-1942">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="36215-1943">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="36215-1943">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="36215-1944">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="36215-1944">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="36215-1945">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="36215-1945">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="36215-1946">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="36215-1946">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="36215-1947">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="36215-1947">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="36215-1948">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="36215-1948">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="36215-1949">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="36215-1949">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="36215-1950">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="36215-1950">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="36215-1951">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1951">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-1952">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-1952">Az.Network</span></span>
* <span data-ttu-id="36215-1953">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="36215-1953">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="36215-1954">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-1954">New cmdlets</span></span>
        - <span data-ttu-id="36215-1955">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="36215-1955">New-AzNatGateway</span></span>
        - <span data-ttu-id="36215-1956">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="36215-1956">Get-AzNatGateway</span></span>
        - <span data-ttu-id="36215-1957">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="36215-1957">Set-AzNatGateway</span></span>
        - <span data-ttu-id="36215-1958">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="36215-1958">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="36215-1959">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-1959">Updated cmdlets</span></span>
        - <span data-ttu-id="36215-1960">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="36215-1960">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="36215-1961">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="36215-1961">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="36215-1962">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="36215-1962">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="36215-1963">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1963">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="36215-1964">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-1964">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36215-1965">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36215-1965">Az.PolicyInsights</span></span>
* <span data-ttu-id="36215-1966">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1966">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="36215-1967">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="36215-1967">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="36215-1968">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="36215-1968">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-1969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-1969">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-1970">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-1970">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="36215-1971">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="36215-1971">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="36215-1972">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="36215-1972">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="36215-1973">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="36215-1973">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="36215-1974">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="36215-1974">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="36215-1975">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="36215-1975">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="36215-1976">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="36215-1976">Az.Relay</span></span>
* <span data-ttu-id="36215-1977">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="36215-1977">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="36215-1978">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="36215-1978">Az.ServiceBus</span></span>
* <span data-ttu-id="36215-1979">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1979">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-1980">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-1980">Az.Storage</span></span>
* <span data-ttu-id="36215-1981">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="36215-1981">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="36215-1982">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="36215-1982">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="36215-1983">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="36215-1983">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="36215-1984">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-1984">New-AzStorageAccount</span></span>
* <span data-ttu-id="36215-1985">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="36215-1985">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="36215-1986">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-1986">New-AzStorageAccount</span></span>
    - <span data-ttu-id="36215-1987">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-1987">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="36215-1988">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-1988">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-1989">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-1989">Az.Websites</span></span>
* <span data-ttu-id="36215-1990">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="36215-1990">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="36215-1991">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="36215-1991">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="36215-1992">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="36215-1992">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="36215-1993">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="36215-1993">Highlights since the last major release</span></span>
* <span data-ttu-id="36215-1994">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-1994">General availability of `Az` module</span></span>
* <span data-ttu-id="36215-1995">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="36215-1995">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="36215-1996">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="36215-1996">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="36215-1997">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1997">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="36215-1998">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1998">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="36215-1999">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-1999">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="36215-2000">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-2000">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36215-2001">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-2001">Az.Accounts</span></span>
* <span data-ttu-id="36215-2002">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2002">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="36215-2003">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36215-2003">Az.Batch</span></span>
* <span data-ttu-id="36215-2004">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2004">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36215-2005">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36215-2005">Az.Cdn</span></span>
* <span data-ttu-id="36215-2006">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2006">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36215-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36215-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="36215-2008">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2008">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2009">Az.Compute</span></span>
* <span data-ttu-id="36215-2010">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2010">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="36215-2011">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2011">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="36215-2012">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2012">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-2013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-2013">Az.DataFactory</span></span>
* <span data-ttu-id="36215-2014">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2014">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-2015">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-2015">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-2016">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2016">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="36215-2017">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="36215-2017">Az.EventGrid</span></span>
* <span data-ttu-id="36215-2018">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2018">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36215-2019">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36215-2019">Az.EventHub</span></span>
* <span data-ttu-id="36215-2020">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2020">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="36215-2021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="36215-2021">Az.HDInsight</span></span>
* <span data-ttu-id="36215-2022">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2022">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36215-2023">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-2023">Az.IotHub</span></span>
* <span data-ttu-id="36215-2024">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2024">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36215-2025">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-2025">Az.KeyVault</span></span>
* <span data-ttu-id="36215-2026">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2026">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="36215-2027">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2027">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="36215-2028">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="36215-2028">Az.MachineLearning</span></span>
* <span data-ttu-id="36215-2029">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2029">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="36215-2030">Az.Media</span><span class="sxs-lookup"><span data-stu-id="36215-2030">Az.Media</span></span>
* <span data-ttu-id="36215-2031">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2031">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-2032">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-2032">Az.Monitor</span></span>
  * <span data-ttu-id="36215-2033">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="36215-2033">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="36215-2034">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="36215-2034">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="36215-2035">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="36215-2035">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="36215-2036">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="36215-2036">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="36215-2037">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="36215-2037">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="36215-2038">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="36215-2038">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="36215-2039">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2039">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-2040">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-2040">Az.Network</span></span>
* <span data-ttu-id="36215-2041">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2041">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="36215-2042">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2042">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="36215-2043">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="36215-2043">Az.NotificationHubs</span></span>
* <span data-ttu-id="36215-2044">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2044">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36215-2045">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36215-2045">Az.OperationalInsights</span></span>
* <span data-ttu-id="36215-2046">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2046">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="36215-2047">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="36215-2047">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="36215-2048">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2048">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-2049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-2049">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-2050">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2050">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="36215-2051">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="36215-2051">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="36215-2052">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2052">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="36215-2053">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2053">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="36215-2054">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="36215-2054">Az.RedisCache</span></span>
* <span data-ttu-id="36215-2055">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2055">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-2056">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2056">Az.Resources</span></span>
* <span data-ttu-id="36215-2057">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2057">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-2058">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-2058">Az.Sql</span></span>
* <span data-ttu-id="36215-2059">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2059">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="36215-2060">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2060">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="36215-2061">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2061">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="36215-2062">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2062">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="36215-2063">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2063">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="36215-2064">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-2064">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="36215-2065">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2065">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-2066">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-2066">Az.Websites</span></span>
* <span data-ttu-id="36215-2067">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2067">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="36215-2068">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2068">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="36215-2069">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2069">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="36215-2070">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="36215-2070">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="36215-2071">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="36215-2071">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="36215-2072">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="36215-2072">Highlights since the last major release</span></span>
* <span data-ttu-id="36215-2073">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-2073">General availability of `Az` module</span></span>
* <span data-ttu-id="36215-2074">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="36215-2074">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="36215-2075">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="36215-2075">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="36215-2076">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2076">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="36215-2077">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2077">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="36215-2078">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2078">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="36215-2079">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-2079">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="36215-2080">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-2080">Az.Accounts</span></span>
* <span data-ttu-id="36215-2081">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2081">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="36215-2082">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="36215-2082">Az.AnalysisServices</span></span>
* <span data-ttu-id="36215-2083">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="36215-2083">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="36215-2084">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="36215-2084">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36215-2085">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36215-2085">Az.Automation</span></span>
* <span data-ttu-id="36215-2086">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2086">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="36215-2087">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="36215-2087">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="36215-2088">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="36215-2088">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2089">Az.Compute</span></span>
* <span data-ttu-id="36215-2090">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2090">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="36215-2091">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2091">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="36215-2092">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="36215-2092">Az.ContainerInstance</span></span>
* <span data-ttu-id="36215-2093">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2093">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-2094">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-2094">Az.DataFactory</span></span>
* <span data-ttu-id="36215-2095">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2095">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="36215-2096">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2096">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-2097">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2097">Az.Resources</span></span>
* <span data-ttu-id="36215-2098">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2098">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="36215-2099">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2099">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="36215-2100">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="36215-2100">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="36215-2101">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="36215-2101">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="36215-2102">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2102">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="36215-2103">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="36215-2103">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-2104">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-2104">Az.Sql</span></span>
* <span data-ttu-id="36215-2105">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-2105">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-2106">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-2106">Az.Storage</span></span>
* <span data-ttu-id="36215-2107">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="36215-2107">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="36215-2108">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="36215-2108">New-AzStorageContext</span></span>
* <span data-ttu-id="36215-2109">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="36215-2109">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="36215-2110">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="36215-2110">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="36215-2111">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="36215-2111">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="36215-2112">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="36215-2112">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="36215-2113">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="36215-2113">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="36215-2114">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="36215-2114">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="36215-2115">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="36215-2115">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="36215-2116">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="36215-2116">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="36215-2117">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="36215-2117">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="36215-2118">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="36215-2118">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="36215-2119">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="36215-2119">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="36215-2120">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="36215-2120">Highlights since the last major release</span></span>
* <span data-ttu-id="36215-2121">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-2121">General availability of `Az` module</span></span>
* <span data-ttu-id="36215-2122">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="36215-2122">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="36215-2123">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="36215-2123">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="36215-2124">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2124">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="36215-2125">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2125">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="36215-2126">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2126">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="36215-2127">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-2127">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36215-2128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36215-2128">Az.Automation</span></span>
* <span data-ttu-id="36215-2129">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="36215-2129">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="36215-2130">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="36215-2130">Dynamic grouping</span></span>
    * <span data-ttu-id="36215-2131">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="36215-2131">Pre-Post script</span></span>
    * <span data-ttu-id="36215-2132">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="36215-2132">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-2133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2133">Az.Compute</span></span>
* <span data-ttu-id="36215-2134">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="36215-2134">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="36215-2135">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2135">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36215-2136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-2136">Az.KeyVault</span></span>
* <span data-ttu-id="36215-2137">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2137">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-2138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-2138">Az.Network</span></span>
* <span data-ttu-id="36215-2139">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2139">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="36215-2140">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2140">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-2141">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-2141">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-2142">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2142">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="36215-2143">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2143">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-2144">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2144">Az.Resources</span></span>
* <span data-ttu-id="36215-2145">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2145">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="36215-2146">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2146">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-2147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-2147">Az.Sql</span></span>
* <span data-ttu-id="36215-2148">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2148">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-2149">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-2149">Az.Storage</span></span>
* <span data-ttu-id="36215-2150">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="36215-2150">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="36215-2151">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="36215-2151">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="36215-2152">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="36215-2152">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="36215-2153">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="36215-2153">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="36215-2154">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="36215-2154">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="36215-2155">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="36215-2155">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="36215-2156">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="36215-2156">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-2157">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-2157">Az.Websites</span></span>
* <span data-ttu-id="36215-2158">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2158">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="36215-2159">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="36215-2159">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-2160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-2160">Az.Accounts</span></span>
* <span data-ttu-id="36215-2161">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2161">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="36215-2162">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2162">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36215-2163">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36215-2163">Az.Automation</span></span>
* <span data-ttu-id="36215-2164">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2164">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="36215-2165">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2165">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="36215-2166">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="36215-2166">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36215-2167">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36215-2167">Az.Cdn</span></span>
* <span data-ttu-id="36215-2168">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="36215-2168">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-2169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2169">Az.Compute</span></span>
* <span data-ttu-id="36215-2170">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2170">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-2171">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-2171">Az.DataFactory</span></span>
* <span data-ttu-id="36215-2172">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2172">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="36215-2173">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="36215-2173">Az.LogicApp</span></span>
* <span data-ttu-id="36215-2174">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="36215-2174">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-2175">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-2175">Az.Network</span></span>
* <span data-ttu-id="36215-2176">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2176">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-2177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-2177">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-2178">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2178">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="36215-2179">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="36215-2179">SDK Update</span></span>
* <span data-ttu-id="36215-2180">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-2180">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="36215-2181">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2181">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-2182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2182">Az.Resources</span></span>
* <span data-ttu-id="36215-2183">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2183">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="36215-2184">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="36215-2184">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="36215-2185">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2185">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="36215-2186">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="36215-2186">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="36215-2187">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2187">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="36215-2188">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="36215-2188">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-2189">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-2189">Az.Sql</span></span>
* <span data-ttu-id="36215-2190">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="36215-2190">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="36215-2191">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="36215-2191">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-2192">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-2192">Az.Storage</span></span>
* <span data-ttu-id="36215-2193">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36215-2193">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="36215-2194">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="36215-2194">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="36215-2195">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="36215-2195">Az.AnalysisServices</span></span>
* <span data-ttu-id="36215-2196">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="36215-2196">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36215-2197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36215-2197">Az.Automation</span></span>
* <span data-ttu-id="36215-2198">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2198">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="36215-2199">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2199">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="36215-2200">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2200">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36215-2201">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36215-2201">Az.CognitiveServices</span></span>
* <span data-ttu-id="36215-2202">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2202">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-2203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2203">Az.Compute</span></span>
* <span data-ttu-id="36215-2204">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2204">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="36215-2205">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2205">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="36215-2206">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2206">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="36215-2207">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="36215-2207">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-2208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-2208">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-2209">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2209">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="36215-2210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="36215-2210">Az.EventHub</span></span>
* <span data-ttu-id="36215-2211">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2211">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36215-2212">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-2212">Az.KeyVault</span></span>
* <span data-ttu-id="36215-2213">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2213">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="36215-2214">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="36215-2214">Az.LogicApp</span></span>
* <span data-ttu-id="36215-2215">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2215">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="36215-2216">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2216">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="36215-2217">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-2217">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="36215-2218">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="36215-2218">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="36215-2219">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="36215-2219">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="36215-2220">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="36215-2220">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="36215-2221">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="36215-2221">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="36215-2222">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="36215-2222">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="36215-2223">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="36215-2223">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="36215-2224">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="36215-2224">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="36215-2225">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="36215-2225">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="36215-2226">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="36215-2226">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="36215-2227">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2227">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="36215-2228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-2228">Az.Monitor</span></span>
* <span data-ttu-id="36215-2229">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2229">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-2230">Az.Network</span></span>
* <span data-ttu-id="36215-2231">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2231">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="36215-2232">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36215-2232">Az.OperationalInsights</span></span>
* <span data-ttu-id="36215-2233">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="36215-2233">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="36215-2234">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2234">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="36215-2235">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2235">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-2236">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2236">Az.Resources</span></span>
* <span data-ttu-id="36215-2237">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2237">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="36215-2238">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2238">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="36215-2239">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2239">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="36215-2240">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2240">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-2241">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-2241">Az.Sql</span></span>
* <span data-ttu-id="36215-2242">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2242">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="36215-2243">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2243">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-2244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-2244">Az.Websites</span></span>
* <span data-ttu-id="36215-2245">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2245">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="36215-2246">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="36215-2246">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-2247">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-2247">Az.Accounts</span></span>
* <span data-ttu-id="36215-2248">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="36215-2248">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="36215-2249">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="36215-2249">Az.AnalysisServices</span></span>
<span data-ttu-id="36215-2250">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="36215-2250">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-2251">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2251">Az.Compute</span></span>
* <span data-ttu-id="36215-2252">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2252">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="36215-2253">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2253">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="36215-2254">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2254">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-2255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-2255">Az.RecoveryServices</span></span>
<span data-ttu-id="36215-2256">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="36215-2256">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-2257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2257">Az.Resources</span></span>
* <span data-ttu-id="36215-2258">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2258">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="36215-2259">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="36215-2259">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="36215-2260">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2260">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="36215-2261">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="36215-2261">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-2262">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-2262">Az.Sql</span></span>
* <span data-ttu-id="36215-2263">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="36215-2263">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="36215-2264">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2264">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="36215-2265">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2265">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="36215-2266">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="36215-2266">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-2267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-2267">Az.Accounts</span></span>
* <span data-ttu-id="36215-2268">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="36215-2268">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="36215-2269">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="36215-2269">Az.AnalysisServices</span></span>
* <span data-ttu-id="36215-2270">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="36215-2270">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="36215-2271">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-2271">Az.RecoveryServices</span></span>
* <span data-ttu-id="36215-2272">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="36215-2272">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="36215-2273">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="36215-2273">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-2274">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-2274">Az.Accounts</span></span>
* <span data-ttu-id="36215-2275">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2275">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="36215-2276">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2276">Update incorrect online help URLs</span></span>
* <span data-ttu-id="36215-2277">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2277">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="36215-2278">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="36215-2278">Az.Aks</span></span>
* <span data-ttu-id="36215-2279">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2279">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="36215-2280">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36215-2280">Az.Automation</span></span>
* <span data-ttu-id="36215-2281">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2281">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="36215-2282">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2282">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="36215-2283">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="36215-2283">Az.Cdn</span></span>
* <span data-ttu-id="36215-2284">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2284">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-2285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2285">Az.Compute</span></span>
* <span data-ttu-id="36215-2286">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2286">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="36215-2287">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2287">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="36215-2288">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2288">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="36215-2289">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="36215-2289">Az.ContainerRegistry</span></span>
* <span data-ttu-id="36215-2290">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2290">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="36215-2291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="36215-2291">Az.DataFactory</span></span>
* <span data-ttu-id="36215-2292">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2292">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-2293">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-2293">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-2294">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2294">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="36215-2295">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="36215-2295">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="36215-2296">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2296">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36215-2297">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-2297">Az.IotHub</span></span>
* <span data-ttu-id="36215-2298">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2298">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="36215-2299">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-2299">Az.KeyVault</span></span>
* <span data-ttu-id="36215-2300">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2300">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-2301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-2301">Az.Network</span></span>
* <span data-ttu-id="36215-2302">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2302">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-2303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2303">Az.Resources</span></span>
* <span data-ttu-id="36215-2304">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2304">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="36215-2305">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2305">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="36215-2306">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2306">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="36215-2307">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2307">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="36215-2308">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2308">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="36215-2309">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2309">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="36215-2310">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="36215-2310">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36215-2311">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36215-2311">Az.ServiceFabric</span></span>
* <span data-ttu-id="36215-2312">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="36215-2312">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="36215-2313">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2313">Fix some error messages.</span></span>
* <span data-ttu-id="36215-2314">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2314">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="36215-2315">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2315">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="36215-2316">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="36215-2316">Az.SignalR</span></span>
* <span data-ttu-id="36215-2317">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2317">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-2318">Az.Sql</span></span>
* <span data-ttu-id="36215-2319">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2319">Update incorrect online help URLs</span></span>
* <span data-ttu-id="36215-2320">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2320">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="36215-2321">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2321">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="36215-2322">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="36215-2322">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-2323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-2323">Az.Storage</span></span>
* <span data-ttu-id="36215-2324">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2324">Update incorrect online help URLs</span></span>
* <span data-ttu-id="36215-2325">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="36215-2325">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="36215-2326">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="36215-2326">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="36215-2327">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="36215-2327">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="36215-2328">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="36215-2328">Az.TrafficManager</span></span>
* <span data-ttu-id="36215-2329">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2329">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-2330">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-2330">Az.Websites</span></span>
* <span data-ttu-id="36215-2331">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2331">Update incorrect online help URLs</span></span>
* <span data-ttu-id="36215-2332">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2332">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="36215-2333">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2333">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="36215-2334">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="36215-2334">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="36215-2335">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-2335">Az.Accounts</span></span>
* <span data-ttu-id="36215-2336">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2336">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-2337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2337">Az.Compute</span></span>
* <span data-ttu-id="36215-2338">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="36215-2338">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="36215-2339">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2339">Updated the description of ID in help files</span></span>
* <span data-ttu-id="36215-2340">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="36215-2340">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-2341">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-2341">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-2342">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2342">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="36215-2343">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2343">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="36215-2344">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="36215-2344">Az.EventGrid</span></span>
* <span data-ttu-id="36215-2345">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2345">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="36215-2346">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2346">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="36215-2347">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-2347">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="36215-2348">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="36215-2348">Event Time-To-Live,</span></span>
        - <span data-ttu-id="36215-2349">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="36215-2349">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="36215-2350">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="36215-2350">Dead letter endpoint.</span></span>
    - <span data-ttu-id="36215-2351">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-2351">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="36215-2352">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="36215-2352">Event Time-To-Live,</span></span>
        - <span data-ttu-id="36215-2353">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="36215-2353">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="36215-2354">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="36215-2354">Dead letter endpoint.</span></span>
* <span data-ttu-id="36215-2355">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2355">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="36215-2356">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="36215-2356">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="36215-2357">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="36215-2357">Az.IotHub</span></span>
* <span data-ttu-id="36215-2358">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2358">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="36215-2359">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="36215-2359">Az.LogicApp</span></span>
* <span data-ttu-id="36215-2360">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="36215-2360">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-2361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2361">Az.Resources</span></span>
* <span data-ttu-id="36215-2362">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2362">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="36215-2363">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="36215-2363">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="36215-2364">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2364">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="36215-2365">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2365">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="36215-2366">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2366">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="36215-2367">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="36215-2367">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="36215-2368">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="36215-2368">Az.SignalR</span></span>
* <span data-ttu-id="36215-2369">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="36215-2369">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-2370">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-2370">Az.Sql</span></span>
* <span data-ttu-id="36215-2371">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="36215-2371">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="36215-2372">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-2372">Az.Storage</span></span>
* <span data-ttu-id="36215-2373">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="36215-2373">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="36215-2374">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="36215-2374">New-AzStorageContext</span></span>
* <span data-ttu-id="36215-2375">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2375">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="36215-2376">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="36215-2376">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-2377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-2377">Az.Websites</span></span>
* <span data-ttu-id="36215-2378">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2378">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="36215-2379">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="36215-2379">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="36215-2380">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="36215-2380">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="36215-2381">Genel</span><span class="sxs-lookup"><span data-stu-id="36215-2381">General</span></span>

- <span data-ttu-id="36215-2382">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-2382">General Availability of Az Module</span></span>
- <span data-ttu-id="36215-2383">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="36215-2383">Online help for each module</span></span>
- <span data-ttu-id="36215-2384">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="36215-2384">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="36215-2385">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2385">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="36215-2386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="36215-2386">Az.Accounts</span></span>
- <span data-ttu-id="36215-2387">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="36215-2387">Changed from Az.Profile</span></span>
- <span data-ttu-id="36215-2388">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2388">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="36215-2389">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36215-2389">Az.ApiManagement</span></span>
- <span data-ttu-id="36215-2390">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="36215-2390">Fixes for #7002</span></span>
- <span data-ttu-id="36215-2391">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2391">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="36215-2392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="36215-2392">Az.Batch</span></span>
- <span data-ttu-id="36215-2393">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2393">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="36215-2394">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="36215-2394">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="36215-2395">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2395">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="36215-2396">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="36215-2396">Az.Billing</span></span>
- <span data-ttu-id="36215-2397">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2397">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="36215-2398">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="36215-2398">Az.CognitivServices</span></span>
- <span data-ttu-id="36215-2399">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2399">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="36215-2400">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-2400">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="36215-2401">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="36215-2401">Az.ContainerInstance</span></span>
- <span data-ttu-id="36215-2402">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2402">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="36215-2403">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="36215-2403">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="36215-2404">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2404">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="36215-2405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-2405">Az.DataLakeStore</span></span>
- <span data-ttu-id="36215-2406">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2406">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="36215-2407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="36215-2407">Az.Monitor</span></span>
- <span data-ttu-id="36215-2408">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2408">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="36215-2409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="36215-2409">Az.KeyVault</span></span>
- <span data-ttu-id="36215-2410">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-2410">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="36215-2411">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="36215-2411">Az.MachineLearning</span></span>
- <span data-ttu-id="36215-2412">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2412">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="36215-2413">Az.Media</span><span class="sxs-lookup"><span data-stu-id="36215-2413">Az.Media</span></span>
- <span data-ttu-id="36215-2414">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="36215-2414">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="36215-2415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-2415">Az.Network</span></span>
<span data-ttu-id="36215-2416">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2416">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="36215-2417">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="36215-2417">New cmdlets added:</span></span>
        - <span data-ttu-id="36215-2418">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="36215-2418">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="36215-2419">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="36215-2419">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="36215-2420">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="36215-2420">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="36215-2421">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="36215-2421">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="36215-2422">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="36215-2422">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="36215-2423">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="36215-2423">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="36215-2424">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="36215-2424">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="36215-2425">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="36215-2425">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="36215-2426">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2426">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="36215-2427">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36215-2427">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="36215-2428">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="36215-2428">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="36215-2429">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="36215-2429">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="36215-2430">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36215-2430">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="36215-2431">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="36215-2431">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="36215-2432">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="36215-2432">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="36215-2433">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2433">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="36215-2434">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="36215-2434">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="36215-2435">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="36215-2435">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="36215-2436">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="36215-2436">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="36215-2437">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2437">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="36215-2438">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2438">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="36215-2439">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="36215-2439">Az.OperationalInsights</span></span>
- <span data-ttu-id="36215-2440">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2440">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="36215-2441">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="36215-2441">Az.Profile</span></span>
- <span data-ttu-id="36215-2442">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2442">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="36215-2443">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-2443">Az.RecoveryServices</span></span>
- <span data-ttu-id="36215-2444">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2444">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="36215-2445">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2445">Az.Resources</span></span>
- <span data-ttu-id="36215-2446">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2446">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="36215-2447">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36215-2447">Az.ServiceFabric</span></span>
- <span data-ttu-id="36215-2448">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="36215-2448">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="36215-2449">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2449">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="36215-2450">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="36215-2450">Az.SIgnalR</span></span>
- <span data-ttu-id="36215-2451">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="36215-2451">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="36215-2452">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-2452">Az.Sql</span></span>
- <span data-ttu-id="36215-2453">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2453">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="36215-2454">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2454">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="36215-2455">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2455">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="36215-2456">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-2456">Az.Storage</span></span>
- <span data-ttu-id="36215-2457">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2457">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="36215-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-2458">Az.Websites</span></span>
- <span data-ttu-id="36215-2459">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="36215-2459">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="36215-2460">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="36215-2460">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="36215-2461">Genel</span><span class="sxs-lookup"><span data-stu-id="36215-2461">General</span></span>

* <span data-ttu-id="36215-2462">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="36215-2462">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="36215-2463">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2463">Az.Compute</span></span>

* <span data-ttu-id="36215-2464">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2464">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="36215-2465">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-2465">Az.DataLakeStore</span></span>

* <span data-ttu-id="36215-2466">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2466">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="36215-2467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="36215-2467">Az.FrontDoor</span></span>

* <span data-ttu-id="36215-2468">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2468">Fixed some broken links</span></span>
    - <span data-ttu-id="36215-2469">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2469">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="36215-2470">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2470">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="36215-2471">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="36215-2471">Az.RecoveryServices</span></span>

* <span data-ttu-id="36215-2472">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2472">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="36215-2473">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2473">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="36215-2474">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2474">Az.Resources</span></span>

* <span data-ttu-id="36215-2475">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="36215-2475">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="36215-2476">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2476">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="36215-2477">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-2477">Az.Sql</span></span>

* <span data-ttu-id="36215-2478">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="36215-2478">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="36215-2479">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2479">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="36215-2480">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2480">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="36215-2481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="36215-2481">Az.Storage</span></span>

* <span data-ttu-id="36215-2482">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2482">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="36215-2483">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2483">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="36215-2484">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="36215-2484">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="36215-2485">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2485">Support Static Website configuration</span></span>
    - <span data-ttu-id="36215-2486">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="36215-2486">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="36215-2487">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="36215-2487">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="36215-2488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-2488">Az.Websites</span></span>

* <span data-ttu-id="36215-2489">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36215-2489">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="36215-2490">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2490">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="36215-2491">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="36215-2491">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="36215-2492">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="36215-2492">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="36215-2493">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="36215-2493">Az.ApiManagement</span></span>
* <span data-ttu-id="36215-2494">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="36215-2494">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="36215-2495">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="36215-2495">Az.Automation</span></span>
* <span data-ttu-id="36215-2496">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="36215-2496">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="36215-2497">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2497">Added Update Management cmdlets</span></span>
* <span data-ttu-id="36215-2498">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2498">Added Source Control cmdlets</span></span>
* <span data-ttu-id="36215-2499">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2499">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="36215-2500">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2500">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="36215-2501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2501">Az.Compute</span></span>
* <span data-ttu-id="36215-2502">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2502">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="36215-2503">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="36215-2503">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="36215-2504">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="36215-2504">Az.ContainerInstance</span></span>
* <span data-ttu-id="36215-2505">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="36215-2505">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="36215-2506">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="36215-2506">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="36215-2507">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2507">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="36215-2508">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-2508">Az.Network</span></span>
* <span data-ttu-id="36215-2509">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2509">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="36215-2510">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2510">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="36215-2511">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2511">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="36215-2512">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2512">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="36215-2513">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="36215-2513">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="36215-2514">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2514">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="36215-2515">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="36215-2515">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="36215-2516">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="36215-2516">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="36215-2517">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2517">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="36215-2518">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="36215-2518">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="36215-2519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="36215-2519">Az.Relay</span></span>
* <span data-ttu-id="36215-2520">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2520">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="36215-2521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2521">Az.Resources</span></span>
* <span data-ttu-id="36215-2522">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2522">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="36215-2523">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2523">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="36215-2524">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="36215-2524">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="36215-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36215-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="36215-2526">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2526">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="36215-2527">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-2527">Az.Sql</span></span>
* <span data-ttu-id="36215-2528">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2528">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="36215-2529">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="36215-2529">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="36215-2530">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="36215-2530">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="36215-2531">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="36215-2531">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="36215-2532">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="36215-2532">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="36215-2533">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="36215-2533">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="36215-2534">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="36215-2534">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="36215-2535">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="36215-2535">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="36215-2536">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="36215-2536">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="36215-2537">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2537">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="36215-2538">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2538">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="36215-2539">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2539">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="36215-2540">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="36215-2540">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="36215-2541">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="36215-2541">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="36215-2542">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="36215-2542">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="36215-2543">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="36215-2543">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="36215-2544">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2544">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="36215-2545">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="36215-2545">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="36215-2546">Genel</span><span class="sxs-lookup"><span data-stu-id="36215-2546">General</span></span>
* <span data-ttu-id="36215-2547">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="36215-2547">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="36215-2548">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="36215-2548">Az.Profile</span></span>
* <span data-ttu-id="36215-2549">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2549">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="36215-2550">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2550">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="36215-2551">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2551">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="36215-2552">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2552">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="36215-2553">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2553">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="36215-2554">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2554">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="36215-2555">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2555">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="36215-2556">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36215-2556">Az.CognitiveServices</span></span>
* <span data-ttu-id="36215-2557">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2557">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-2558">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2558">Az.Compute</span></span>
* <span data-ttu-id="36215-2559">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2559">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="36215-2560">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="36215-2560">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="36215-2561">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2561">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-2562">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-2563">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2563">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="36215-2564">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2564">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="36215-2565">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="36215-2565">Az.Insights</span></span>
* <span data-ttu-id="36215-2566">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2566">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="36215-2567">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="36215-2567">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="36215-2568">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2568">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="36215-2569">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="36215-2569">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-2570">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-2570">Az.Network</span></span>
* <span data-ttu-id="36215-2571">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="36215-2571">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="36215-2572">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="36215-2572">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="36215-2573">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="36215-2573">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="36215-2574">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="36215-2574">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="36215-2575">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="36215-2575">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="36215-2576">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="36215-2576">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="36215-2577">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="36215-2577">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="36215-2578">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="36215-2578">Az.PolicyInsights</span></span>
* <span data-ttu-id="36215-2579">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2579">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-2580">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2580">Az.Resources</span></span>
* <span data-ttu-id="36215-2581">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="36215-2581">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="36215-2582">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="36215-2582">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="36215-2583">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="36215-2583">Az.ServiceBus</span></span>
* <span data-ttu-id="36215-2584">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2584">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="36215-2585">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="36215-2585">Az.ServiceFabric</span></span>
* <span data-ttu-id="36215-2586">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2586">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="36215-2587">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2587">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="36215-2588">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="36215-2588">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="36215-2589">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="36215-2589">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="36215-2590">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2590">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="36215-2591">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="36215-2591">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="36215-2592">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="36215-2592">Az.Profile</span></span>
* <span data-ttu-id="36215-2593">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="36215-2593">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="36215-2594">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="36215-2594">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-2595">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2595">Az.Compute</span></span>
* <span data-ttu-id="36215-2596">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2596">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="36215-2597">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2597">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="36215-2598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36215-2598">Az.DataLakeStore</span></span>
* <span data-ttu-id="36215-2599">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="36215-2599">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="36215-2600">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="36215-2600">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="36215-2601">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="36215-2601">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="36215-2602">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="36215-2602">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="36215-2603">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="36215-2603">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-2604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-2604">Az.Network</span></span>
* <span data-ttu-id="36215-2605">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="36215-2605">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="36215-2606">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2606">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-2607">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2607">Az.Resources</span></span>
* <span data-ttu-id="36215-2608">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2608">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="36215-2609">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="36215-2609">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="36215-2610">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="36215-2610">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="36215-2611">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="36215-2611">Azure.Storage</span></span>
* <span data-ttu-id="36215-2612">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="36215-2612">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="36215-2613">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="36215-2613">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="36215-2614">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="36215-2614">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="36215-2615">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="36215-2615">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="36215-2616">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="36215-2616">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="36215-2617">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="36215-2617">Az.CognitiveServices</span></span>
* <span data-ttu-id="36215-2618">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="36215-2618">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="36215-2619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="36215-2619">Az.Compute</span></span>
* <span data-ttu-id="36215-2620">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2620">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="36215-2621">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2621">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="36215-2622">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2622">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="36215-2623">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="36215-2623">Az.DataFactoryV2</span></span>
* <span data-ttu-id="36215-2624">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="36215-2624">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="36215-2625">Az.Network</span><span class="sxs-lookup"><span data-stu-id="36215-2625">Az.Network</span></span>
* <span data-ttu-id="36215-2626">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="36215-2626">Added NetworkProfile functionality.</span></span> <span data-ttu-id="36215-2627">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2627">new cmdlets added</span></span>
    - <span data-ttu-id="36215-2628">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="36215-2628">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="36215-2629">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="36215-2629">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="36215-2630">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="36215-2630">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="36215-2631">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="36215-2631">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="36215-2632">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="36215-2632">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="36215-2633">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="36215-2633">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="36215-2634">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2634">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="36215-2635">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2635">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="36215-2636">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2636">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="36215-2637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="36215-2637">Az.RedisCache</span></span>
* <span data-ttu-id="36215-2638">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="36215-2638">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="36215-2639">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2639">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="36215-2640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="36215-2640">Az.Resources</span></span>
* <span data-ttu-id="36215-2641">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="36215-2641">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="36215-2642">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2642">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="36215-2643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="36215-2643">Az.Sql</span></span>
* <span data-ttu-id="36215-2644">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="36215-2644">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="36215-2645">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="36215-2645">Az.Websites</span></span>
* <span data-ttu-id="36215-2646">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="36215-2646">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="36215-2647">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="36215-2647">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="36215-2648">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="36215-2648">0.2.0 - September 2018</span></span>
 <span data-ttu-id="36215-2649">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="36215-2649">Initial Release</span></span>
