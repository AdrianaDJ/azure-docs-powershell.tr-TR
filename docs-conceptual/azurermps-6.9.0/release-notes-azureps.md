---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 3cb71087a61a0fcd06c014394e8f9e5654d4c1a8
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47179012"
---
# <a name="release-notes"></a><span data-ttu-id="a68a3-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="a68a3-103">Release notes</span></span>

<span data-ttu-id="a68a3-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a68a3-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="690---september-2018"></a><span data-ttu-id="a68a3-105">6.9.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="a68a3-105">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a68a3-106">Genel</span><span class="sxs-lookup"><span data-stu-id="a68a3-106">General</span></span>
* <span data-ttu-id="a68a3-107">AzureRM.SignalR, AzureRM toplu modülüne eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-107">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a68a3-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a68a3-108">AzureRM.Profile</span></span>
* <span data-ttu-id="a68a3-109">Depolama ortak kodunda küçük değişiklikler yapıldı</span><span class="sxs-lookup"><span data-stu-id="a68a3-109">Minor changes to the storage common code</span></span>
* <span data-ttu-id="a68a3-110">Yardım dosyaları tüm parametre türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-110">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="a68a3-111">ServicePrincipalCertificateWithSubscriptionId parametre kümesindeki -ServicePrincipal parametresi zorunlu olmaktan çıkarıldı</span><span class="sxs-lookup"><span data-stu-id="a68a3-111">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="a68a3-112">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="a68a3-112">Azure.Storage</span></span>
* <span data-ttu-id="a68a3-113">OAuth ile Depolama Bağlamı oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-113">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="a68a3-114">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a68a3-114">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="a68a3-115">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="a68a3-115">AzureRM.Cdn</span></span>
* <span data-ttu-id="a68a3-116">CDN fiyatlandırma SKU'suna Standard_Microsoft eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-116">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="a68a3-117">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a68a3-117">AzureRM.Compute</span></span>
* <span data-ttu-id="a68a3-118">Keyvault ve Storage bağımlılıkları ortak bağımlılıklara taşındı</span><span class="sxs-lookup"><span data-stu-id="a68a3-118">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="a68a3-119">AEM cmdlet'lerine daha fazla sanal makine boyutu için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-119">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="a68a3-120">New-AzureRmVmssIpConfig cmdlet'ine Add PublicIPPrefix parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-120">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a68a3-121">Invoke-AzureRmVMRunCommand cmdlet'ine ResourceId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-121">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="a68a3-122">Invoke-AzureRmVmssVMRunCommand cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-122">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="a68a3-123">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a68a3-123">AzureRM.Dns</span></span>
* <span data-ttu-id="a68a3-124">DNS kaydı oluşturma işlemi sırasında diğer ad kaydı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-124">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a68a3-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a68a3-125">AzureRM.Insights</span></span>
* <span data-ttu-id="a68a3-126">6833 ve 7102 numaralı sorunlar giderildi (Tanılama Ayarları bölümü)</span><span class="sxs-lookup"><span data-stu-id="a68a3-126">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="a68a3-127">Tanılama ayarlarını oluşturma ve listeleme/alma sırasında karşılaşılan varsayılan ad 'service' sorunları</span><span class="sxs-lookup"><span data-stu-id="a68a3-127">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="a68a3-128">Kategoriye sahip tanılama ayarı oluşturma sorunları</span><span class="sxs-lookup"><span data-stu-id="a68a3-128">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="a68a3-129">Ölçümler zaman dilimi parametreleri için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-129">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="a68a3-130">Zaman dilimi parametreleri yine kabul ediliyor (bu bir hataya neden olan değişiklik değil) ancak yalnızca PT1M geçerli olduğu için bu parametreler arka uçta yoksayılıyor</span><span class="sxs-lookup"><span data-stu-id="a68a3-130">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a68a3-131">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a68a3-131">AzureRM.Network</span></span>
* <span data-ttu-id="a68a3-132">LoadBalancer cmdlet'lerinde değişiklikler yapıldı</span><span class="sxs-lookup"><span data-stu-id="a68a3-132">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="a68a3-133">LoadBalancerInboundNatPoolConfig: IdleTimeoutInMinutes, EnableFloatingIp ve EnableTcpReset parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-133">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="a68a3-134">LoadBalancerInboundNatRuleConfig: EnableTcpReset parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-134">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="a68a3-135">LoadBalancerRuleConfig: EnableTcpReset parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-135">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="a68a3-136">LoadBalancerProbeConfig: Protocol parametresi için "Https" değeri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-136">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="a68a3-137">Yeni LoadBalancer alt kaynağı OutboundRule için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-137">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="a68a3-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a68a3-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a68a3-140">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-140">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a68a3-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a68a3-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="a68a3-143">PSNetworkInterface için yeni HostedWorkloads özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-143">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="a68a3-144">ARM aracılığıyla Azure Güvenlik Duvarı özelliği için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-144">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="a68a3-145">Get-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-145">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="a68a3-146">Set-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-146">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="a68a3-147">New-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-147">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="a68a3-148">Remove-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-148">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="a68a3-149">New-AzureRmFirewallApplicationRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-149">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="a68a3-150">New-AzureRmFirewallApplicationRule eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-150">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="a68a3-151">New-AzureRmFirewallNatRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-151">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="a68a3-152">New-AzureRmFirewallNatRule eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-152">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="a68a3-153">New-AzureRmFirewallNetworkRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-153">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="a68a3-154">New-AzureRmFirewallNetworkRule eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-154">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="a68a3-155">Application Gateway'de Güvenilen Kök sertifika ve Otomatik ölçeklendirme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-155">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="a68a3-156">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="a68a3-156">New Cmdlets added:</span></span>
      - <span data-ttu-id="a68a3-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a68a3-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a68a3-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a68a3-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a68a3-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a68a3-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a68a3-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a68a3-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a68a3-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a68a3-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a68a3-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a68a3-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="a68a3-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a68a3-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="a68a3-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a68a3-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="a68a3-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a68a3-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="a68a3-166">Cmdlet'ler isteğe bağlı -TrustedRootCertificate parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-166">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="a68a3-167">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a68a3-167">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="a68a3-168">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a68a3-168">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="a68a3-169">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a68a3-169">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="a68a3-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a68a3-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="a68a3-171">Cmdlet'ler isteğe bağlı -AutoscaleConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-171">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="a68a3-172">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a68a3-172">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="a68a3-173">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a68a3-173">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="a68a3-174">Arabirim Uç Noktası için Get-AzureInterfaceEndpoint cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-174">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="a68a3-175">Bir alt ağda birden fazla adres ön eki için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-175">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="a68a3-176">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="a68a3-176">Updated cmdlets:</span></span>
  - <span data-ttu-id="a68a3-177">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-177">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a68a3-178">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-178">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a68a3-179">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-179">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a68a3-180">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-180">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a68a3-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a68a3-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="a68a3-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="a68a3-183">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-183">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="a68a3-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="a68a3-185">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a68a3-185">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="a68a3-186">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a68a3-186">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="a68a3-187">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a68a3-187">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="a68a3-188">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-188">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="a68a3-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="a68a3-190">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-190">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="a68a3-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="a68a3-192">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-192">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="a68a3-193">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-193">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="a68a3-194">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-194">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="a68a3-195">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a68a3-195">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="a68a3-196">Alt ağ temsilcisi seçme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-196">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="a68a3-197">New-AzureRmDelegation: Bir alt ağa eklenebilecek yeni bir temsilci oluşturur</span><span class="sxs-lookup"><span data-stu-id="a68a3-197">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="a68a3-198">Remove-AzureRmDelegation: Bir alt ağı alır ve belirtilen temsilci adını o alt ağdan kaldırır</span><span class="sxs-lookup"><span data-stu-id="a68a3-198">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="a68a3-199">Add-AzureRmDelegation: Bir alt ağı alır ve belirtilen hizmet adını o alt ağa temsilci olarak ekler</span><span class="sxs-lookup"><span data-stu-id="a68a3-199">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="a68a3-200">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="a68a3-200">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="a68a3-201">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="a68a3-201">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a68a3-202">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a68a3-202">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a68a3-203">Yönetilen disk desteği</span><span class="sxs-lookup"><span data-stu-id="a68a3-203">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a68a3-204">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a68a3-204">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a68a3-205">Insights bağımlılığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-205">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a68a3-206">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a68a3-206">AzureRM.Resources</span></span>
