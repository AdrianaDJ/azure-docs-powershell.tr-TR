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
ms.openlocfilehash: 6a33d1a85fc61d0281bf1183163185b0dc4d3a12
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399068"
---
# <a name="release-notes"></a><span data-ttu-id="cecdd-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="cecdd-103">Release notes</span></span>

<span data-ttu-id="cecdd-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="cecdd-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6100---october-2018"></a><span data-ttu-id="cecdd-105">6.10.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="cecdd-105">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="cecdd-106">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="cecdd-106">Azure.Storage</span></span>
* <span data-ttu-id="cecdd-107">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="cecdd-107">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="cecdd-108">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cecdd-108">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="cecdd-109">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cecdd-109">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="cecdd-110">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cecdd-110">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="cecdd-111">Mevcut hesap olmadan Get-AzureRmCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="cecdd-111">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="cecdd-112">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cecdd-112">AzureRM.Compute</span></span>
* <span data-ttu-id="cecdd-113">Get-AzureRmVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-113">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="cecdd-114">New-AzureRmVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-114">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="cecdd-115">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-115">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="cecdd-116">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cecdd-116">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="cecdd-117">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-117">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="cecdd-118">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cecdd-118">AzureRM.Network</span></span>
* <span data-ttu-id="cecdd-119">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-119">Added NetworkProfile functionality.</span></span> <span data-ttu-id="cecdd-120">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-120">new cmdlets added</span></span>
    - <span data-ttu-id="cecdd-121">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cecdd-121">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="cecdd-122">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cecdd-122">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="cecdd-123">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cecdd-123">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="cecdd-124">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cecdd-124">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="cecdd-125">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-125">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="cecdd-126">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-126">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="cecdd-127">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-127">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="cecdd-128">New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-128">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="cecdd-129">Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-129">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="cecdd-130">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cecdd-130">AzureRM.RedisCache</span></span>
* <span data-ttu-id="cecdd-131">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="cecdd-131">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="cecdd-132">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-132">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="cecdd-133">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cecdd-133">AzureRM.Resources</span></span>
* <span data-ttu-id="cecdd-134">Set-AzureRmPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-134">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="cecdd-135">Origin öğesi User içeren işlemler için Get-AzureRmProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-135">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="cecdd-136">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="cecdd-136">AzureRM.Sql</span></span>
* <span data-ttu-id="cecdd-137">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-137">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="cecdd-138">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="cecdd-138">AzureRM.Storage</span></span>
* <span data-ttu-id="cecdd-139">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="cecdd-139">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="cecdd-140">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cecdd-140">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="cecdd-141">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="cecdd-141">AzureRM.Websites</span></span>
* <span data-ttu-id="cecdd-142">Yeni Get-AzureRMWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="cecdd-142">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="cecdd-143">Yeni New-AzureRMWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="cecdd-143">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="cecdd-144">6.9.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="cecdd-144">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cecdd-145">Genel</span><span class="sxs-lookup"><span data-stu-id="cecdd-145">General</span></span>
* <span data-ttu-id="cecdd-146">AzureRM.SignalR, AzureRM toplu modülüne eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-146">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="cecdd-147">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="cecdd-147">AzureRM.Profile</span></span>
* <span data-ttu-id="cecdd-148">Depolama ortak kodunda küçük değişiklikler yapıldı</span><span class="sxs-lookup"><span data-stu-id="cecdd-148">Minor changes to the storage common code</span></span>
* <span data-ttu-id="cecdd-149">Yardım dosyaları tüm parametre türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-149">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="cecdd-150">ServicePrincipalCertificateWithSubscriptionId parametre kümesindeki -ServicePrincipal parametresi zorunlu olmaktan çıkarıldı</span><span class="sxs-lookup"><span data-stu-id="cecdd-150">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="cecdd-151">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="cecdd-151">Azure.Storage</span></span>
* <span data-ttu-id="cecdd-152">OAuth ile Depolama Bağlamı oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-152">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="cecdd-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="cecdd-153">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="cecdd-154">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="cecdd-154">AzureRM.Cdn</span></span>
* <span data-ttu-id="cecdd-155">CDN fiyatlandırma SKU'suna Standard_Microsoft eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-155">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="cecdd-156">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cecdd-156">AzureRM.Compute</span></span>
* <span data-ttu-id="cecdd-157">Keyvault ve Storage bağımlılıkları ortak bağımlılıklara taşındı</span><span class="sxs-lookup"><span data-stu-id="cecdd-157">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="cecdd-158">AEM cmdlet'lerine daha fazla sanal makine boyutu için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-158">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="cecdd-159">New-AzureRmVmssIpConfig cmdlet'ine Add PublicIPPrefix parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-159">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="cecdd-160">Invoke-AzureRmVMRunCommand cmdlet'ine ResourceId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-160">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="cecdd-161">Invoke-AzureRmVmssVMRunCommand cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-161">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="cecdd-162">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="cecdd-162">AzureRM.Dns</span></span>
* <span data-ttu-id="cecdd-163">DNS kaydı oluşturma işlemi sırasında diğer ad kaydı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-163">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="cecdd-164">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="cecdd-164">AzureRM.Insights</span></span>
* <span data-ttu-id="cecdd-165">6833 ve 7102 numaralı sorunlar giderildi (Tanılama Ayarları bölümü)</span><span class="sxs-lookup"><span data-stu-id="cecdd-165">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="cecdd-166">Tanılama ayarlarını oluşturma ve listeleme/alma sırasında karşılaşılan varsayılan ad 'service' sorunları</span><span class="sxs-lookup"><span data-stu-id="cecdd-166">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="cecdd-167">Kategoriye sahip tanılama ayarı oluşturma sorunları</span><span class="sxs-lookup"><span data-stu-id="cecdd-167">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="cecdd-168">Ölçümler zaman dilimi parametreleri için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-168">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="cecdd-169">Zaman dilimi parametreleri yine kabul ediliyor (bu bir hataya neden olan değişiklik değil) ancak yalnızca PT1M geçerli olduğu için bu parametreler arka uçta yoksayılıyor</span><span class="sxs-lookup"><span data-stu-id="cecdd-169">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="cecdd-170">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cecdd-170">AzureRM.Network</span></span>
* <span data-ttu-id="cecdd-171">LoadBalancer cmdlet'lerinde değişiklikler yapıldı</span><span class="sxs-lookup"><span data-stu-id="cecdd-171">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="cecdd-172">LoadBalancerInboundNatPoolConfig: IdleTimeoutInMinutes, EnableFloatingIp ve EnableTcpReset parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-172">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="cecdd-173">LoadBalancerInboundNatRuleConfig: EnableTcpReset parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-173">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="cecdd-174">LoadBalancerRuleConfig: EnableTcpReset parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-174">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="cecdd-175">LoadBalancerProbeConfig: Protocol parametresi için "Https" değeri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-175">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="cecdd-176">Yeni LoadBalancer alt kaynağı OutboundRule için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-176">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="cecdd-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="cecdd-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="cecdd-179">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-179">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="cecdd-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="cecdd-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="cecdd-182">PSNetworkInterface için yeni HostedWorkloads özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-182">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="cecdd-183">ARM aracılığıyla Azure Güvenlik Duvarı özelliği için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-183">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="cecdd-184">Get-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-184">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="cecdd-185">Set-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-185">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="cecdd-186">New-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-186">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="cecdd-187">Remove-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-187">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="cecdd-188">New-AzureRmFirewallApplicationRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-188">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="cecdd-189">New-AzureRmFirewallApplicationRule eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-189">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="cecdd-190">New-AzureRmFirewallNatRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-190">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="cecdd-191">New-AzureRmFirewallNatRule eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-191">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="cecdd-192">New-AzureRmFirewallNetworkRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-192">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="cecdd-193">New-AzureRmFirewallNetworkRule eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-193">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="cecdd-194">Application Gateway'de Güvenilen Kök sertifika ve Otomatik ölçeklendirme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-194">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="cecdd-195">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="cecdd-195">New Cmdlets added:</span></span>
      - <span data-ttu-id="cecdd-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cecdd-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="cecdd-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cecdd-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="cecdd-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cecdd-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="cecdd-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cecdd-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="cecdd-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cecdd-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="cecdd-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cecdd-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="cecdd-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cecdd-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="cecdd-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cecdd-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="cecdd-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cecdd-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="cecdd-205">Cmdlet'ler isteğe bağlı -TrustedRootCertificate parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-205">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="cecdd-206">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cecdd-206">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="cecdd-207">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cecdd-207">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="cecdd-208">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="cecdd-208">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="cecdd-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="cecdd-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="cecdd-210">Cmdlet'ler isteğe bağlı -AutoscaleConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-210">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="cecdd-211">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cecdd-211">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="cecdd-212">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cecdd-212">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="cecdd-213">Arabirim Uç Noktası için Get-AzureInterfaceEndpoint cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-213">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="cecdd-214">Bir alt ağda birden fazla adres ön eki için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-214">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="cecdd-215">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="cecdd-215">Updated cmdlets:</span></span>
  - <span data-ttu-id="cecdd-216">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-216">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="cecdd-217">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-217">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="cecdd-218">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-218">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="cecdd-219">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-219">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="cecdd-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cecdd-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="cecdd-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="cecdd-222">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-222">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="cecdd-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="cecdd-224">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cecdd-224">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="cecdd-225">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cecdd-225">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="cecdd-226">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cecdd-226">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="cecdd-227">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-227">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="cecdd-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="cecdd-229">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-229">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="cecdd-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="cecdd-231">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-231">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="cecdd-232">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-232">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="cecdd-233">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-233">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="cecdd-234">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cecdd-234">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="cecdd-235">Alt ağ temsilcisi seçme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-235">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="cecdd-236">New-AzureRmDelegation: Bir alt ağa eklenebilecek yeni bir temsilci oluşturur</span><span class="sxs-lookup"><span data-stu-id="cecdd-236">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="cecdd-237">Remove-AzureRmDelegation: Bir alt ağı alır ve belirtilen temsilci adını o alt ağdan kaldırır</span><span class="sxs-lookup"><span data-stu-id="cecdd-237">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="cecdd-238">Add-AzureRmDelegation: Bir alt ağı alır ve belirtilen hizmet adını o alt ağa temsilci olarak ekler</span><span class="sxs-lookup"><span data-stu-id="cecdd-238">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="cecdd-239">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="cecdd-239">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="cecdd-240">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="cecdd-240">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="cecdd-241">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cecdd-241">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="cecdd-242">Yönetilen disk desteği</span><span class="sxs-lookup"><span data-stu-id="cecdd-242">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="cecdd-243">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cecdd-243">AzureRM.RedisCache</span></span>