* <span data-ttu-id="a68a3-207">New-AzureRmResourceGroupDeployment cmdlet'i yeni RollbackAction parametresi eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-207">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="a68a3-208">Yeni parametreyle OnErrorDeployment desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-208">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="a68a3-209">İlke atamalarında yönetilen kimlik desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-209">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="a68a3-210">Varsayılan değerlere sahip parametrelerin artık 'New-AzureRmPolicyAssignment' ile ilke atama işlemi sırasında belirtilmesi zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="a68a3-210">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="a68a3-211">İlke diğer adlarını almak için yeni Get-AzureRmPolicyAlias cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-211">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a68a3-212">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a68a3-212">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a68a3-213">7161 numaralı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-213">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="a68a3-214">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="a68a3-214">AzureRM.SignalR</span></span>
* <span data-ttu-id="a68a3-215">SKU adları Free_F1 ve Standard_S1 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-215">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="a68a3-216">PSSignalRResource nesnesine sürüm alanı, PSSignalRKeys nesnesine de bağlantı dizesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-216">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a68a3-217">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a68a3-217">AzureRM.Storage</span></span>
* <span data-ttu-id="a68a3-218">AzureRm.Storage için Değiştirilemezlik İlkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-218">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="a68a3-219">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a68a3-219">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="a68a3-220">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a68a3-220">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a68a3-221">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a68a3-221">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a68a3-222">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a68a3-222">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a68a3-223">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a68a3-223">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a68a3-224">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="a68a3-224">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="a68a3-225">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="a68a3-225">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="a68a3-226">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a68a3-226">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="a68a3-227">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a68a3-227">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="a68a3-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a68a3-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="a68a3-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a68a3-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a68a3-230">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a68a3-230">AzureRM.Websites</span></span>
* <span data-ttu-id="a68a3-231">İki yeni cmdlet eklendi: Get-AzureRmDeletedWebApp ve Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a68a3-231">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="a68a3-232">Windows kapsayıcısı ile App Service planı oluşturmak için New-AzureRmAppServicePlan -HyperV anahtarı eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-232">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="a68a3-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Windows kapsayıcı uygulaması oluşturmak ve yönetmek için yeni parametreler (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="a68a3-234">6.8.1 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="a68a3-234">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a68a3-235">Genel</span><span class="sxs-lookup"><span data-stu-id="a68a3-235">General</span></span>
* <span data-ttu-id="a68a3-236">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-236">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="a68a3-237">Ortak çalışma zamanı bütünleştirilmiş kodları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-237">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a68a3-238">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a68a3-238">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a68a3-239">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-239">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="a68a3-240">https://github.com/Azure/azure-powershell/issues/6603 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-240">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="a68a3-241">Import-AzureRmApiManagementApi ve \*-AzureRmApiManagementCertificate cmdlet’leri artık göreli yolları işleyebiliyor</span><span class="sxs-lookup"><span data-stu-id="a68a3-241">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="a68a3-242">https://github.com/Azure/azure-powershell/issues/6879 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-242">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="a68a3-243">CertificateInformation, Set-AzureRmApiManagement cmdlet’inin düzgün çalışmasını sağlayan, ayarlanabilir bir özelliktir.</span><span class="sxs-lookup"><span data-stu-id="a68a3-243">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="a68a3-244">4.0.4-preview nuget’e yükselterek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-244">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="a68a3-245">https://github.com/Azure/azure-powershell/issues/6853 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-245">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="a68a3-246">Odata filtresi Ürün üzerinde Ada Göre Arama için düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-246">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="a68a3-247">https://github.com/Azure/azure-powershell/issues/6814 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-247">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="a68a3-248">Odata filtresi API üzerinde Ada Göre Arama için düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-248">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="a68a3-249">Azure İzleyici günlükçüsüne yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-249">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="a68a3-250">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a68a3-250">AzureRM.Compute</span></span>
* <span data-ttu-id="a68a3-251">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-251">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="a68a3-252">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-252">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="a68a3-253">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-253">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="a68a3-254">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-254">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a68a3-255">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a68a3-255">AzureRM.Network</span></span>
* <span data-ttu-id="a68a3-256">Varsayılan cmdlet çıkış gösterimi, tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-256">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a68a3-257">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a68a3-257">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a68a3-258">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-258">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="a68a3-259">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a68a3-259">AzureRM.Resources</span></span>
* <span data-ttu-id="a68a3-260">Market’ten yönetilen uygulama oluşturmayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-260">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a68a3-261">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a68a3-261">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a68a3-262">Düzeltilen sorunlar</span><span class="sxs-lookup"><span data-stu-id="a68a3-262">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a68a3-263">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a68a3-263">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a68a3-264">Çoklu değer yönlendirme yöntemi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-264">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="a68a3-265">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="a68a3-265">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="a68a3-266">Alt ağ yönlendirme yöntemi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-266">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="a68a3-267">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="a68a3-267">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="a68a3-268">Profillerde Özel Üst Bilgi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-268">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="a68a3-269">Profillerde Beklenen durum kodu aralığı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-269">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="a68a3-270">Uç noktalarda Özel Üst Bilgi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-270">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="a68a3-271">6.8.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="a68a3-271">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a68a3-272">Genel</span><span class="sxs-lookup"><span data-stu-id="a68a3-272">General</span></span>
* <span data-ttu-id="a68a3-273">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-273">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a68a3-274">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a68a3-274">AzureRM.Profile</span></span>
* <span data-ttu-id="a68a3-275">Connect-AzureRmAccount sırasında döndürülen belirteçlere sona erme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-275">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a68a3-276">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a68a3-276">AzureRM.Compute</span></span>
* <span data-ttu-id="a68a3-277">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-277">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="a68a3-278">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-278">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="a68a3-279">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-279">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a68a3-280">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a68a3-280">AzureRM.IotHub</span></span>
* <span data-ttu-id="a68a3-281">New-AzureRmIotHubExportDevices ve New-AzureRmIotHubImportDevices için düzeltme örnekleri</span><span class="sxs-lookup"><span data-stu-id="a68a3-281">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a68a3-282">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a68a3-282">AzureRM.Network</span></span>
* <span data-ttu-id="a68a3-283">Varsayılan model gösterimi tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-283">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a68a3-284">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a68a3-284">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a68a3-285">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-285">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a68a3-286">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a68a3-286">AzureRM.Resources</span></span>
* <span data-ttu-id="a68a3-287">Marketten yönetilen uygulamayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-287">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a68a3-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a68a3-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a68a3-289">Sorunlar için düzeltme</span><span class="sxs-lookup"><span data-stu-id="a68a3-289">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a68a3-290">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a68a3-290">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a68a3-291">Çoklu değer yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="a68a3-291">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="a68a3-292">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="a68a3-292">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="a68a3-293">Alt ağ yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="a68a3-293">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="a68a3-294">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="a68a3-294">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="a68a3-295">Profillerde Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="a68a3-295">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="a68a3-296">Profillerde Beklenen durum kodu aralığı desteği</span><span class="sxs-lookup"><span data-stu-id="a68a3-296">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="a68a3-297">Uç noktalarda Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="a68a3-297">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a68a3-298">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a68a3-298">AzureRM.Websites</span></span>
* <span data-ttu-id="a68a3-299">Varsayılan kaynak gruplarının yanlış ayarlanmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-299">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="a68a3-300">6.7.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="a68a3-300">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a68a3-301">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a68a3-301">AzureRM.Profile</span></span>
* <span data-ttu-id="a68a3-302">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-302">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a68a3-303">Bağlam çakışmasını önlemek için varsayılan bağlam adına kullanıcı kimliği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-303">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="a68a3-304">Bağlam #6398 seçerken sorunlara neden olan Clear-AzureRmContext ile ilgili sorunlar giderildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-304">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="a68a3-305">'Connect-AzureRmAccount' için kiracı etki alanının '-TenantId' parametresine geçirilmesi etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-305">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="a68a3-306">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="a68a3-306">Azure.Storage</span></span>
* <span data-ttu-id="a68a3-307">Azure Dosya Paylaşımı kotasındaki 5 TB'lık sınır kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="a68a3-307">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="a68a3-308">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="a68a3-308">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a68a3-309">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a68a3-309">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a68a3-310">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="a68a3-311">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a68a3-311">Azure.AnalysisServices</span></span>
* <span data-ttu-id="a68a3-312">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a68a3-313">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a68a3-313">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a68a3-314">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="a68a3-315">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a68a3-315">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="a68a3-316">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-316">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a68a3-317">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a68a3-317">AzureRM.Automation</span></span>
* <span data-ttu-id="a68a3-318">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-318">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="a68a3-319">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="a68a3-319">AzureRM.Backup</span></span>
* <span data-ttu-id="a68a3-320">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-320">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a68a3-321">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a68a3-321">AzureRM.Batch</span></span>
* <span data-ttu-id="a68a3-322">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-322">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="a68a3-323">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="a68a3-323">AzureRM.Billing</span></span>
* <span data-ttu-id="a68a3-324">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-324">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="a68a3-325">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="a68a3-325">AzureRM.Cdn</span></span>
* <span data-ttu-id="a68a3-326">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-326">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="a68a3-327">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a68a3-327">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="a68a3-328">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-328">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a68a3-329">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a68a3-329">AzureRM.Compute</span></span>
* <span data-ttu-id="a68a3-330">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-330">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a68a3-331">New-AzureRmVmssConfig’e EvictionPolicy parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-331">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="a68a3-332">Hiçbir konum belirtilmediyse New-AzureRmVm’nin DiskFileParameterSet parametresinde varsayılan konum kullanılıyor.</span><span class="sxs-lookup"><span data-stu-id="a68a3-332">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="a68a3-333">Save-AzureRmVMImage cmdlet'inde parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-333">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a68a3-334">Singlepass ile ilgili bazı senaryolarda Get-AzureRmVMDiskEncryptionStatus cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-334">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a68a3-335">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a68a3-335">AzureRM.Consumption</span></span>
* <span data-ttu-id="a68a3-336">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-336">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="a68a3-337">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a68a3-337">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="a68a3-338">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-338">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="a68a3-339">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a68a3-339">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="a68a3-340">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-340">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="a68a3-341">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="a68a3-341">AzureRM.DataFactories</span></span>
* <span data-ttu-id="a68a3-342">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-342">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a68a3-343">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a68a3-343">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a68a3-344">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-344">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a68a3-345">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a68a3-345">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a68a3-346">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-346">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a68a3-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a68a3-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a68a3-348">DebugPreference Powershell komut satırından ayarlandığında hata ayıklama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-348">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="a68a3-349">Set-AzureRmDataLakeStoreItemAcl örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-349">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a68a3-350">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-350">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a68a3-351">Set-AzureRmDataLakeStoreItemAclEntry örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-351">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="a68a3-352">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="a68a3-352">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="a68a3-353">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="a68a3-354">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a68a3-354">AzureRM.Dns</span></span>
* <span data-ttu-id="a68a3-355">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a68a3-356">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a68a3-356">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a68a3-357">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a68a3-358">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a68a3-358">AzureRM.EventHub</span></span>
* <span data-ttu-id="a68a3-359">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="a68a3-360">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a68a3-360">AzureRM.HDInsight</span></span>
* <span data-ttu-id="a68a3-361">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a68a3-362">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a68a3-362">AzureRM.Insights</span></span>
* <span data-ttu-id="a68a3-363">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a68a3-364">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a68a3-364">AzureRM.IotHub</span></span>
* <span data-ttu-id="a68a3-365">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a68a3-366">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a68a3-366">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a68a3-367">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a68a3-368">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a68a3-368">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a68a3-369">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-369">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="a68a3-370">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a68a3-370">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="a68a3-371">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-371">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="a68a3-372">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a68a3-372">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="a68a3-373">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-373">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="a68a3-374">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a68a3-374">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="a68a3-375">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="a68a3-376">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="a68a3-376">AzureRM.Media</span></span>
* <span data-ttu-id="a68a3-377">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a68a3-378">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a68a3-378">AzureRM.Network</span></span>
* <span data-ttu-id="a68a3-379">Set-AzureRmLocalNetworkGateway örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-379">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="a68a3-380">Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey ve New-AzureRmVirtualNetworkGatewayConnection için örnek ve açıklamalar eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-380">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a68a3-381">Remove-AzureRmVirtualNetworkGatewayIpConfig ve Reset-AzureRmVirtualNetworkGateway örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-381">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="a68a3-382">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-382">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a68a3-383">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-383">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a68a3-384">Set-AzureRmVirtualNetworkGatewayConnection örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-384">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a68a3-385">ApplicationSecurityGroup, RouteTable ve Usage için en son kod oluşturucu kullanılarak cmdlet’ler yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="a68a3-385">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="a68a3-386">Varolmayan bir alt ağ alma girişiminde bulunulduğunda Get-AzureRmVirtualNetworkSubnetConfig cmdlet'inin hata iletisi netleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-386">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="a68a3-387">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a68a3-387">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="a68a3-388">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="a68a3-389">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a68a3-389">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a68a3-390">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-390">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a68a3-391">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a68a3-391">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a68a3-392">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a68a3-393">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a68a3-393">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a68a3-394">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="a68a3-395">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a68a3-395">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="a68a3-396">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a68a3-397">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a68a3-397">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a68a3-398">Get-AzureRmRecoveryServicesBackItem cmdlet’ine ilke filtresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-398">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="a68a3-399">Komut, verilen ilke kimliği tarafından korunan yedekleme öğelerinin listesini döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="a68a3-399">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="a68a3-400">Microsoft.Azure.Management.RecoveryServices.Backup, sürüm 3.0.0 önizlemesine güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-400">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="a68a3-401">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-401">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a68a3-402">Restore-AzureRmRecoveryServicesBackupItem’e TargetResourceGroupName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-402">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="a68a3-403">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="a68a3-403">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="a68a3-404">Yönetilen disklerle yapılan VM yedeklemesi için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="a68a3-404">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a68a3-405">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a68a3-405">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a68a3-406">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a68a3-407">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a68a3-407">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a68a3-408">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a68a3-409">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a68a3-409">AzureRM.Relay</span></span>
* <span data-ttu-id="a68a3-410">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a68a3-411">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a68a3-411">AzureRM.Resources</span></span>
* <span data-ttu-id="a68a3-412">Abonelik kapsamındaki şablon dağıtımı destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="a68a3-412">Support template deployment at subscription scope.</span></span> <span data-ttu-id="a68a3-413">Yeni Cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="a68a3-413">Add new Cmdlets:</span></span>
    - <span data-ttu-id="a68a3-414">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a68a3-414">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="a68a3-415">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a68a3-415">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="a68a3-416">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a68a3-416">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="a68a3-417">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a68a3-417">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="a68a3-418">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a68a3-418">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="a68a3-419">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a68a3-419">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="a68a3-420">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a68a3-420">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="a68a3-421">Set-AzureRmResource’a bağlam geçirilirken hata oluşmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-421">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="a68a3-422">New-AzureRmResourceGroupDeployment cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-422">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="a68a3-423">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a68a3-424">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a68a3-424">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a68a3-425">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a68a3-426">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a68a3-426">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a68a3-427">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a68a3-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a68a3-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a68a3-429">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a68a3-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a68a3-430">AzureRM.Sql</span></span>
* <span data-ttu-id="a68a3-431">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a68a3-432">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a68a3-432">AzureRM.Storage</span></span>
* <span data-ttu-id="a68a3-433">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="a68a3-434">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="a68a3-434">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="a68a3-435">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a68a3-436">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a68a3-436">AzureRM.Tags</span></span>
* <span data-ttu-id="a68a3-437">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a68a3-438">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a68a3-438">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a68a3-439">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-439">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="a68a3-440">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="a68a3-440">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="a68a3-441">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-441">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a68a3-442">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a68a3-442">AzureRM.Websites</span></span>
* <span data-ttu-id="a68a3-443">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-443">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="a68a3-444">6.6.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="a68a3-444">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a68a3-445">Genel</span><span class="sxs-lookup"><span data-stu-id="a68a3-445">General</span></span>
* <span data-ttu-id="a68a3-446">Tüm yardım dosyaları tam parametre türleriyle doğru giriş/çıkış türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-446">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a68a3-447">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a68a3-447">AzureRM.Profile</span></span>
* <span data-ttu-id="a68a3-448">Kaynağın geçerli yapılandırmasının hedef kaynakla uyumlu olduğunu doğrulayabilmek için Common.Strategy kitaplığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-448">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="a68a3-449">Common.Storage'a ps1xml türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-449">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a68a3-450">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="a68a3-450">Azure.Storage</span></span>
* <span data-ttu-id="a68a3-451">DefaultProfile’dan Depolama Bağlamı almak için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-451">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="a68a3-452">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-452">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a68a3-453">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a68a3-453">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a68a3-454">https://github.com/Azure/azure-powershell/issues/6370 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-454">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="a68a3-455">PsApiManagementApi'yi ApiContract'e çevirmek için Automapper hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-455">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="a68a3-456">https://github.com/Azure/azure-powershell/issues/6515 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-456">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="a68a3-457">Kodlama Türü ile aşırı yüklemeyi önlemek için File.Save hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-457">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="a68a3-458">https://github.com/Azure/azure-powershell/issues/6560 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-458">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="a68a3-459">apiId üzerindeki desen özel durumunu düzelten 4.0.3 Nuget sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-459">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a68a3-460">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a68a3-460">AzureRM.Compute</span></span>
* <span data-ttu-id="a68a3-461">PremiumLRS depolama hesap türü yeniden adlandırması nedeniyle New-AzureRmVm'de DiskFileParameterSet kullanılarak sanal makine oluşturmanın başarısız olmasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-461">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="a68a3-462">Invoke-AzureRmVMRunCommand cmdlet'i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-462">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="a68a3-463">Abonelikteki tüm kullanılabilir kümelerin listelenebilmesi için Get-AzureRmAvailabilitySet güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-463">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="a68a3-464">(ResouceGroupName parametresi artık isteğe bağlı.)</span><span class="sxs-lookup"><span data-stu-id="a68a3-464">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="a68a3-465">Uygun sanal makinelerde Hızlandırılmış Ağı etkinleştirmek için 'New-AzureRmVm' cmdlet'inin SimpleParameterSet öğesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-465">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="a68a3-466">Kullanıcının belirttiği LB zaten mevcut olduğunda vmss oluşturmanın başarısız olması için New-AzureRmVmss basit parametre kümesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-466">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="a68a3-467">New-AzureRmDisk örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-467">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="a68a3-468">'New-AzureRmVM' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-468">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="a68a3-469">Set-AzureRmVMOSDisk açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-469">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="a68a3-470">Yazımı ve ön eki düzeltmek amacıyla Set-AzureRmVMBginfoExtension için Örnek 1 güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-470">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a68a3-471">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a68a3-471">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a68a3-472">ADF .Net SDK sürümü 1.1.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-472">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="a68a3-473">Veri fabrikaları arasında paylaşılan şirket içinde barındırılan tümleştirme çalışma zamanı desteği.</span><span class="sxs-lookup"><span data-stu-id="a68a3-473">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="a68a3-474">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine yeni -SharedIntegrationRuntimeResourceId parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-474">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="a68a3-475">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine isteğe bağlı yeni -LinkedDataFactoryName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-475">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a68a3-476">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a68a3-476">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a68a3-477">DataPlane SDK'sı (Microsoft.Azure.DataLake.Store) sürümü 1.1.9'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-477">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a68a3-478">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a68a3-478">AzureRM.EventHub</span></span>
* <span data-ttu-id="a68a3-479">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-479">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a68a3-480">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a68a3-480">AzureRM.Insights</span></span>
* <span data-ttu-id="a68a3-481">Yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-481">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="a68a3-482">Microsoft.Azure.Management.Monitor SDK 0.19.1-preview kullanımı</span><span class="sxs-lookup"><span data-stu-id="a68a3-482">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a68a3-483">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a68a3-483">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a68a3-484">Set-AzureRmKeyVaultAccessPolicy'de yönlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-484">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a68a3-485">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a68a3-485">AzureRM.Network</span></span>
* <span data-ttu-id="a68a3-486">LoadBalancerInboundNatPoolConfig cmdlet'leri için örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-486">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a68a3-487">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a68a3-487">AzureRM.Resources</span></span>
* <span data-ttu-id="a68a3-488">'Get-AzureRmResource' için hem etiket adı hem de değer sağlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-488">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="a68a3-489">'Set-AzureRmResource' için yönlendirme senaryosu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-489">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a68a3-490">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a68a3-490">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a68a3-491">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-491">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="a68a3-492">birkaç sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-492">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="a68a3-493">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a68a3-493">AzureRM.Sql</span></span>
* <span data-ttu-id="a68a3-494">Aşağıdaki cmdlet'lere Sunucu Gelişmiş Tehdit Koruması desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="a68a3-494">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="a68a3-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a68a3-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a68a3-496">Aşağıdaki cmdlet'lere Güvenlik Açığı Değerlendirme desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="a68a3-496">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="a68a3-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="a68a3-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="a68a3-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="a68a3-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="a68a3-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="a68a3-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="a68a3-500">Remove-AzureRmSqlServerFirewallRulecmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-500">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="a68a3-501">Get-AzureSqlSyncGroupLog içinde ABD temelli olmayan kültürde yanlış tarih saat işlemesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-501">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a68a3-502">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a68a3-502">AzureRM.Storage</span></span>
* <span data-ttu-id="a68a3-503">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-503">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="a68a3-504">Tablo görünümünde StorageAccount cmdlet'i çıkışı gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="a68a3-504">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="a68a3-505">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a68a3-505">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a68a3-506">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a68a3-506">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a68a3-507">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a68a3-507">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a68a3-508">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a68a3-508">AzureRM.Tags</span></span>
* <span data-ttu-id="a68a3-509">Tag cmdlet'inin yardımında hatayı deyim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="a68a3-509">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="a68a3-510">6.5.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="a68a3-510">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a68a3-511">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a68a3-511">AzureRM.Profile</span></span>
* <span data-ttu-id="a68a3-512">'Get-AzureRmContextAutosaveSetting' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-512">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a68a3-513">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="a68a3-513">Azure.Storage</span></span>
* <span data-ttu-id="a68a3-514">Salt yazılır Sas belirteciyle Karşıya Yükleme Blobu veya Dosyası desteği</span><span class="sxs-lookup"><span data-stu-id="a68a3-514">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="a68a3-515">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a68a3-515">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="a68a3-516">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a68a3-516">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a68a3-517">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a68a3-517">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a68a3-518">AS'ye gerekli ResourceGroupName özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-518">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a68a3-519">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a68a3-519">AzureRM.Automation</span></span>
* <span data-ttu-id="a68a3-520">'New-AzureRMAutomationSchedule' için yardım güncelleştirildi ve örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-520">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a68a3-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a68a3-521">AzureRM.Compute</span></span>
* <span data-ttu-id="a68a3-522">Update/New-AzureRmAvailabilitySet komutlarına -Tag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-522">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="a68a3-523">'Add-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-523">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a68a3-524">'Remove-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-524">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a68a3-525">'Set-AzureRmVMAccessExtension' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-525">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="a68a3-526">New-AzureRmVmss için SimpleParameterSet güncelleştirilerek SinglePlacementGroup varsayılan olarak false değerine ayarlandı ve kullanıcının tek yerleşim grubunda VMSS oluşturmasına olanak tanıyan 'SinglePlacementGroup' geçiş parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-526">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a68a3-527">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a68a3-527">AzureRM.EventHub</span></span>
* <span data-ttu-id="a68a3-528">PSEventHubDRConfigurationAttributes sınıfına, çoğaltma işlemi devam ederken bekleyen çoğaltma işlemlerinin sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-528">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a68a3-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a68a3-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a68a3-530">Set-AzureRmKeyVaultAccessPolicy için hata iletisi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-530">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a68a3-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a68a3-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a68a3-532">New-AzureRmLogicApp’te "parametre kümesi çözümlenemedi" hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-532">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a68a3-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a68a3-533">AzureRM.Network</span></span>
* <span data-ttu-id="a68a3-534">Set/Add-AzureRmVirtualNetworkPeering için birden çok Kiracıdaki Sanal Makineler arasında eşleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-534">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="a68a3-535">Aşağıdaki cmdlet’ler Application Gateway için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-535">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="a68a3-536">New-AzureRmApplicationGateway : EnableFIPS bayrağı ve Zones desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-536">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="a68a3-537">New-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-537">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="a68a3-538">Set-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-538">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="a68a3-539">RouteTable cmdlet’leri en son oluşturucu sürümüyle yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="a68a3-539">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a68a3-540">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a68a3-540">AzureRM.Relay</span></span>
* <span data-ttu-id="a68a3-541">Markdown dosyaları güncelleştirildi, örnekteki parametre adı sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="a68a3-541">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a68a3-542">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a68a3-542">AzureRM.Resources</span></span>
* <span data-ttu-id="a68a3-543">Roleassignment ve roledefinition cmdlet’leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="a68a3-543">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="a68a3-544">Disk belleğinin parçası olarak yapılan ek roledefinition çağrıları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="a68a3-544">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="a68a3-545">Get-AzureRmRoleAssignment cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-545">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="a68a3-546">-ExpandPrincipalGroups komut parametresi işlevselliği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-546">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="a68a3-547">'-ResourceType' parametresinin büyük/küçük harfe duyarlı olduğu 'Get-AzureRmResource' sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-547">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a68a3-548">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a68a3-548">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a68a3-549">Liste cmdlet’lerine top ve skip parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-549">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="a68a3-550">Standard'dan Premium NameSpace'e geçiş cmdlet’leri eklendi :</span><span class="sxs-lookup"><span data-stu-id="a68a3-550">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="a68a3-551">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a68a3-551">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a68a3-552">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a68a3-552">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a68a3-553">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a68a3-553">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a68a3-554">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a68a3-554">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a68a3-555">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a68a3-555">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="a68a3-556">PSServiceBusDRConfigurationAttributes sınıfına, çoğaltma işlemi sürerken beklemede olan çoğaltma işlemi sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-556">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a68a3-557">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a68a3-557">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a68a3-558">'New-AzureRmServiceFabricCluster' için örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-558">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a68a3-559">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a68a3-559">AzureRM.Sql</span></span>
* <span data-ttu-id="a68a3-560">Müşterilerin Sql Server örneğine veya Yönetilen Örneğe TDE Sertifikası ekleyebilmeleri için yeni Management.Sql Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-560">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="a68a3-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a68a3-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="a68a3-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a68a3-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a68a3-563">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a68a3-563">AzureRM.Websites</span></span>
* <span data-ttu-id="a68a3-564">Artık `Set-AzureRmWebApp -AssignIdentity` ve `Set-AzureRmWebAppSlot -AssignIdentity` false olarak ayarlandığında site object.Removing önizleme etiketinden Identity özelliğini kaldırıyor.</span><span class="sxs-lookup"><span data-stu-id="a68a3-564">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="a68a3-565">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-565">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="a68a3-566">`Set-AzureRmWebApp -PhpVersion` geçerli bir php sürümü off değerini destekliyor</span><span class="sxs-lookup"><span data-stu-id="a68a3-566">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="a68a3-567">6.4.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="a68a3-567">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a68a3-568">Genel</span><span class="sxs-lookup"><span data-stu-id="a68a3-568">General</span></span>
* <span data-ttu-id="a68a3-569">Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-569">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a68a3-570">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a68a3-570">AzureRM.Profile</span></span>
* <span data-ttu-id="a68a3-571">Temel çıkış türlerine Ps1Xml özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-571">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a68a3-572">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a68a3-572">AzureRM.Compute</span></span>
* <span data-ttu-id="a68a3-573">VMSS için IP Etiketi özelliği</span><span class="sxs-lookup"><span data-stu-id="a68a3-573">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="a68a3-574">'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-574">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="a68a3-575">New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-575">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a68a3-576">VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-576">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="a68a3-577">New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-577">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="a68a3-578">VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği</span><span class="sxs-lookup"><span data-stu-id="a68a3-578">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="a68a3-579">Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-579">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a68a3-580">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a68a3-580">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a68a3-581">Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:</span><span class="sxs-lookup"><span data-stu-id="a68a3-581">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="a68a3-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a68a3-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a68a3-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a68a3-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a68a3-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a68a3-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a68a3-585">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a68a3-585">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a68a3-586">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-586">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a68a3-587">Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-587">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a68a3-588">Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-588">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="a68a3-589">DataLake cmdlet'lerinin test konumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-589">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a68a3-590">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a68a3-590">AzureRM.EventHub</span></span>
* <span data-ttu-id="a68a3-591">Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-591">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="a68a3-592">New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-592">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="a68a3-593">Varsayılan Parametre kümesi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="a68a3-593">Provided Default Parameter set.</span></span>
* <span data-ttu-id="a68a3-594">Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-594">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a68a3-595">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a68a3-595">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a68a3-596">Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-596">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a68a3-597">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a68a3-597">AzureRM.Network</span></span>
* <span data-ttu-id="a68a3-598">Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="a68a3-598">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="a68a3-599">ARM aracılığıyla ExpressRoute Partner API'leri özelliği için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-599">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="a68a3-600">Get-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-600">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a68a3-601">Set-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-601">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a68a3-602">Add-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-602">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a68a3-603">Get-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-603">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a68a3-604">Remove-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-604">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a68a3-605">Get-AzureRMExpressRouteCrossConnectionArpTable eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-605">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a68a3-606">Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-606">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a68a3-607">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-607">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a68a3-608">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a68a3-608">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a68a3-609">Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-609">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="a68a3-610">Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="a68a3-610">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="a68a3-611">Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a68a3-611">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a68a3-612">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a68a3-612">AzureRM.Resources</span></span>
* <span data-ttu-id="a68a3-613">Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="a68a3-613">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="a68a3-614">Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-614">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="a68a3-615">Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-615">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="a68a3-616">control parametresine -Effective ve -All anahtarları eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-616">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="a68a3-617">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-617">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="a68a3-618">Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-618">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a68a3-619">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-619">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a68a3-620">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-620">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="a68a3-621">Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-621">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a68a3-622">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-622">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a68a3-623">'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-623">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="a68a3-624">'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-624">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="a68a3-625">'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-625">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="a68a3-626">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a68a3-626">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a68a3-627">Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-627">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a68a3-628">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a68a3-628">AzureRM.Sql</span></span>
* <span data-ttu-id="a68a3-629">New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-629">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="a68a3-630">Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-630">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="a68a3-631">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="a68a3-631">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a68a3-632">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a68a3-632">AzureRM.Profile</span></span>
* <span data-ttu-id="a68a3-633">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-633">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="a68a3-634">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="a68a3-634">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a68a3-635">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="a68a3-635">Azure.Storage</span></span>
* <span data-ttu-id="a68a3-636">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-636">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a68a3-637">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a68a3-637">AzureRM.Compute</span></span>
* <span data-ttu-id="a68a3-638">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-638">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="a68a3-639">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-639">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="a68a3-640">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a68a3-640">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a68a3-641">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a68a3-641">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a68a3-642">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a68a3-642">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a68a3-643">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="a68a3-643">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="a68a3-644">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a68a3-644">Start-AzureRmVM</span></span>
    - <span data-ttu-id="a68a3-645">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a68a3-645">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="a68a3-646">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a68a3-646">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="a68a3-647">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a68a3-647">Set-AzureRmVM</span></span>
    - <span data-ttu-id="a68a3-648">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a68a3-648">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="a68a3-649">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a68a3-649">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="a68a3-650">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a68a3-650">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="a68a3-651">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a68a3-651">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="a68a3-652">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a68a3-652">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="a68a3-653">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a68a3-653">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="a68a3-654">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a68a3-654">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="a68a3-655">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a68a3-655">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="a68a3-656">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a68a3-656">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="a68a3-657">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a68a3-657">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a68a3-658">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="a68a3-658">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="a68a3-659">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a68a3-659">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a68a3-660">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="a68a3-660">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="a68a3-661">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a68a3-661">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="a68a3-662">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a68a3-662">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a68a3-663">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a68a3-663">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a68a3-664">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="a68a3-664">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a68a3-665">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a68a3-665">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a68a3-666">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-666">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a68a3-667">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a68a3-667">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a68a3-668">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="a68a3-668">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="a68a3-669">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="a68a3-669">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="a68a3-670">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-670">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a68a3-671">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a68a3-671">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a68a3-672">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-672">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="a68a3-673">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="a68a3-673">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a68a3-674">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a68a3-674">AzureRM.Sql</span></span>