* <span data-ttu-id="cecdd-244">Insights bağımlılığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-244">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="cecdd-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cecdd-245">AzureRM.Resources</span></span>
* <span data-ttu-id="cecdd-246">New-AzureRmResourceGroupDeployment cmdlet'i yeni RollbackAction parametresi eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-246">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="cecdd-247">Yeni parametreyle OnErrorDeployment desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-247">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="cecdd-248">İlke atamalarında yönetilen kimlik desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-248">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="cecdd-249">Varsayılan değerlere sahip parametrelerin artık 'New-AzureRmPolicyAssignment' ile ilke atama işlemi sırasında belirtilmesi zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="cecdd-249">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="cecdd-250">İlke diğer adlarını almak için yeni Get-AzureRmPolicyAlias cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-250">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="cecdd-251">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cecdd-251">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="cecdd-252">7161 numaralı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-252">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="cecdd-253">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="cecdd-253">AzureRM.SignalR</span></span>
* <span data-ttu-id="cecdd-254">SKU adları Free_F1 ve Standard_S1 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-254">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="cecdd-255">PSSignalRResource nesnesine sürüm alanı, PSSignalRKeys nesnesine de bağlantı dizesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-255">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="cecdd-256">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="cecdd-256">AzureRM.Storage</span></span>
* <span data-ttu-id="cecdd-257">AzureRm.Storage için Değiştirilemezlik İlkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-257">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="cecdd-258">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cecdd-258">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="cecdd-259">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cecdd-259">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="cecdd-260">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cecdd-260">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="cecdd-261">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cecdd-261">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="cecdd-262">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cecdd-262">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="cecdd-263">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="cecdd-263">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="cecdd-264">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="cecdd-264">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="cecdd-265">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cecdd-265">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="cecdd-266">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cecdd-266">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="cecdd-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cecdd-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="cecdd-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cecdd-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="cecdd-269">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="cecdd-269">AzureRM.Websites</span></span>
* <span data-ttu-id="cecdd-270">İki yeni cmdlet eklendi: Get-AzureRmDeletedWebApp ve Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="cecdd-270">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="cecdd-271">Windows kapsayıcısı ile App Service planı oluşturmak için New-AzureRmAppServicePlan -HyperV anahtarı eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-271">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="cecdd-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Windows kapsayıcı uygulaması oluşturmak ve yönetmek için yeni parametreler (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="cecdd-273">6.8.1 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="cecdd-273">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cecdd-274">Genel</span><span class="sxs-lookup"><span data-stu-id="cecdd-274">General</span></span>
* <span data-ttu-id="cecdd-275">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-275">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="cecdd-276">Ortak çalışma zamanı bütünleştirilmiş kodları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-276">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="cecdd-277">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cecdd-277">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="cecdd-278">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-278">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="cecdd-279">https://github.com/Azure/azure-powershell/issues/6603 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-279">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="cecdd-280">Import-AzureRmApiManagementApi ve \*-AzureRmApiManagementCertificate cmdlet’leri artık göreli yolları işleyebiliyor</span><span class="sxs-lookup"><span data-stu-id="cecdd-280">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="cecdd-281">https://github.com/Azure/azure-powershell/issues/6879 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-281">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="cecdd-282">CertificateInformation, Set-AzureRmApiManagement cmdlet’inin düzgün çalışmasını sağlayan, ayarlanabilir bir özelliktir.</span><span class="sxs-lookup"><span data-stu-id="cecdd-282">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="cecdd-283">4.0.4-preview nuget’e yükselterek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-283">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="cecdd-284">https://github.com/Azure/azure-powershell/issues/6853 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-284">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="cecdd-285">Odata filtresi Ürün üzerinde Ada Göre Arama için düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-285">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="cecdd-286">https://github.com/Azure/azure-powershell/issues/6814 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-286">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="cecdd-287">Odata filtresi API üzerinde Ada Göre Arama için düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-287">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="cecdd-288">Azure İzleyici günlükçüsüne yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-288">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="cecdd-289">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cecdd-289">AzureRM.Compute</span></span>
* <span data-ttu-id="cecdd-290">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-290">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="cecdd-291">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-291">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="cecdd-292">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-292">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="cecdd-293">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-293">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="cecdd-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cecdd-294">AzureRM.Network</span></span>
* <span data-ttu-id="cecdd-295">Varsayılan cmdlet çıkış gösterimi, tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-295">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="cecdd-296">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cecdd-296">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="cecdd-297">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-297">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="cecdd-298">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cecdd-298">AzureRM.Resources</span></span>
* <span data-ttu-id="cecdd-299">Market’ten yönetilen uygulama oluşturmayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-299">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="cecdd-300">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cecdd-300">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="cecdd-301">Düzeltilen sorunlar</span><span class="sxs-lookup"><span data-stu-id="cecdd-301">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="cecdd-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cecdd-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="cecdd-303">Çoklu değer yönlendirme yöntemi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-303">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="cecdd-304">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="cecdd-304">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="cecdd-305">Alt ağ yönlendirme yöntemi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-305">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="cecdd-306">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="cecdd-306">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="cecdd-307">Profillerde Özel Üst Bilgi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-307">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="cecdd-308">Profillerde Beklenen durum kodu aralığı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-308">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="cecdd-309">Uç noktalarda Özel Üst Bilgi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-309">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="cecdd-310">6.8.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="cecdd-310">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cecdd-311">Genel</span><span class="sxs-lookup"><span data-stu-id="cecdd-311">General</span></span>
* <span data-ttu-id="cecdd-312">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-312">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="cecdd-313">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="cecdd-313">AzureRM.Profile</span></span>
* <span data-ttu-id="cecdd-314">Connect-AzureRmAccount sırasında döndürülen belirteçlere sona erme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-314">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="cecdd-315">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cecdd-315">AzureRM.Compute</span></span>
* <span data-ttu-id="cecdd-316">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-316">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="cecdd-317">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-317">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="cecdd-318">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-318">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="cecdd-319">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="cecdd-319">AzureRM.IotHub</span></span>
* <span data-ttu-id="cecdd-320">New-AzureRmIotHubExportDevices ve New-AzureRmIotHubImportDevices için düzeltme örnekleri</span><span class="sxs-lookup"><span data-stu-id="cecdd-320">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="cecdd-321">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cecdd-321">AzureRM.Network</span></span>
* <span data-ttu-id="cecdd-322">Varsayılan model gösterimi tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-322">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="cecdd-323">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cecdd-323">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="cecdd-324">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-324">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="cecdd-325">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cecdd-325">AzureRM.Resources</span></span>
* <span data-ttu-id="cecdd-326">Marketten yönetilen uygulamayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-326">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="cecdd-327">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cecdd-327">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="cecdd-328">Sorunlar için düzeltme</span><span class="sxs-lookup"><span data-stu-id="cecdd-328">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="cecdd-329">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cecdd-329">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="cecdd-330">Çoklu değer yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="cecdd-330">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="cecdd-331">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="cecdd-331">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="cecdd-332">Alt ağ yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="cecdd-332">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="cecdd-333">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="cecdd-333">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="cecdd-334">Profillerde Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="cecdd-334">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="cecdd-335">Profillerde Beklenen durum kodu aralığı desteği</span><span class="sxs-lookup"><span data-stu-id="cecdd-335">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="cecdd-336">Uç noktalarda Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="cecdd-336">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="cecdd-337">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="cecdd-337">AzureRM.Websites</span></span>
* <span data-ttu-id="cecdd-338">Varsayılan kaynak gruplarının yanlış ayarlanmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-338">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="cecdd-339">6.7.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="cecdd-339">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="cecdd-340">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="cecdd-340">AzureRM.Profile</span></span>
* <span data-ttu-id="cecdd-341">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-341">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="cecdd-342">Bağlam çakışmasını önlemek için varsayılan bağlam adına kullanıcı kimliği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-342">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="cecdd-343">Bağlam #6398 seçerken sorunlara neden olan Clear-AzureRmContext ile ilgili sorunlar giderildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-343">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="cecdd-344">'Connect-AzureRmAccount' için kiracı etki alanının '-TenantId' parametresine geçirilmesi etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-344">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="cecdd-345">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="cecdd-345">Azure.Storage</span></span>
* <span data-ttu-id="cecdd-346">Azure Dosya Paylaşımı kotasındaki 5 TB'lık sınır kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="cecdd-346">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="cecdd-347">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="cecdd-347">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="cecdd-348">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cecdd-348">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="cecdd-349">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-349">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="cecdd-350">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cecdd-350">Azure.AnalysisServices</span></span>
* <span data-ttu-id="cecdd-351">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-351">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="cecdd-352">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cecdd-352">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="cecdd-353">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="cecdd-354">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cecdd-354">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="cecdd-355">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="cecdd-356">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="cecdd-356">AzureRM.Automation</span></span>
* <span data-ttu-id="cecdd-357">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="cecdd-358">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="cecdd-358">AzureRM.Backup</span></span>
* <span data-ttu-id="cecdd-359">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="cecdd-360">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="cecdd-360">AzureRM.Batch</span></span>
* <span data-ttu-id="cecdd-361">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="cecdd-362">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="cecdd-362">AzureRM.Billing</span></span>
* <span data-ttu-id="cecdd-363">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="cecdd-364">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="cecdd-364">AzureRM.Cdn</span></span>
* <span data-ttu-id="cecdd-365">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="cecdd-366">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cecdd-366">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="cecdd-367">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="cecdd-368">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cecdd-368">AzureRM.Compute</span></span>
* <span data-ttu-id="cecdd-369">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-369">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="cecdd-370">New-AzureRmVmssConfig’e EvictionPolicy parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-370">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="cecdd-371">Hiçbir konum belirtilmediyse New-AzureRmVm’nin DiskFileParameterSet parametresinde varsayılan konum kullanılıyor.</span><span class="sxs-lookup"><span data-stu-id="cecdd-371">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="cecdd-372">Save-AzureRmVMImage cmdlet'inde parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-372">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="cecdd-373">Singlepass ile ilgili bazı senaryolarda Get-AzureRmVMDiskEncryptionStatus cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-373">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="cecdd-374">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="cecdd-374">AzureRM.Consumption</span></span>
* <span data-ttu-id="cecdd-375">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="cecdd-376">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cecdd-376">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="cecdd-377">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="cecdd-378">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cecdd-378">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="cecdd-379">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-379">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="cecdd-380">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="cecdd-380">AzureRM.DataFactories</span></span>
* <span data-ttu-id="cecdd-381">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-381">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="cecdd-382">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cecdd-382">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="cecdd-383">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-383">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="cecdd-384">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cecdd-384">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="cecdd-385">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-385">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="cecdd-386">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cecdd-386">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="cecdd-387">DebugPreference Powershell komut satırından ayarlandığında hata ayıklama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-387">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="cecdd-388">Set-AzureRmDataLakeStoreItemAcl örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-388">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="cecdd-389">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-389">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="cecdd-390">Set-AzureRmDataLakeStoreItemAclEntry örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-390">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="cecdd-391">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="cecdd-391">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="cecdd-392">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="cecdd-393">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="cecdd-393">AzureRM.Dns</span></span>
* <span data-ttu-id="cecdd-394">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="cecdd-395">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cecdd-395">AzureRM.EventGrid</span></span>
* <span data-ttu-id="cecdd-396">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="cecdd-397">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="cecdd-397">AzureRM.EventHub</span></span>
* <span data-ttu-id="cecdd-398">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="cecdd-399">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cecdd-399">AzureRM.HDInsight</span></span>
* <span data-ttu-id="cecdd-400">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="cecdd-401">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="cecdd-401">AzureRM.Insights</span></span>
* <span data-ttu-id="cecdd-402">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="cecdd-403">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="cecdd-403">AzureRM.IotHub</span></span>
* <span data-ttu-id="cecdd-404">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="cecdd-405">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cecdd-405">AzureRM.KeyVault</span></span>
* <span data-ttu-id="cecdd-406">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="cecdd-407">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cecdd-407">AzureRM.LogicApp</span></span>
* <span data-ttu-id="cecdd-408">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="cecdd-409">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cecdd-409">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="cecdd-410">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="cecdd-411">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="cecdd-411">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="cecdd-412">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-412">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="cecdd-413">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cecdd-413">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="cecdd-414">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-414">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="cecdd-415">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="cecdd-415">AzureRM.Media</span></span>
* <span data-ttu-id="cecdd-416">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-416">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="cecdd-417">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cecdd-417">AzureRM.Network</span></span>
* <span data-ttu-id="cecdd-418">Set-AzureRmLocalNetworkGateway örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-418">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="cecdd-419">Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey ve New-AzureRmVirtualNetworkGatewayConnection için örnek ve açıklamalar eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-419">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="cecdd-420">Remove-AzureRmVirtualNetworkGatewayIpConfig ve Reset-AzureRmVirtualNetworkGateway örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-420">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="cecdd-421">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-421">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="cecdd-422">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-422">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="cecdd-423">Set-AzureRmVirtualNetworkGatewayConnection örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-423">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="cecdd-424">ApplicationSecurityGroup, RouteTable ve Usage için en son kod oluşturucu kullanılarak cmdlet’ler yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="cecdd-424">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="cecdd-425">Varolmayan bir alt ağ alma girişiminde bulunulduğunda Get-AzureRmVirtualNetworkSubnetConfig cmdlet'inin hata iletisi netleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-425">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="cecdd-426">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="cecdd-426">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="cecdd-427">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="cecdd-428">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cecdd-428">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="cecdd-429">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="cecdd-430">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cecdd-430">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="cecdd-431">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="cecdd-432">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cecdd-432">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="cecdd-433">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="cecdd-434">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cecdd-434">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="cecdd-435">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="cecdd-436">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cecdd-436">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cecdd-437">Get-AzureRmRecoveryServicesBackItem cmdlet’ine ilke filtresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-437">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="cecdd-438">Komut, verilen ilke kimliği tarafından korunan yedekleme öğelerinin listesini döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="cecdd-438">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="cecdd-439">Microsoft.Azure.Management.RecoveryServices.Backup, sürüm 3.0.0 önizlemesine güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-439">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="cecdd-440">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-440">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="cecdd-441">Restore-AzureRmRecoveryServicesBackupItem’e TargetResourceGroupName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-441">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="cecdd-442">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="cecdd-442">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="cecdd-443">Yönetilen disklerle yapılan VM yedeklemesi için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="cecdd-443">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="cecdd-444">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cecdd-444">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="cecdd-445">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-445">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="cecdd-446">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cecdd-446">AzureRM.RedisCache</span></span>
* <span data-ttu-id="cecdd-447">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-447">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="cecdd-448">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="cecdd-448">AzureRM.Relay</span></span>
* <span data-ttu-id="cecdd-449">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-449">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="cecdd-450">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cecdd-450">AzureRM.Resources</span></span>
* <span data-ttu-id="cecdd-451">Abonelik kapsamındaki şablon dağıtımı destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="cecdd-451">Support template deployment at subscription scope.</span></span> <span data-ttu-id="cecdd-452">Yeni Cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="cecdd-452">Add new Cmdlets:</span></span>
    - <span data-ttu-id="cecdd-453">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="cecdd-453">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="cecdd-454">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="cecdd-454">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="cecdd-455">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="cecdd-455">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="cecdd-456">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="cecdd-456">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="cecdd-457">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="cecdd-457">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="cecdd-458">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="cecdd-458">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="cecdd-459">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="cecdd-459">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="cecdd-460">Set-AzureRmResource’a bağlam geçirilirken hata oluşmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-460">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="cecdd-461">New-AzureRmResourceGroupDeployment cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-461">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="cecdd-462">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-462">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="cecdd-463">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="cecdd-463">AzureRM.Scheduler</span></span>
* <span data-ttu-id="cecdd-464">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-464">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="cecdd-465">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cecdd-465">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="cecdd-466">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="cecdd-467">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cecdd-467">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="cecdd-468">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="cecdd-469">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="cecdd-469">AzureRM.Sql</span></span>
* <span data-ttu-id="cecdd-470">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="cecdd-471">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="cecdd-471">AzureRM.Storage</span></span>
* <span data-ttu-id="cecdd-472">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-472">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="cecdd-473">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="cecdd-473">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="cecdd-474">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-474">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="cecdd-475">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="cecdd-475">AzureRM.Tags</span></span>
* <span data-ttu-id="cecdd-476">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-476">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="cecdd-477">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cecdd-477">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="cecdd-478">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-478">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="cecdd-479">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="cecdd-479">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="cecdd-480">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-480">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="cecdd-481">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="cecdd-481">AzureRM.Websites</span></span>
* <span data-ttu-id="cecdd-482">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-482">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="cecdd-483">6.6.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="cecdd-483">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cecdd-484">Genel</span><span class="sxs-lookup"><span data-stu-id="cecdd-484">General</span></span>
* <span data-ttu-id="cecdd-485">Tüm yardım dosyaları tam parametre türleriyle doğru giriş/çıkış türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-485">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="cecdd-486">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="cecdd-486">AzureRM.Profile</span></span>
* <span data-ttu-id="cecdd-487">Kaynağın geçerli yapılandırmasının hedef kaynakla uyumlu olduğunu doğrulayabilmek için Common.Strategy kitaplığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-487">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="cecdd-488">Common.Storage'a ps1xml türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-488">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="cecdd-489">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="cecdd-489">Azure.Storage</span></span>
* <span data-ttu-id="cecdd-490">DefaultProfile’dan Depolama Bağlamı almak için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-490">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="cecdd-491">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-491">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="cecdd-492">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cecdd-492">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="cecdd-493">https://github.com/Azure/azure-powershell/issues/6370 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-493">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="cecdd-494">PsApiManagementApi'yi ApiContract'e çevirmek için Automapper hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-494">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="cecdd-495">https://github.com/Azure/azure-powershell/issues/6515 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-495">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="cecdd-496">Kodlama Türü ile aşırı yüklemeyi önlemek için File.Save hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-496">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="cecdd-497">https://github.com/Azure/azure-powershell/issues/6560 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-497">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="cecdd-498">apiId üzerindeki desen özel durumunu düzelten 4.0.3 Nuget sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-498">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="cecdd-499">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cecdd-499">AzureRM.Compute</span></span>
* <span data-ttu-id="cecdd-500">PremiumLRS depolama hesap türü yeniden adlandırması nedeniyle New-AzureRmVm'de DiskFileParameterSet kullanılarak sanal makine oluşturmanın başarısız olmasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-500">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="cecdd-501">Invoke-AzureRmVMRunCommand cmdlet'i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-501">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="cecdd-502">Abonelikteki tüm kullanılabilir kümelerin listelenebilmesi için Get-AzureRmAvailabilitySet güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-502">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="cecdd-503">(ResouceGroupName parametresi artık isteğe bağlı.)</span><span class="sxs-lookup"><span data-stu-id="cecdd-503">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="cecdd-504">Uygun sanal makinelerde Hızlandırılmış Ağı etkinleştirmek için 'New-AzureRmVm' cmdlet'inin SimpleParameterSet öğesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-504">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="cecdd-505">Kullanıcının belirttiği LB zaten mevcut olduğunda vmss oluşturmanın başarısız olması için New-AzureRmVmss basit parametre kümesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-505">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="cecdd-506">New-AzureRmDisk örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-506">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="cecdd-507">'New-AzureRmVM' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-507">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="cecdd-508">Set-AzureRmVMOSDisk açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-508">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="cecdd-509">Yazımı ve ön eki düzeltmek amacıyla Set-AzureRmVMBginfoExtension için Örnek 1 güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-509">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="cecdd-510">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cecdd-510">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="cecdd-511">ADF .Net SDK sürümü 1.1.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-511">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="cecdd-512">Veri fabrikaları arasında paylaşılan şirket içinde barındırılan tümleştirme çalışma zamanı desteği.</span><span class="sxs-lookup"><span data-stu-id="cecdd-512">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="cecdd-513">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine yeni -SharedIntegrationRuntimeResourceId parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-513">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="cecdd-514">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine isteğe bağlı yeni -LinkedDataFactoryName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-514">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="cecdd-515">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cecdd-515">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="cecdd-516">DataPlane SDK'sı (Microsoft.Azure.DataLake.Store) sürümü 1.1.9'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-516">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="cecdd-517">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="cecdd-517">AzureRM.EventHub</span></span>
* <span data-ttu-id="cecdd-518">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-518">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="cecdd-519">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="cecdd-519">AzureRM.Insights</span></span>
* <span data-ttu-id="cecdd-520">Yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-520">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="cecdd-521">Microsoft.Azure.Management.Monitor SDK 0.19.1-preview kullanımı</span><span class="sxs-lookup"><span data-stu-id="cecdd-521">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="cecdd-522">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cecdd-522">AzureRM.KeyVault</span></span>
* <span data-ttu-id="cecdd-523">Set-AzureRmKeyVaultAccessPolicy'de yönlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-523">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="cecdd-524">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cecdd-524">AzureRM.Network</span></span>
* <span data-ttu-id="cecdd-525">LoadBalancerInboundNatPoolConfig cmdlet'leri için örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-525">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="cecdd-526">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cecdd-526">AzureRM.Resources</span></span>
* <span data-ttu-id="cecdd-527">'Get-AzureRmResource' için hem etiket adı hem de değer sağlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-527">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="cecdd-528">'Set-AzureRmResource' için yönlendirme senaryosu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-528">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="cecdd-529">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cecdd-529">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="cecdd-530">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-530">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="cecdd-531">birkaç sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-531">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="cecdd-532">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="cecdd-532">AzureRM.Sql</span></span>
* <span data-ttu-id="cecdd-533">Aşağıdaki cmdlet'lere Sunucu Gelişmiş Tehdit Koruması desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="cecdd-533">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="cecdd-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cecdd-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="cecdd-535">Aşağıdaki cmdlet'lere Güvenlik Açığı Değerlendirme desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="cecdd-535">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="cecdd-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="cecdd-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="cecdd-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="cecdd-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="cecdd-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="cecdd-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="cecdd-539">Remove-AzureRmSqlServerFirewallRulecmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-539">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="cecdd-540">Get-AzureSqlSyncGroupLog içinde ABD temelli olmayan kültürde yanlış tarih saat işlemesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-540">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="cecdd-541">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="cecdd-541">AzureRM.Storage</span></span>
* <span data-ttu-id="cecdd-542">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-542">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="cecdd-543">Tablo görünümünde StorageAccount cmdlet'i çıkışı gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="cecdd-543">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="cecdd-544">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cecdd-544">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="cecdd-545">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cecdd-545">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="cecdd-546">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cecdd-546">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="cecdd-547">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="cecdd-547">AzureRM.Tags</span></span>
* <span data-ttu-id="cecdd-548">Tag cmdlet'inin yardımında hatayı deyim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="cecdd-548">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="cecdd-549">6.5.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="cecdd-549">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="cecdd-550">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="cecdd-550">AzureRM.Profile</span></span>
* <span data-ttu-id="cecdd-551">'Get-AzureRmContextAutosaveSetting' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-551">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="cecdd-552">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="cecdd-552">Azure.Storage</span></span>
* <span data-ttu-id="cecdd-553">Salt yazılır Sas belirteciyle Karşıya Yükleme Blobu veya Dosyası desteği</span><span class="sxs-lookup"><span data-stu-id="cecdd-553">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="cecdd-554">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cecdd-554">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="cecdd-555">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cecdd-555">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="cecdd-556">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cecdd-556">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="cecdd-557">AS'ye gerekli ResourceGroupName özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-557">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="cecdd-558">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="cecdd-558">AzureRM.Automation</span></span>
* <span data-ttu-id="cecdd-559">'New-AzureRMAutomationSchedule' için yardım güncelleştirildi ve örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-559">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="cecdd-560">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cecdd-560">AzureRM.Compute</span></span>
* <span data-ttu-id="cecdd-561">Update/New-AzureRmAvailabilitySet komutlarına -Tag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-561">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="cecdd-562">'Add-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-562">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="cecdd-563">'Remove-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-563">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="cecdd-564">'Set-AzureRmVMAccessExtension' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-564">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="cecdd-565">New-AzureRmVmss için SimpleParameterSet güncelleştirilerek SinglePlacementGroup varsayılan olarak false değerine ayarlandı ve kullanıcının tek yerleşim grubunda VMSS oluşturmasına olanak tanıyan 'SinglePlacementGroup' geçiş parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-565">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="cecdd-566">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="cecdd-566">AzureRM.EventHub</span></span>
* <span data-ttu-id="cecdd-567">PSEventHubDRConfigurationAttributes sınıfına, çoğaltma işlemi devam ederken bekleyen çoğaltma işlemlerinin sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-567">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="cecdd-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cecdd-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="cecdd-569">Set-AzureRmKeyVaultAccessPolicy için hata iletisi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-569">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="cecdd-570">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cecdd-570">AzureRM.LogicApp</span></span>
* <span data-ttu-id="cecdd-571">New-AzureRmLogicApp’te "parametre kümesi çözümlenemedi" hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-571">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="cecdd-572">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cecdd-572">AzureRM.Network</span></span>
* <span data-ttu-id="cecdd-573">Set/Add-AzureRmVirtualNetworkPeering için birden çok Kiracıdaki Sanal Makineler arasında eşleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-573">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="cecdd-574">Aşağıdaki cmdlet’ler Application Gateway için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-574">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="cecdd-575">New-AzureRmApplicationGateway : EnableFIPS bayrağı ve Zones desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-575">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="cecdd-576">New-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-576">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="cecdd-577">Set-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-577">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="cecdd-578">RouteTable cmdlet’leri en son oluşturucu sürümüyle yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="cecdd-578">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="cecdd-579">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="cecdd-579">AzureRM.Relay</span></span>
* <span data-ttu-id="cecdd-580">Markdown dosyaları güncelleştirildi, örnekteki parametre adı sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="cecdd-580">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="cecdd-581">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cecdd-581">AzureRM.Resources</span></span>
* <span data-ttu-id="cecdd-582">Roleassignment ve roledefinition cmdlet’leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="cecdd-582">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="cecdd-583">Disk belleğinin parçası olarak yapılan ek roledefinition çağrıları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cecdd-583">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="cecdd-584">Get-AzureRmRoleAssignment cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-584">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="cecdd-585">-ExpandPrincipalGroups komut parametresi işlevselliği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-585">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="cecdd-586">'-ResourceType' parametresinin büyük/küçük harfe duyarlı olduğu 'Get-AzureRmResource' sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-586">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="cecdd-587">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cecdd-587">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="cecdd-588">Liste cmdlet’lerine top ve skip parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-588">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="cecdd-589">Standard'dan Premium NameSpace'e geçiş cmdlet’leri eklendi :</span><span class="sxs-lookup"><span data-stu-id="cecdd-589">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="cecdd-590">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="cecdd-590">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="cecdd-591">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="cecdd-591">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="cecdd-592">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="cecdd-592">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="cecdd-593">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="cecdd-593">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="cecdd-594">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="cecdd-594">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="cecdd-595">PSServiceBusDRConfigurationAttributes sınıfına, çoğaltma işlemi sürerken beklemede olan çoğaltma işlemi sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-595">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="cecdd-596">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cecdd-596">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="cecdd-597">'New-AzureRmServiceFabricCluster' için örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-597">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="cecdd-598">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="cecdd-598">AzureRM.Sql</span></span>
* <span data-ttu-id="cecdd-599">Müşterilerin Sql Server örneğine veya Yönetilen Örneğe TDE Sertifikası ekleyebilmeleri için yeni Management.Sql Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-599">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="cecdd-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="cecdd-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="cecdd-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="cecdd-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="cecdd-602">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="cecdd-602">AzureRM.Websites</span></span>
* <span data-ttu-id="cecdd-603">Artık `Set-AzureRmWebApp -AssignIdentity` ve `Set-AzureRmWebAppSlot -AssignIdentity` false olarak ayarlandığında site object.Removing önizleme etiketinden Identity özelliğini kaldırıyor.</span><span class="sxs-lookup"><span data-stu-id="cecdd-603">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="cecdd-604">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-604">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="cecdd-605">`Set-AzureRmWebApp -PhpVersion` geçerli bir php sürümü off değerini destekliyor</span><span class="sxs-lookup"><span data-stu-id="cecdd-605">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="cecdd-606">6.4.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="cecdd-606">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cecdd-607">Genel</span><span class="sxs-lookup"><span data-stu-id="cecdd-607">General</span></span>
* <span data-ttu-id="cecdd-608">Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-608">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="cecdd-609">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="cecdd-609">AzureRM.Profile</span></span>
* <span data-ttu-id="cecdd-610">Temel çıkış türlerine Ps1Xml özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-610">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="cecdd-611">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cecdd-611">AzureRM.Compute</span></span>
* <span data-ttu-id="cecdd-612">VMSS için IP Etiketi özelliği</span><span class="sxs-lookup"><span data-stu-id="cecdd-612">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="cecdd-613">'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-613">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="cecdd-614">New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-614">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="cecdd-615">VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-615">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="cecdd-616">New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-616">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="cecdd-617">VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği</span><span class="sxs-lookup"><span data-stu-id="cecdd-617">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="cecdd-618">Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-618">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="cecdd-619">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cecdd-619">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="cecdd-620">Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:</span><span class="sxs-lookup"><span data-stu-id="cecdd-620">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="cecdd-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cecdd-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="cecdd-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cecdd-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="cecdd-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cecdd-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="cecdd-624">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cecdd-624">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="cecdd-625">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-625">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="cecdd-626">Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-626">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="cecdd-627">Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-627">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="cecdd-628">DataLake cmdlet'lerinin test konumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-628">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="cecdd-629">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="cecdd-629">AzureRM.EventHub</span></span>
* <span data-ttu-id="cecdd-630">Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-630">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="cecdd-631">New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-631">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="cecdd-632">Varsayılan Parametre kümesi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="cecdd-632">Provided Default Parameter set.</span></span>
* <span data-ttu-id="cecdd-633">Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-633">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="cecdd-634">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cecdd-634">AzureRM.KeyVault</span></span>
* <span data-ttu-id="cecdd-635">Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-635">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="cecdd-636">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cecdd-636">AzureRM.Network</span></span>
* <span data-ttu-id="cecdd-637">Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="cecdd-637">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="cecdd-638">ARM aracılığıyla ExpressRoute Partner API'leri özelliği için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-638">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="cecdd-639">Get-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-639">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="cecdd-640">Set-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-640">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="cecdd-641">Add-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-641">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="cecdd-642">Get-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-642">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="cecdd-643">Remove-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-643">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="cecdd-644">Get-AzureRMExpressRouteCrossConnectionArpTable eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-644">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="cecdd-645">Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-645">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="cecdd-646">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-646">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="cecdd-647">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cecdd-647">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cecdd-648">Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-648">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="cecdd-649">Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="cecdd-649">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="cecdd-650">Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cecdd-650">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="cecdd-651">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cecdd-651">AzureRM.Resources</span></span>
* <span data-ttu-id="cecdd-652">Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="cecdd-652">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="cecdd-653">Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-653">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="cecdd-654">Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-654">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="cecdd-655">control parametresine -Effective ve -All anahtarları eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-655">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="cecdd-656">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-656">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="cecdd-657">Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-657">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="cecdd-658">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-658">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="cecdd-659">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-659">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="cecdd-660">Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-660">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="cecdd-661">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-661">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="cecdd-662">'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-662">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="cecdd-663">'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-663">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="cecdd-664">'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-664">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="cecdd-665">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cecdd-665">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="cecdd-666">Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-666">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="cecdd-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="cecdd-667">AzureRM.Sql</span></span>
* <span data-ttu-id="cecdd-668">New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-668">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="cecdd-669">Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-669">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="cecdd-670">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="cecdd-670">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="cecdd-671">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="cecdd-671">AzureRM.Profile</span></span>
* <span data-ttu-id="cecdd-672">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-672">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="cecdd-673">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="cecdd-673">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="cecdd-674">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="cecdd-674">Azure.Storage</span></span>
* <span data-ttu-id="cecdd-675">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-675">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="cecdd-676">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cecdd-676">AzureRM.Compute</span></span>
* <span data-ttu-id="cecdd-677">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-677">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="cecdd-678">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-678">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="cecdd-679">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="cecdd-679">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="cecdd-680">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="cecdd-680">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="cecdd-681">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="cecdd-681">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="cecdd-682">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="cecdd-682">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="cecdd-683">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cecdd-683">Start-AzureRmVM</span></span>
    - <span data-ttu-id="cecdd-684">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cecdd-684">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="cecdd-685">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cecdd-685">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="cecdd-686">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cecdd-686">Set-AzureRmVM</span></span>
    - <span data-ttu-id="cecdd-687">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cecdd-687">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="cecdd-688">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cecdd-688">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="cecdd-689">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="cecdd-689">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="cecdd-690">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="cecdd-690">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="cecdd-691">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cecdd-691">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="cecdd-692">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cecdd-692">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="cecdd-693">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cecdd-693">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="cecdd-694">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cecdd-694">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="cecdd-695">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="cecdd-695">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="cecdd-696">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="cecdd-696">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="cecdd-697">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="cecdd-697">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="cecdd-698">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="cecdd-698">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="cecdd-699">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="cecdd-699">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="cecdd-700">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="cecdd-700">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="cecdd-701">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="cecdd-701">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="cecdd-702">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cecdd-702">AzureRM.EventGrid</span></span>
* <span data-ttu-id="cecdd-703">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cecdd-703">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="cecdd-704">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cecdd-704">AzureRM.KeyVault</span></span>
* <span data-ttu-id="cecdd-705">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-705">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="cecdd-706">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cecdd-706">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="cecdd-707">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="cecdd-707">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="cecdd-708">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="cecdd-708">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="cecdd-709">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-709">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="cecdd-710">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cecdd-710">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cecdd-711">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-711">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="cecdd-712">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="cecdd-712">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="cecdd-713">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="cecdd-713">AzureRM.Sql</span></span>
* <span data-ttu-id="cecdd-714">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-714">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="cecdd-715">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cecdd-715">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="cecdd-716">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-716">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="cecdd-717">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="cecdd-717">AzureRM.Websites</span></span>
* <span data-ttu-id="cecdd-718">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-718">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="cecdd-719">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-719">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="cecdd-720">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="cecdd-720">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="cecdd-721">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cecdd-721">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="cecdd-722">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-722">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="cecdd-723">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="cecdd-723">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="cecdd-724">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="cecdd-724">AzureRM.Profile</span></span>
* <span data-ttu-id="cecdd-725">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-725">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="cecdd-726">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cecdd-726">AzureRM.Compute</span></span>
* <span data-ttu-id="cecdd-727">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="cecdd-727">VMSS VM Update feature</span></span>
    - <span data-ttu-id="cecdd-728">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-728">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="cecdd-729">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-729">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="cecdd-730">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cecdd-730">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="cecdd-731">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="cecdd-731">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="cecdd-732">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-732">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="cecdd-733">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-733">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="cecdd-734">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-734">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="cecdd-735">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-735">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="cecdd-736">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cecdd-736">AzureRM.KeyVault</span></span>
* <span data-ttu-id="cecdd-737">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-737">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="cecdd-738">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cecdd-738">AzureRM.Network</span></span>
* <span data-ttu-id="cecdd-739">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-739">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="cecdd-740">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cecdd-740">AzureRM.Resources</span></span>
* <span data-ttu-id="cecdd-741">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-741">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="cecdd-742">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="cecdd-742">AzureRM.Scheduler</span></span>
* <span data-ttu-id="cecdd-743">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-743">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="cecdd-744">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="cecdd-744">AzureRM.Sql</span></span>
* <span data-ttu-id="cecdd-745">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="cecdd-745">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="cecdd-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cecdd-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="cecdd-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="cecdd-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="cecdd-748">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cecdd-748">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="cecdd-749">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="cecdd-749">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="cecdd-750">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cecdd-750">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="cecdd-751">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="cecdd-751">AzureRM.Websites</span></span>
* <span data-ttu-id="cecdd-752">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-752">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="cecdd-753">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="cecdd-753">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="cecdd-754">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="cecdd-754">AzureRM.Profile</span></span>
* <span data-ttu-id="cecdd-755">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-755">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="cecdd-756">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cecdd-756">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="cecdd-757">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="cecdd-757">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="cecdd-758">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cecdd-758">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="cecdd-759">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-759">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="cecdd-760">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-760">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="cecdd-761">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-761">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="cecdd-762">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-762">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="cecdd-763">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-763">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="cecdd-764">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-764">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="cecdd-765">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-765">Added support for MSI identity</span></span>
* <span data-ttu-id="cecdd-766">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="cecdd-766">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="cecdd-767">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="cecdd-767">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="cecdd-768">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="cecdd-768">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="cecdd-769">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="cecdd-769">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="cecdd-770">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="cecdd-770">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="cecdd-771">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="cecdd-771">AzureRM.Batch</span></span>
* <span data-ttu-id="cecdd-772">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="cecdd-772">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="cecdd-773">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="cecdd-773">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="cecdd-774">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="cecdd-774">AzureRM.Consumption</span></span>
* <span data-ttu-id="cecdd-775">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="cecdd-775">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="cecdd-776">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cecdd-776">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="cecdd-777">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="cecdd-777">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="cecdd-778">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="cecdd-778">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="cecdd-779">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="cecdd-779">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="cecdd-780">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cecdd-780">AzureRM.Network</span></span>
* <span data-ttu-id="cecdd-781">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="cecdd-781">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="cecdd-782">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-782">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="cecdd-783">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cecdd-783">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="cecdd-784">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-784">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="cecdd-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="cecdd-786">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-786">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="cecdd-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="cecdd-788">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="cecdd-788">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="cecdd-789">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="cecdd-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="cecdd-790">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cecdd-790">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="cecdd-791">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="cecdd-791">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="cecdd-792">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="cecdd-792">AzureRM.Sql</span></span>
* <span data-ttu-id="cecdd-793">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cecdd-793">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="cecdd-794">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cecdd-794">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="cecdd-795">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cecdd-795">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="cecdd-796">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="cecdd-796">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="cecdd-797">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="cecdd-797">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="cecdd-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cecdd-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="cecdd-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="cecdd-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="cecdd-800">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cecdd-800">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="cecdd-801">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="cecdd-801">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="cecdd-802">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cecdd-802">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="cecdd-803">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cecdd-803">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="cecdd-804">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="cecdd-804">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