* <span data-ttu-id="a68a3-675">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-675">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a68a3-676">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a68a3-676">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a68a3-677">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-677">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a68a3-678">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a68a3-678">AzureRM.Websites</span></span>
* <span data-ttu-id="a68a3-679">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-679">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="a68a3-680">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-680">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="a68a3-681">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="a68a3-681">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="a68a3-682">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a68a3-682">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a68a3-683">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-683">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="a68a3-684">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="a68a3-684">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a68a3-685">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a68a3-685">AzureRM.Profile</span></span>
* <span data-ttu-id="a68a3-686">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-686">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a68a3-687">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a68a3-687">AzureRM.Compute</span></span>
* <span data-ttu-id="a68a3-688">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="a68a3-688">VMSS VM Update feature</span></span>
    - <span data-ttu-id="a68a3-689">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-689">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="a68a3-690">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-690">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a68a3-691">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a68a3-691">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a68a3-692">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="a68a3-692">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="a68a3-693">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-693">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="a68a3-694">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-694">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="a68a3-695">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-695">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="a68a3-696">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-696">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="a68a3-697">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a68a3-697">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a68a3-698">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-698">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="a68a3-699">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a68a3-699">AzureRM.Network</span></span>
* <span data-ttu-id="a68a3-700">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-700">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a68a3-701">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a68a3-701">AzureRM.Resources</span></span>
* <span data-ttu-id="a68a3-702">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-702">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a68a3-703">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a68a3-703">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a68a3-704">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-704">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="a68a3-705">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a68a3-705">AzureRM.Sql</span></span>
* <span data-ttu-id="a68a3-706">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="a68a3-706">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="a68a3-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a68a3-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a68a3-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a68a3-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a68a3-709">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a68a3-709">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a68a3-710">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a68a3-710">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a68a3-711">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a68a3-711">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a68a3-712">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a68a3-712">AzureRM.Websites</span></span>
* <span data-ttu-id="a68a3-713">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-713">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="a68a3-714">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="a68a3-714">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a68a3-715">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a68a3-715">AzureRM.Profile</span></span>
* <span data-ttu-id="a68a3-716">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-716">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a68a3-717">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a68a3-717">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a68a3-718">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="a68a3-718">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a68a3-719">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a68a3-719">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a68a3-720">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-720">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="a68a3-721">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-721">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="a68a3-722">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-722">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="a68a3-723">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-723">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="a68a3-724">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-724">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="a68a3-725">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-725">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="a68a3-726">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-726">Added support for MSI identity</span></span>
* <span data-ttu-id="a68a3-727">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="a68a3-727">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="a68a3-728">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a68a3-728">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="a68a3-729">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a68a3-729">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="a68a3-730">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a68a3-730">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="a68a3-731">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a68a3-731">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a68a3-732">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a68a3-732">AzureRM.Batch</span></span>
* <span data-ttu-id="a68a3-733">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="a68a3-733">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="a68a3-734">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="a68a3-734">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a68a3-735">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a68a3-735">AzureRM.Consumption</span></span>
* <span data-ttu-id="a68a3-736">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="a68a3-736">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a68a3-737">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a68a3-737">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a68a3-738">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="a68a3-738">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a68a3-739">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="a68a3-739">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="a68a3-740">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="a68a3-740">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="a68a3-741">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a68a3-741">AzureRM.Network</span></span>
* <span data-ttu-id="a68a3-742">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="a68a3-742">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="a68a3-743">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-743">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="a68a3-744">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a68a3-744">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="a68a3-745">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-745">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="a68a3-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a68a3-747">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-747">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="a68a3-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a68a3-749">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="a68a3-749">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="a68a3-750">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a68a3-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a68a3-751">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a68a3-751">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a68a3-752">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="a68a3-752">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a68a3-753">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a68a3-753">AzureRM.Sql</span></span>
* <span data-ttu-id="a68a3-754">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a68a3-754">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="a68a3-755">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a68a3-755">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="a68a3-756">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a68a3-756">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="a68a3-757">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a68a3-757">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="a68a3-758">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="a68a3-758">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="a68a3-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a68a3-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a68a3-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a68a3-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a68a3-761">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a68a3-761">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a68a3-762">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a68a3-762">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a68a3-763">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a68a3-763">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a68a3-764">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a68a3-764">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a68a3-765">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a68a3-765">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
