---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 98bae70dbd61c74aa92e69cb67afc89ebae23f70
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928618"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="c1187-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="c1187-103">Azure PowerShell release notes</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="c1187-104">4.7.0 - Eylül 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-104">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-105">Az.Accounts</span></span>
* <span data-ttu-id="c1187-106">Yaklaşan yeni değişiklik iletileri biçimlendirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-106">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="c1187-107">Azure.Core 1.4.1 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-107">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="c1187-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c1187-108">Az.Aks</span></span>
* <span data-ttu-id="c1187-109">'New-AzAksCluster', 'Set-AzAksCluster' ve 'New-AzAksNodePool' için istemci tarafı parametre doğrulama mantığı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-109">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="c1187-110">[#12372]</span><span class="sxs-lookup"><span data-stu-id="c1187-110">[#12372]</span></span>
* <span data-ttu-id="c1187-111">'New-AzAksCluster' cmdlet’inde eklentilere yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-111">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="c1187-112">[#11239]</span><span class="sxs-lookup"><span data-stu-id="c1187-112">[#11239]</span></span>
* <span data-ttu-id="c1187-113">Eklentiler için 'Enable-AzAksAddOn' ve 'Disable-AzAksAddOn' cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-113">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="c1187-114">[#11239]</span><span class="sxs-lookup"><span data-stu-id="c1187-114">[#11239]</span></span>
* <span data-ttu-id="c1187-115">'New-AzAksCluster' için 'GenerateSshKey' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-115">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="c1187-116">[#12371]</span><span class="sxs-lookup"><span data-stu-id="c1187-116">[#12371]</span></span>
* <span data-ttu-id="c1187-117">API sürümü 2020-06-01 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-117">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c1187-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1187-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="c1187-119">Belirli API’ler için ek yasal koşullar gösterildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-119">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-120">Az.Compute</span></span>
* <span data-ttu-id="c1187-121">'New-AzVmDiskEncryptionSetConfig' için isteğe bağlı '-EncryptionType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-121">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="c1187-122">Yeni kaynak türü için yeni cmdlet’ler: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="c1187-122">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="c1187-123">'New-AzSnapshotConfig' cmdlet’ine isteğe bağlı '-DiskAccessId' ve '-NetworkAccessPolicy' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-123">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="c1187-124">'New-AzDiskConfig' cmdlet’ine isteğe bağlı '-DiskAccessId' ve '-NetworkAccessPolicy' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-124">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="c1187-125">VirtualMachine Örnek Görünümüne 'PatchStatus' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-125">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="c1187-126">'Get-AzVm' cmdlet’i '-Status' ile çağrıldığında döndürülen nesne olan 'VMHealth' özelliği, sanal makinenin örnek görünümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-126">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="c1187-127">'Get-AzVM' ve 'Get-AzVmss' örnek görünümlerine 'AssignedHost' alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-127">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="c1187-128">Alan, sanal makine örneğinin kaynak kimliğini gösterir</span><span class="sxs-lookup"><span data-stu-id="c1187-128">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="c1187-129">'New-AzHostGroup' cmdlet’ine isteğe bağlı '-SupportAutomaticPlacement' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-129">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="c1187-130">'New-AzVm' ve 'New-AzVmss' cmdlet’lerine '-HostGroupId' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-130">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-131">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-131">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-132">ADF .NET SDK’sı 4.11.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-132">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c1187-133">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1187-133">Az.EventHub</span></span>
* <span data-ttu-id="c1187-134">Yeni 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions' Cluster cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-134">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="c1187-135">#10722 numaralı soruna yönelik aşağıdaki düzeltmeler yapıldı: AuthorizationRule haklarına yalnızca 'Listen' atanabilecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-135">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="c1187-136">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="c1187-136">Az.Functions</span></span>
* <span data-ttu-id="c1187-137">Desteklemeyen bölgelerde v2 İşlevleri oluşturma özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-137">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="c1187-138">PowerShell 6.2 sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-138">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="c1187-139">Kullanıcı PowerShell 6.2 işlev uygulaması oluşturduğunda, bunun yerine PowerShell 7.0 işlev uygulaması oluşturmasını öneren bir uyarı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-139">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c1187-140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-140">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-141">Otomatik ölçeklendirme yapılandırmasıyla küme oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-141">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="c1187-142">'New-AzHDInsightCluster' cmdlet’ine yeni 'AutoscaleConfiguration' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-142">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="c1187-143">Kümenin Otomatik ölçeklendirme yapılandırmasını çalıştırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-143">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="c1187-144">Yeni 'Get-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-144">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="c1187-145">Yeni 'New-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-145">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="c1187-146">Yeni 'Set-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-146">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="c1187-147">Yeni 'Remove-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-147">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="c1187-148">Yeni 'New-AzHDInsihgtClusterAutoscaleScheduleCondition' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-148">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-149">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-149">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-150">RBAC yetkilendirmesi desteği eklendi [#10557]</span><span class="sxs-lookup"><span data-stu-id="c1187-150">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="c1187-151">'Set-AzKeyVaultAccessPolicy' cmdlet’indeki hata işleme özelliği iyileştirildi [#4007]</span><span class="sxs-lookup"><span data-stu-id="c1187-151">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="c1187-152">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="c1187-152">Az.Kusto</span></span>
* <span data-ttu-id="c1187-153">'Az.Kusto' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-153">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-154">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-154">Az.Network</span></span>
* <span data-ttu-id="c1187-155">[Yeni Değişiklik] Aşağıdaki cmdlet’ler, kaynak sanal yönlendiricisini ve sanal merkezi uyumlu hale getirecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-155">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="c1187-156">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="c1187-156">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="c1187-157">IP yapılandırması alt kaynağını desteklemek için -HostedSubnet parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-157">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="c1187-158">-HostedGateway ve -HostedGatewayId parametreleri silindi</span><span class="sxs-lookup"><span data-stu-id="c1187-158">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="c1187-159">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="c1187-159">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="c1187-160">Abonelik düzeyi parametre kümesi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-160">Added subscription level parameter set</span></span>
    - <span data-ttu-id="c1187-161">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="c1187-161">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="c1187-162">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="c1187-162">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="c1187-163">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="c1187-163">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="c1187-164">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="c1187-164">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="c1187-165">Azure ExpressRoute Bağlantı Noktası için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-165">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="c1187-166">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="c1187-166">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="c1187-167">VirtualNetwork Eşleme Kaynağına RemoteBgpCommunities özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-167">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="c1187-168">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-168">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="c1187-169">'Get-AzVpnGateway' çıkışına VpnGatewayIpConfigurations eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-169">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="c1187-170">'Set-AzApplicationGatewaySslCertificate' ile ilgili hata düzeltildi [#9488]</span><span class="sxs-lookup"><span data-stu-id="c1187-170">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="c1187-171">'AzureFirewall' öğesine 'AllowActiveFTP' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-171">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="c1187-172">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde internet güvenliğini ayarlama/kaldırma özelliği etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-172">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="c1187-173">'New-AzP2sVpnGateway' güncelleştirildi: Müşterilerin P2SVpnGateway üzerinde internet güvenliğini etkinleştirmek için true olarak ayarlayacakları, Noktadan siteye istemcilere uygulanacak olan isteğe bağlı 'EnableInternetSecurityFlag' anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-173">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="c1187-174">'Update-AzP2sVpnGateway' güncelleştirildi: Müşterilerin P2SVpnGateway üzerinde internet güvenliğini etkinleştirip devre dışı bırakmak için true/false olarak ayarlayacakları, Noktadan siteye istemcilere uygulanacak olan isteğe bağlı 'EnableInternetSecurityFlag' veya 'DisableInternetSecurityFlag' anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-174">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="c1187-175">Müşterilerin sorun giderme amacıyla VirtualWan P2SVpnGateway’lerini sıfırlamalarını/yeniden başlatmalarını sağlayan yeni 'Reset-AzP2sVpnGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-175">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="c1187-176">Müşterilerin sorun giderme amacıyla VirtualWan VpnGateway’lerini sıfırlamalarını/yeniden başlatmalarını sağlayan yeni 'Reset-AzVpnGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-176">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="c1187-177">'Set-AzVirtualNetworkSubnetConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-177">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="c1187-178">Parametrelerde açıkça ayarlanmışsa alt ağın NSG ve Yönlendirme Tablosu özelliklerinin null olarak ayarlanması [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="c1187-178">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-179">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-180">İş yükü Yedekleme Öğeleri için Silme Durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-180">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-181">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-181">Az.Resources</span></span>
* <span data-ttu-id="c1187-182">Eksik olan denetim Set-AzRoleAssignment cmdlet’ine eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-182">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="c1187-183">'Get-AzResourceGroupDeploymentOperation' cmdlet’inin 'SubscriptionId' parametresine hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-183">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="c1187-184">ARM şablonu What-If cmdlet’leri 'Ignore' kaynak değişiklikleri son olarak gösterülecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-184">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="c1187-185">Dağıtım cmdlet’lerindeki güvenlik ve dizi parametresi serileştirme sorunları düzeltildi [#12773]</span><span class="sxs-lookup"><span data-stu-id="c1187-185">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c1187-186">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1187-186">Az.ServiceFabric</span></span>
* <span data-ttu-id="c1187-187">Yönetilen kümeler ve düğüm türleri için yeni cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-187">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="c1187-188">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="c1187-188">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="c1187-189">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="c1187-189">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="c1187-190">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="c1187-190">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="c1187-191">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="c1187-191">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="c1187-192">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="c1187-192">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="c1187-193">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="c1187-193">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="c1187-194">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="c1187-194">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="c1187-195">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="c1187-195">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="c1187-196">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="c1187-196">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="c1187-197">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="c1187-197">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="c1187-198">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="c1187-198">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="c1187-199">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="c1187-199">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="c1187-200">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="c1187-200">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="c1187-201">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="c1187-201">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="c1187-202">Service Fabric SDK’sı, geçerli model için Service Fabric kaynak sağlayıcısı 2020-03-01 API sürümünü kullanan 1.2.0 sürümüne, yönetilen kümeler için 2020-01-01-preview sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-202">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-203">Az.Sql</span></span>
* <span data-ttu-id="c1187-204">'New-AzSqlInstance' ve 'Get-AzSqlInstance' cmdlet’lerine BackupStorageRedundancy eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-204">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="c1187-205">'Get-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-205">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="c1187-206">'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-206">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="c1187-207">'New-AzSqlInstance' cmdlet’ine Force parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-207">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="c1187-208">Yönetilen Veritabanı Günlük Yeniden Oynatma hizmetine cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-208">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="c1187-209">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="c1187-209">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="c1187-210">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="c1187-210">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="c1187-211">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="c1187-211">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="c1187-212">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="c1187-212">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="c1187-213">'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-213">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="c1187-214">'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-214">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="c1187-215">'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-215">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="c1187-216">Ağ yalıtım işlevselliğini desteklemek için 'New-AzSqlDatabaseImport' ve 'New-AzSqlDatabaseExport' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-216">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="c1187-217">'New-AzSqlDatabaseImportExisting' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-217">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="c1187-218">Database cmdlet’leri yedekleme alanı tür belirtimini destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-218">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="c1187-219">'New-AzSqlDatabase' cmdlet’ine Force parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-219">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="c1187-220">'New-AzSqlDatabase' cmdlet’indeki seçili bölgelerde yer alan BackupStorageRedundancy yapılandırmasına yönelik uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-220">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="c1187-221">Sunucu ve örneğe yönelik ActiveDirectoryOnlyAuthentication cmdlet’leri, ResourceId ve InputObject’i içerek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-221">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-222">Az.Storage</span></span>
* <span data-ttu-id="c1187-223">Microsoft.Azure.Storage.DataMovement 2.0.0 sürümüne yükseltme sırasında blob karşıya yüklenirken oluşan hata düzeltildi [#12220]</span><span class="sxs-lookup"><span data-stu-id="c1187-223">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="c1187-224">Belirli Bir Noktaya Geri Yükleme Desteği Eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-224">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="c1187-225">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="c1187-225">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="c1187-226">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="c1187-226">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="c1187-227">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="c1187-227">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="c1187-228">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="c1187-228">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="c1187-229">get-AzureRMStorageAccount cmdlet’ini -IncludeBlobRestoreStatus parametresiyle çalıştırarak Depolama hesabının blobu geri yükleme durumunu almaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-229">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="c1187-230">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c1187-230">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="c1187-231">Yaklaşan cmdlet çıkış değişikliği için hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-231">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="c1187-232">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="c1187-232">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="c1187-233">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="c1187-233">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="c1187-234">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="c1187-234">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="c1187-235">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="c1187-235">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="c1187-236">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="c1187-236">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="c1187-237">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="c1187-237">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="c1187-238">Microsoft.Azure.Cosmos.Table SDK 1.0.8 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-238">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="c1187-239">Topluluğumuzdan katkıda bulunanlara teşekkür ederiz</span><span class="sxs-lookup"><span data-stu-id="c1187-239">Thanks to our community contributors</span></span>
* <span data-ttu-id="c1187-240">Thomas Van Laere (@ThomVanL), Dockerfile-alpine-3.10’u ekledi (#12911)</span><span class="sxs-lookup"><span data-stu-id="c1187-240">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="c1187-241">Lohith Chowdary Chilukuri (@Lochiluk), Remove-AzNetworkInterfaceIpConfig.md dosyasını güncelleştirdi (#12807)</span><span class="sxs-lookup"><span data-stu-id="c1187-241">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="c1187-242">Roberth Strand (@roberthstrand), Get-AzResourceGroup-New örneği ve temizleme (#12828)</span><span class="sxs-lookup"><span data-stu-id="c1187-242">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="c1187-243">Ravi Mishra (@inmishrar), Azure Web App çalışma zamanı yığınını DOTNETCORE’a güncelleştirdi (#12833)</span><span class="sxs-lookup"><span data-stu-id="c1187-243">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="c1187-244">@jack-education, Set-AzVirtualNetworkSubnetConfig cmdlet’i NSG ve Rota Tablosunu alt ağdan kaldıracak şekilde güncelleştirdi (#12351)</span><span class="sxs-lookup"><span data-stu-id="c1187-244">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="c1187-245">@hagop-globanet, Add-AzApplicationGatewayCustomError.md dosyasını güncelleştirdi (#12784)</span><span class="sxs-lookup"><span data-stu-id="c1187-245">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="c1187-246">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="c1187-246">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="c1187-247">Özellikten Özelliğe yazımını güncelleştirdi (#12821)</span><span class="sxs-lookup"><span data-stu-id="c1187-247">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="c1187-248">New-AzResourceLock.md örneklerini güncelleştirdi (#12806)</span><span class="sxs-lookup"><span data-stu-id="c1187-248">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="c1187-249">Eragon Riddle (@eragonriddle), örnekteki parametre alanı adını düzeltti (#12825)</span><span class="sxs-lookup"><span data-stu-id="c1187-249">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="c1187-250">@rossifumax, New-AzConfigurationAssignment.md dosyasındaki yazım hatasını düzeltti (#12701)</span><span class="sxs-lookup"><span data-stu-id="c1187-250">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="c1187-251">4.6.1 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-251">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="c1187-252">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-252">Az.Compute</span></span>
* <span data-ttu-id="c1187-253">False değerinin varsayılan değerini kaldırmak için 'New-AzVm' içindeki '-EncryptionAtHost' parametresine yama uygulandı [#12776]</span><span class="sxs-lookup"><span data-stu-id="c1187-253">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="c1187-254">4.6.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-254">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-255">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-255">Az.Accounts</span></span>
* <span data-ttu-id="c1187-256">Bulma uç noktası varsayılan AzureCloud ortamını veya diğer genel ortamları döndürmediğinden tüm genel bulut ortamları yüklendi (#12633)</span><span class="sxs-lookup"><span data-stu-id="c1187-256">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="c1187-257">SubscriptionPolicies, 'Get-AzSubscription' cmdlet’inde kullanıma sunuldu [#12551]</span><span class="sxs-lookup"><span data-stu-id="c1187-257">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-258">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-258">Az.Automation</span></span>
* <span data-ttu-id="c1187-259">Karma Çalışanı Grubu belirtmek için 'Set-AzAutomationWebhook' cmdlet’ine '-RunOn' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-259">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-260">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-260">Az.Compute</span></span>
* <span data-ttu-id="c1187-261">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' ve 'Update-AzVmss' cmdlet’lerine '-EncryptionAtHost' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-261">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="c1187-262">'Get-AzVM' ve 'Get-AzVmss' cmdlet’lerinin dönüş nesnesine 'SecurityProfile' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-262">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="c1187-263">'-InstanceView' anahtarı 'Get-AzHostGroup' cmdlet’ine isteğe bağlı parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-263">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="c1187-264">Yeni 'Invoke-AzVmPatchAssessment' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-264">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-265">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-265">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-266">PSPipelineRun sınıfındaki eksik özellikler eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-266">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c1187-267">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-267">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-268">Konakta şifreleme özelliğiyle küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-268">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-269">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-269">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-270">Geçici silmeyi devre dışı bırakma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-270">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="c1187-271">SecretValueText özniteliğini kaldırma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-271">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="c1187-272">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="c1187-272">Az.Maintenance</span></span>
* <span data-ttu-id="c1187-273">'New-AzMaintenanceConfiguration' cmdlet’ine isteğe bağlı zamanlamayla ilgili alanlar eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-273">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="c1187-274">'Get-AzMaintenancePublicConfiguration' için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-274">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="c1187-275">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="c1187-275">Az.ManagedServices</span></span>
* <span data-ttu-id="c1187-276">Yönetilen hizmet atama ve tanım cmdlet’lerine hataya neden olan değişiklik uyarıları eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-276">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-277">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-277">Az.Monitor</span></span>
* <span data-ttu-id="c1187-278">Günlüklerin ve Ölçümlerin ayrılmasını etkinleştirmek için 'Set-AzDiagnosticSetting' cmdlet’indeki parametre kümesi genişletildi [#12482]</span><span class="sxs-lookup"><span data-stu-id="c1187-278">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="c1187-279">'Add-AzMetricAlertRuleV2' cmdlet’inde işlem hattından ölçüm uyarısı alınırken oluşan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-279">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-280">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-280">Az.Resources</span></span>
* <span data-ttu-id="c1187-281">'Get-AzPolicyAlias' cmdlet’i, diğer adın Azure İlkesi tarafından değiştirilebilir olup olmadığını belirten bilgiler içerek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-281">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="c1187-282">Yeni 'Set-AzRoleAssignment' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-282">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="c1187-283">Yönetim grubu kapsamındaki ARM şablonu Durum sonuçlarını almak için 'Get-AzDeploymentManagementGroupWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-283">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="c1187-284">Kiracı kapsamındaki ARM şablonu Durum sonuçlarını almaya yönelik yeni 'Get-AzTenantWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-284">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="c1187-285">'New-AzManagementGroupDeployment' ve 'New-AzTenantDeployment' için '-WhatIf' ve '-Confirm' parametreleri, ARM şablonu Durum sonuçlarını kullanacak şekilde geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="c1187-285">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="c1187-286">Yeni dağıtım cmdlet’lerindeki '-WhatIf' ve '-Confirm' parametrelerinin davranışları False ile uyumlu olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-286">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="c1187-287">'-TemplateObject' ve 'TemplateParameterObject' için serileştirme hatası düzeltildi [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="c1187-287">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="c1187-288">'Get-AzResourceGroupDeploymentOperation' cmdlet’ine, yaklaşan çıkış türü değişikliğine yönelik hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-288">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c1187-289">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c1187-289">Az.SignalR</span></span>
* <span data-ttu-id="c1187-290">'Restart-AzSignalR' ve 'Update-AzSignalR' yardım dosyalarındaki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-290">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="c1187-291">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-291">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-292">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-292">Az.Storage</span></span>
* <span data-ttu-id="c1187-293">Blob sorgu hızlandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-293">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="c1187-294">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="c1187-294">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="c1187-295">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="c1187-295">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="c1187-296">Yardım dosyası güncelleştirildi, daha fazla açıklama eklendi ve yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-296">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="c1187-297">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="c1187-297">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="c1187-298">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="c1187-298">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="c1187-299">İlgili alt dizin mevcut olmadığında blobu indirme işleminin başarısız olmasıyla ilgili sorun düzeltildi [#12592]</span><span class="sxs-lookup"><span data-stu-id="c1187-299">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="c1187-300">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="c1187-300">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="c1187-301">Depolama hesaplarında Set/Get/Remove Nesne Çoğaltma İlkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-301">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="c1187-302">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="c1187-302">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="c1187-303">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="c1187-303">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="c1187-304">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="c1187-304">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="c1187-305">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="c1187-305">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="c1187-306">Bir Depolama hesabının Blob Hizmeti üzerinde ChangeFeed’i etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-306">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="c1187-307">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="c1187-307">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="c1187-308">4.5.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-308">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-309">Az.Accounts</span></span>
* <span data-ttu-id="c1187-310">'Connect-AzAccount' cmdlet’i 'MaxContextPopulation' parametresini kabul edecek şekilde güncelleştirildi [#9865]</span><span class="sxs-lookup"><span data-stu-id="c1187-310">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="c1187-311">SubscriptionClient sürümü 2019-06-01 olarak ve kiracı etki alanlarını görüntüleyecek şekilde güncelleştirildi [#9838]</span><span class="sxs-lookup"><span data-stu-id="c1187-311">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="c1187-312">Aboneliğin giriş kiracısı ve yöneten kiracısı bilgilerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-312">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="c1187-313">Telemetri verilerindeki modül adı ve sürüm bilgileri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-313">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="c1187-314">SqlDatabaseDnsSuffix ve ServiceManagementUrl, ortam meta verileri uç noktasının uyumsuz değer döndürdüğü durumlar için ayarlandı</span><span class="sxs-lookup"><span data-stu-id="c1187-314">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="c1187-315">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c1187-315">Az.Aks</span></span>
* <span data-ttu-id="c1187-316">'ClientIdAndSecret' kaldırılarak 'ServicePrincipalIdAndSecret' eklendi ve 'ClientIdAndSecret' bir diğer ad olarak ayarlandı [#12381].</span><span class="sxs-lookup"><span data-stu-id="c1187-316">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="c1187-317">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' cmdlet’leri kaldırılarak 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' eklendi ve özgün olanlar diğer ad olarak ayarlandı [#12373].</span><span class="sxs-lookup"><span data-stu-id="c1187-317">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c1187-318">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-318">Az.ApiManagement</span></span>
* <span data-ttu-id="c1187-319">Yeni 'Add-AzApiManagementApiToGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-319">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="c1187-320">Yeni 'Get-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-320">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="c1187-321">Yeni 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-321">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="c1187-322">Yeni 'Get-AzApiManagementGatewayKey' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-322">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="c1187-323">Yeni 'New-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-323">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="c1187-324">Yeni 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-324">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="c1187-325">Yeni 'New-AzApiManagementResourceLocationObject' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-325">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="c1187-326">Yeni 'Remove-AzApiManagementApiFromGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-326">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="c1187-327">Yeni 'Remove-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-327">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="c1187-328">Yeni 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-328">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="c1187-329">Yeni 'Update-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-329">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="c1187-330">'Get-AzApiManagementApi' cmdlet’ine yeni ve isteğe bağlı [-GatewayId] parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-330">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c1187-331">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1187-331">Az.CognitiveServices</span></span>
* <span data-ttu-id="c1187-332">'Deny', özellikle NetworkRules varsayılan eylemi olarak kullanıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-332">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c1187-333">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c1187-333">Az.FrontDoor</span></span>
* <span data-ttu-id="c1187-334">Enum.Parse metodu, bir null değeri Enabled veya Disabled sabit listesi değerlerine zorladığında özel durum oluşturulmasıyla ilgili bir sorun düzeltildi [#12344]</span><span class="sxs-lookup"><span data-stu-id="c1187-334">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c1187-335">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-335">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-336">Aktarma özelliğinde şifrelemeye sahip küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-336">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="c1187-337">'New-AzHDInsightCluster' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-337">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="c1187-338">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-338">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="c1187-339">Özel bağlantı özelliğine sahip küme oluşturma desteği eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-339">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="c1187-340">'New-AzHDInsightCluster' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-340">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="c1187-341">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-341">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="c1187-342">'New-AzHDInsightCluster' veya 'Get-AzHDInsightCluster' çağrıldığında sanal ağ bilgileri döndürüldü</span><span class="sxs-lookup"><span data-stu-id="c1187-342">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-343">Az.Network</span></span>
* <span data-ttu-id="c1187-344">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-344">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="c1187-345">Hataya neden olmayan değişiklikler eklendi: 'Remove-AzExpressRouteCircutPeeringConfig' cmdlet’inde Özel Eşleme’ye yönelik PeerAddressType işlevi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-345">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="c1187-346">AddressPrefixType ve PeerAddressType parametresindeki kodlar büyük/küçük harfi yoksayacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-346">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="c1187-347">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-347">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c1187-348">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-348">Az.OperationalInsights</span></span>
* <span data-ttu-id="c1187-349">'Remove-AzOperationalInsightsworkspace' için '-ForceDelete' seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-349">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="c1187-350">Yeni 'Get-AzOperationalInsightsDeletedWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-350">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="c1187-351">Yeni 'Restore-AzOperationalInsightsWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-351">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-352">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-353">Azure Backup kapsayıcı/öğe keşif deneyimi iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-353">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-354">Az.Resources</span></span>
* <span data-ttu-id="c1187-355">'New-AzRoleAssignment' cmdlet’ine 'Condition', 'ConditionVersion' ve 'Description' özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-355">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="c1187-356">Bu, veri modellerinde yapılan tüm ilgili değişiklikleri içerir</span><span class="sxs-lookup"><span data-stu-id="c1187-356">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-357">Az.Sql</span></span>
* <span data-ttu-id="c1187-358">'New-AzSqlServer' ve 'Set-AzSqlServer' cmdlet’lerindeki sunucu adının olası büyük/küçük harfe duyarsızlık hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-358">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="c1187-359">'New-AzSqlDatabaseSecondary' cmdlet’indeki mevcut veritabanına yanlış veritabanı adının döndürülmesi hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-359">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-360">Az.Storage</span></span>
* <span data-ttu-id="c1187-361">Yeni x,t izniyle kapsayıcı/blob Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-361">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="c1187-362">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="c1187-362">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="c1187-363">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="c1187-363">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="c1187-364">Yeni x,t,f izniyle hesap Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-364">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="c1187-365">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="c1187-365">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="c1187-366">Tek dosya paylaşımı kullanımını alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-366">Supported get single file share usage</span></span>
    - <span data-ttu-id="c1187-367">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="c1187-367">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="c1187-368">4.4.0 - Temmuz 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-368">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-369">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-369">Az.Accounts</span></span>
* <span data-ttu-id="c1187-370">“Invoke-AzRestMethod” adlı yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-370">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="c1187-371">“Start-Job” kullanan birden çok Azure PowerShell cmdlet’inin çalıştığı durumlar gibi çok işlemli senaryolarda kimlik doğrulama hatalarına sebep olabilen bir sorun düzeltildi [#9448]</span><span class="sxs-lookup"><span data-stu-id="c1187-371">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="c1187-372">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c1187-372">Az.Aks</span></span>
* <span data-ttu-id="c1187-373">“Get-AzAks” cmdlet’inin tüm kümeleri almamasına neden olan hata düzeltildi [#12296]</span><span class="sxs-lookup"><span data-stu-id="c1187-373">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c1187-374">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c1187-374">Az.AnalysisServices</span></span>
* <span data-ttu-id="c1187-375">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-375">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-376">Az.Automation</span></span>
* <span data-ttu-id="c1187-377">Kaçış karakterleri içeren dizenin bir JSON nesnesine dönüştürülememesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-377">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-378">Az.Compute</span></span>
* <span data-ttu-id="c1187-379">“En son” resim sürümü olmadan “New-AzVmss” cmdlet’ini kullanırken görüntülenecek bir uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-379">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-380">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-380">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-381">Data Factory’ye genel parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-381">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c1187-382">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c1187-382">Az.EventGrid</span></span>
* <span data-ttu-id="c1187-383">2020-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-383">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="c1187-384">Yeni özellikler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-384">Added new features:</span></span>
    - <span data-ttu-id="c1187-385">Giriş eşleme</span><span class="sxs-lookup"><span data-stu-id="c1187-385">Input mapping</span></span>
    - <span data-ttu-id="c1187-386">Olay Teslim Şeması</span><span class="sxs-lookup"><span data-stu-id="c1187-386">Event Delivery Schema</span></span>
    - <span data-ttu-id="c1187-387">Özel Bağlantı</span><span class="sxs-lookup"><span data-stu-id="c1187-387">Private Link</span></span>
    - <span data-ttu-id="c1187-388">Bulut Olayı V10 Şeması</span><span class="sxs-lookup"><span data-stu-id="c1187-388">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="c1187-389">Hedef Olarak Service Bus Konu Başlığı</span><span class="sxs-lookup"><span data-stu-id="c1187-389">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="c1187-390">Hedef Olarak Azure İşlevi</span><span class="sxs-lookup"><span data-stu-id="c1187-390">Azure Function As Destination</span></span>
    - <span data-ttu-id="c1187-391">Web Kancası Toplu İş</span><span class="sxs-lookup"><span data-stu-id="c1187-391">WebHook Batching</span></span>
    - <span data-ttu-id="c1187-392">Güvenli web kancası (AAD desteği)</span><span class="sxs-lookup"><span data-stu-id="c1187-392">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="c1187-393">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="c1187-393">IpFiltering</span></span>
* <span data-ttu-id="c1187-394">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-394">Updated cmdlets:</span></span>
    - <span data-ttu-id="c1187-395">“New-AzEventGridSubscription'/'Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="c1187-395">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="c1187-396">Web kancası toplu işlemin destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-396">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="c1187-397">AAD kullanarak güvenli web kancasını desteklemek için yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-397">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="c1187-398">Yeni hedef olarak Azure İşlevi’ni ve Service Bus konu başlığını desteklemek üzere EndpointType parametresi için yeni bir sabit listesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-398">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="c1187-399">Teslim şeması için yeni, isteğe bağlı parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-399">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="c1187-400">“New-AzEventGridTopic'/'Update-AzEventGridTopic” ve “New-AzEventGridDomain'/'Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="c1187-400">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="c1187-401">IpFiltering’i destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-401">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="c1187-402">“New-AzEventGridTopic'/'New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="c1187-402">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="c1187-403">Giriş eşlemeyi destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-403">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c1187-404">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c1187-404">Az.FrontDoor</span></span>
* <span data-ttu-id="c1187-405">Modül, API 2020-05-01 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-405">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="c1187-406">Depolama, Key Vault ve Web App Service kaynakları için Özel bağlantı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-406">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c1187-407">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-407">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-408">Ulusal bulutlarda ADLS 1. veya 2. Nesil depolama ile küme oluşturmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-408">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-409">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-409">Az.Monitor</span></span>
* <span data-ttu-id="c1187-410">Ölçümler ve günlükler null olduğunda “Get-AzDiagnosticSetting” cmdlet’inde oluşan hata düzeltildi [#12272]</span><span class="sxs-lookup"><span data-stu-id="c1187-410">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-411">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-411">Az.Network</span></span>
* <span data-ttu-id="c1187-412">VWan HubVnet bağlantısında değişen parametreler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-412">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="c1187-413">Azure Ağ Sanal Alet Siteleri’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-413">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="c1187-414">“Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="c1187-414">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="c1187-415">“New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="c1187-415">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="c1187-416">“Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="c1187-416">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="c1187-417">“Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="c1187-417">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="c1187-418">“New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="c1187-418">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="c1187-419">Azure Ağ Sanal Gereçi’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-419">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="c1187-420">“Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="c1187-420">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="c1187-421">“New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="c1187-421">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="c1187-422">“Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="c1187-422">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="c1187-423">“Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="c1187-423">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="c1187-424">“Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="c1187-424">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="c1187-425">“New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="c1187-425">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="c1187-426">Özel Bağlantı Ortak Cmdlet’lerine Application Gateway eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-426">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="c1187-427">Özel Bağlantı Ortak Cmdlet’lerine StorageSync Eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-427">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="c1187-428">Özel Bağlantı Ortak Cmdlet’lerine SignalR Eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-428">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-429">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-429">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-430">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-430">Removed project reference to Authentication</span></span>
* <span data-ttu-id="c1187-431">Azure Backup, cmdlet’leri metinlerin daha doğru görüneceği şekilde ayarladı</span><span class="sxs-lookup"><span data-stu-id="c1187-431">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="c1187-432">Azure Backup, “Get-AzRecoveryServicesBackupJob” cmdlet’i kullanılarak MAB aracı işlerinin getirilmesine yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="c1187-432">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-433">Az.Resources</span></span>
* <span data-ttu-id="c1187-434">“Save-AzResourceGroupDeploymentTemplate” cmdlet’i SDK’yı kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-434">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="c1187-435">“Unregister-AzResourceProvider” cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-435">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-436">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-436">Az.Sql</span></span>
* <span data-ttu-id="c1187-437">“Set-AzSqlInstanceActiveDirectoryAdministrator” cmdlet’indeki Hizmet sorumlusu ve konuk kullanıcılara yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-437">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="c1187-438">Veri Sınıflandırma cmdlet’lerindeki bir sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-438">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="c1187-439">Azure SQL Yönetilen Örneği yük devretmesine yönelik destek eklendi: “Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="c1187-439">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-440">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-440">Az.Storage</span></span>
* <span data-ttu-id="c1187-441">Bazı veri düzlemi cmdlet’leri için UserAgent’ın eklenmemesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-441">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="c1187-442">MinimumTlsVersion ve AllowBlobPublicAccess içeren bir Depolama hesabını oluşturmaya/güncelleştirmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-442">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="c1187-443">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c1187-443">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="c1187-444">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c1187-444">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="c1187-445">Bir Depolama hesabının Blob Hizmeti üzerinde sürüm oluşturmayı etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-445">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="c1187-446">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="c1187-446">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="c1187-447">Blob sürümlerini içeren destek listesi blobları</span><span class="sxs-lookup"><span data-stu-id="c1187-447">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="c1187-448">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="c1187-448">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="c1187-449">Tek bir blob anlık görüntüsünü veya blob sürümünü almaya/kaldırmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-449">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="c1187-450">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="c1187-450">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="c1187-451">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="c1187-451">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="c1187-452">Azure.Storage.Blobs V12’den oluşturulan blob nesnesindeki işlem hattına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-452">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="c1187-453">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="c1187-453">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="c1187-454">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="c1187-454">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="c1187-455">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="c1187-455">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="c1187-456">“Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="c1187-456">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="c1187-457">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="c1187-457">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c1187-458">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c1187-458">Az.StorageSync</span></span>
* <span data-ttu-id="c1187-459">ApiVersion 2020-03-01 sürümünü hedefleyen yeni bir StorageSync SDK sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-459">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="c1187-460">“UpdateStorageSyncService” cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-460">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="c1187-461">“Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="c1187-461">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="c1187-462">StorageSyncService cmdlet’ine IncomingTrafficPolicy ve PrivateEndpointConnections eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-462">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-463">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-463">Az.Websites</span></span>
* <span data-ttu-id="c1187-464">App Service Planıyla aynı kaynak grubunda bulunmayan Yuvalar için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-464">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="c1187-465">4.3.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-465">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-466">Az.Accounts</span></span>
* <span data-ttu-id="c1187-467">Ortam ayarını varsayılan olarak bulma ve 'Add-AzEnvironment' aracılığıyla ortam ekleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-467">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="c1187-468">Önceden yüklenmiş bütünleştirilmiş kodlar güncelleştirildi [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="c1187-468">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="c1187-469">Azure.Core bütünleştirilmiş kodu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-469">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="c1187-470">'Connect-AzAccount' cmdlet’inin çok iş parçacıklı yürütmede başarısız olmasına neden olabilen bir sorun düzeltildi [#11201]</span><span class="sxs-lookup"><span data-stu-id="c1187-470">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="c1187-471">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c1187-471">Az.Aks</span></span>
* <span data-ttu-id="c1187-472">Eski [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)’sinin kullanımı [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) ve [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API’lerine yönelik çağrılarla değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-472">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c1187-473">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c1187-473">Az.Batch</span></span>
* <span data-ttu-id="c1187-474">Az.Batch, 'Microsoft.Azure.Management.Batch' SDK sürüm 11.0.0 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-474">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="c1187-475">BatchAccount.Identity özelliğini 'New-AzBatchAccount' cmdlet’ine ayarlama özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-475">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c1187-476">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1187-476">Az.CognitiveServices</span></span>
* <span data-ttu-id="c1187-477">Hesap özelliklerini görüntüleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-477">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="c1187-478">PublicNetworkAccess özelliğinin değiştirilmesi desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-478">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-479">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-479">Az.Compute</span></span>
* <span data-ttu-id="c1187-480">Set-AzVM ve Set-AzVmssVM cmdlet’lerine SimulateEviction parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-480">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="c1187-481">New-AzGalleryImageVersion cmdlet’i için StorageAccountType parametresinin bağımsız değişken tamamlayıcısına 'Premium_LRS' eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-481">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="c1187-482">VMCustomScriptExtension için Alt Durumlar eklendi [#11297]</span><span class="sxs-lookup"><span data-stu-id="c1187-482">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="c1187-483">New-AzVM ve New-AzVMConfig cmdlet’leri için EvictionPolicy parametresinin bağımsız değişken tamamlayıcısına 'Delete' eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-483">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="c1187-484">SAP için yeni VM Uzantısı’nın adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-484">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-485">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-485">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-486">ADF .NET SDK’sı 4.9.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-486">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c1187-487">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1187-487">Az.EventHub</span></span>
* <span data-ttu-id="c1187-488">'New-AzEventHubNamespace' ve 'Set-AzEventHubNamespace' cmdlet’lerine Yönetilen Kimlik parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-488">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="c1187-489">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="c1187-489">Az.Functions</span></span>
* <span data-ttu-id="c1187-490">PowerShell 7.0 ve Java 11 işlev uygulamaları oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-490">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c1187-491">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-491">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-492">HDInsight kümesinin konaklarını listeleme ve belirli konaklarını yeniden başlatma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-492">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="c1187-493">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="c1187-493">Az.HealthcareApis</span></span>
* <span data-ttu-id="c1187-494">SDK sürümü 1.1.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-494">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="c1187-495">Dışarı aktarma ayarları ve Yönetilen Kimlik desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-495">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-496">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-496">Az.Monitor</span></span>
* <span data-ttu-id="c1187-497">'Set-AzActivityLogAlert' için giriş nesnesi parametresi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-497">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="c1187-498">'Set-AzActionGroup' için 'InputObject' parametresi düzeltildi [#10868]</span><span class="sxs-lookup"><span data-stu-id="c1187-498">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-499">Az.Network</span></span>
* <span data-ttu-id="c1187-500">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-500">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="c1187-501">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-501">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="c1187-502">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="c1187-502">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="c1187-503">Güvenlik Duvarı İlkesi için Ağ Kuralları’nda Hedef FQDN Desteği</span><span class="sxs-lookup"><span data-stu-id="c1187-503">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="c1187-504">Arka uç adres havuzu işlemlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-504">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="c1187-505">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="c1187-505">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="c1187-506">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="c1187-506">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="c1187-507">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="c1187-507">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="c1187-508">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="c1187-508">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="c1187-509">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="c1187-509">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="c1187-510">'New-AzIpGroup' için ad doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-510">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="c1187-511">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-511">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="c1187-512">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="c1187-512">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="c1187-513">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde özel DNS sunucuları ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="c1187-513">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="c1187-514">New-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-514">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="c1187-515">Update-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-515">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="c1187-516">'Update-AzVpnGateway' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-516">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="c1187-517">Müşterilerin özel BGP’lerini VpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-BgpPeeringAddress' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-517">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="c1187-518">Bir VirtualHub kaynağının yönlendirme durumunu sıfırlamayı desteklemek amacıyla yeni cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-518">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="c1187-519">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="c1187-519">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="c1187-520">Güvenlik Duvarı İlkesi’nde yapılan son Swagger değişikliğine göre aşağıdakiler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-520">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="c1187-521">RuleGroup, RuleCollectionGroup ve RuleType adları değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-521">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="c1187-522">Birden çok NAT Kural Koleksiyonu’nu desteklemek amacıyla Güvenlik Duvarı İlkesi NAT Kural Koleksiyonları’na yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-522">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="c1187-523">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule' ve 'New-AzFirewallPolicyNetworkRule' için 'SourceIpGroup' zorunlu parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-523">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="c1187-524">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-524">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="c1187-525">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-525">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="c1187-526">[Yeni Değişiklik] Şu zorunu parametreler kaldırıldı: 'New-AzFirewallPolicyNatRuleCollection' için 'TranslatedAddress', 'TranslatedPort'.</span><span class="sxs-lookup"><span data-stu-id="c1187-526">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="c1187-527">Application Gateway üzerinde PrivateLink’i destekleyecek yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-527">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="c1187-528">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c1187-528">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="c1187-529">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c1187-529">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="c1187-530">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c1187-530">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="c1187-531">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c1187-531">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="c1187-532">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c1187-532">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="c1187-533">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c1187-533">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="c1187-534">VirtualHub’ın HubRouteTables alt kaynağı için yeni cmdlet’ler eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-534">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="c1187-535">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="c1187-535">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="c1187-536">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="c1187-536">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="c1187-537">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="c1187-537">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="c1187-538">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="c1187-538">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="c1187-539">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="c1187-539">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="c1187-540">Mevcut cmdlet’ler VirtualWan’deki özel yönlendirmede isteğe bağlı RoutingConfiguration giriş parametresini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-540">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="c1187-541">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="c1187-541">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="c1187-542">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="c1187-542">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="c1187-543">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="c1187-543">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="c1187-544">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="c1187-544">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="c1187-545">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="c1187-545">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="c1187-546">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="c1187-546">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="c1187-547">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="c1187-547">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="c1187-548">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="c1187-548">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c1187-549">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-549">Az.OperationalInsights</span></span>
* <span data-ttu-id="c1187-550">PSWorkspace’in OperationalInsightsWorkspace’i uygulamamasıyla ilgili hata düzeltildi [#12135]</span><span class="sxs-lookup"><span data-stu-id="c1187-550">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="c1187-551">'Set-AzOperationalInsightsWorkspace' cmdlet’indeki 'Sku' parametresinin geçerli değer kümesine 'pergb2018' eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-551">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="c1187-552">'FunctionParameter' parametresi için 'FunctionParameters' diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-552">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="c1187-553">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="c1187-553">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="c1187-554">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="c1187-554">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-555">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-556">Azure Backup’a MAB öğelerini getirme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-556">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="c1187-557">Azure Site Recovery, 'StandardSSD_LRS' disk türünü destekler</span><span class="sxs-lookup"><span data-stu-id="c1187-557">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-558">Az.Resources</span></span>
* <span data-ttu-id="c1187-559">'PSADUser' değerine 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname' eklendi [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="c1187-559">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="c1187-560">'Get-AzADUser' üzerinde '-Mail' değerinin çalışmamasıyla ilgili sorun düzeltildi [#11981]</span><span class="sxs-lookup"><span data-stu-id="c1187-560">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="c1187-561">'Get-AzDeploymentWhatIfResult' ve 'Get-AzResourceGroupDeploymentWhatIfResult' cmdlet’lerine -ExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-561">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="c1187-562">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' cmdlet’lerine '-WhatIfExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-562">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="c1187-563">'Test-Az\*Deployment' cmdlet’leri daha iyi hata iletileri gösterecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-563">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="c1187-564">deployment create ve What-If cmdlet’lerinin '-Name' parametresine yönelik yardım iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-564">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-565">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-565">Az.Sql</span></span>
* <span data-ttu-id="c1187-566">SQL Server Azure Active Directory Yönetici cmdlet’ine hizmet sorumlusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-566">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="c1187-567">Veri Sınıflandırma cmdlet’lerindeki eşitleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-567">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="c1187-568">'Set-AzSqlServerActiveDirectoryAdministrator' üzerinde postaya göre kullanıcı arama desteği eklendi [#12192]</span><span class="sxs-lookup"><span data-stu-id="c1187-568">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-569">Az.Storage</span></span>
* <span data-ttu-id="c1187-570">RequireInfrastructureEncryption ile Depolama hesabı oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-570">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="c1187-571">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c1187-571">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="c1187-572">Azure.Core yükleme mantığı Az.Accounts’a taşındı</span><span class="sxs-lookup"><span data-stu-id="c1187-572">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-573">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-573">Az.Websites</span></span>
* <span data-ttu-id="c1187-574">'Restore-AzDeletedWebApp' cmdlet’inde geri yüklemenin başarısız olması durumunda, oluşturulan web uygulamasının silinmesine yönelik koruma eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-574">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="c1187-575">'New-AzWebApp' ve 'New-AzWebAppSlot' için SourceWebApp.Location' eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-575">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="c1187-576">'Set-AzWebApp' ve 'Set-AzWebAppSlot' cmdlet’lerinde Kapsayıcı ayarlarının değiştirilmesini engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-576">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="c1187-577">Get-AzWebApp için -Name verilmediğinde SiteConfig alınmasıyla ilgili hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-577">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="c1187-578">Linux Uygulamaları için ASP oluşturmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-578">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="c1187-579">Kaynak grupları arasında kopyalama için özel durumlar eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-579">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="c1187-580">4.2.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-580">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-581">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-581">Az.Accounts</span></span>
* <span data-ttu-id="c1187-582">Azure Otomasyonu veya PowerShell işlerinde Az’nin günlükleri atlamasına neden olabilecek bir sorun düzeltildi [#11492]</span><span class="sxs-lookup"><span data-stu-id="c1187-582">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c1187-583">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c1187-583">Az.AnalysisServices</span></span>
* <span data-ttu-id="c1187-584">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-584">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c1187-585">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-585">Az.ApiManagement</span></span>
* <span data-ttu-id="c1187-586">Hizmet yönetimi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-586">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="c1187-587">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c1187-587">Az.Billing</span></span>
* <span data-ttu-id="c1187-588">Tüketim cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-588">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c1187-589">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1187-589">Az.CognitiveServices</span></span>
* <span data-ttu-id="c1187-590">PrivateEndpoint ve PublicNetworkAccess denetimini destekler.</span><span class="sxs-lookup"><span data-stu-id="c1187-590">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-591">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-592">Veri fabrikası V2 cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-592">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="c1187-593">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="c1187-593">Az.DataShare</span></span>
* <span data-ttu-id="c1187-594">''Az.DataShare'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-594">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="c1187-595">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="c1187-595">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="c1187-596">''Az.DesktopVirtualization'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-596">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c1187-597">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-597">Az.OperationalInsights</span></span>
* <span data-ttu-id="c1187-598">SDK 0.21.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-598">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="c1187-599">İsteğe bağlı aşağıdaki parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-599">Added optional parameters to</span></span> 
    - <span data-ttu-id="c1187-600">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="c1187-600">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="c1187-601">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="c1187-601">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c1187-602">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-602">Az.PolicyInsights</span></span>
* <span data-ttu-id="c1187-603">'Start-AzPolicyComplianceScan' için 3. örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-603">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="c1187-604">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c1187-604">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="c1187-605">PowerBI cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-605">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="c1187-606">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="c1187-606">Az.PrivateDns</span></span>
* <span data-ttu-id="c1187-607">Remove-AzPrivateDnsRecordSet için ayrıntılı çıkış dizesi biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-607">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-608">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-608">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-609">XML girişinden bölgeler arasında çoğaltma için kurtarma planı oluşturmaya yönelik Azure Site Recovery desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-609">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="c1187-610">SiteRecovery ve Backup cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-610">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-611">Az.Resources</span></span>
* <span data-ttu-id="c1187-612">Get-AzDeploymentScriptLog ve Save-AzDeploymentScriptLog cmdlet’lerine Tail parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-612">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="c1187-613">Çıkış özelliği biçimlendirildi ve Get-AzDeploymentScript cmdlet çıkışında gösterildi</span><span class="sxs-lookup"><span data-stu-id="c1187-613">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="c1187-614">-DeploymentScriptInputObject parametresinin adı -DeploymentScriptObject olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-614">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="c1187-615">Cmdlet iletilerinde geçersiz dosya/hedef adı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-615">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="c1187-616">Kaynak yöneticisi ve etiketler cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-616">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-617">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-617">Az.Sql</span></span>
* <span data-ttu-id="c1187-618">'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine UsePrivateLinkConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-618">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="c1187-619">'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine SyncMemberAzureDatabaseResourceId eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-619">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="c1187-620">SQL Server Azure Active Directory Yönetici cmdlet’ine Konuk kullanıcı arama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-620">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-621">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-621">Az.Storage</span></span>
* <span data-ttu-id="c1187-622">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-622">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="c1187-623">4.1.0 - Mayıs 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-623">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="c1187-624">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="c1187-624">Highlights since the last release</span></span>
* <span data-ttu-id="c1187-625">Desteklenen PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="c1187-625">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="c1187-626">Az.Functions genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-626">General availability of Az.Functions</span></span> 
* <span data-ttu-id="c1187-627">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources ve Az.Storage için ana sürüm yayımlandı</span><span class="sxs-lookup"><span data-stu-id="c1187-627">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c1187-628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-628">Az.Accounts</span></span>
* <span data-ttu-id="c1187-629">'Add-AzEnvironment' ve 'Set-AzEnvironment', 'AzureSynapseAnalyticsEndpointResourceId' ve 'AzureSynapseAnalyticsEndpointSuffix' parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-629">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="c1187-630">Azure.Core ile ilgili bütünleştirilmiş kodlar Az.Accounts’a eklendi, desteklenen PowerShell platformları Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+ sürümlerini içerir</span><span class="sxs-lookup"><span data-stu-id="c1187-630">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="c1187-631">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c1187-631">Az.Aks</span></span>
* <span data-ttu-id="c1187-632">API Sürümü 2019-10-01’e yükseltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-632">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="c1187-633">Windows kapsayıcısı kullanılarak AKS oluşturma desteği sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-633">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="c1187-634">Yeni cmdlet’ler sağlandı: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="c1187-634">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c1187-635">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-635">Az.ApiManagement</span></span>
* <span data-ttu-id="c1187-636">'New-AzApiManagement' ve 'Set-AzApiManagement': [-AssignIdentity] parametresi [-SystemAssignedIdentity] olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-636">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="c1187-637">'New-AzApiManagement' ve 'Set-AzApiManagement': Yeni parametre eklendi: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="c1187-637">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="c1187-638">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-638">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="c1187-639">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-639">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="c1187-640">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-640">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="c1187-641">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-641">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="c1187-642">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-642">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="c1187-643">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-643">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="c1187-644">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-644">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="c1187-645">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-645">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="c1187-646">Yeni 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementAuthorizationServer' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c1187-646">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="c1187-647">Yeni 'Get-AzApiManagementNamedValueSecretValue' cmdlet’i eklendi. 'Get-AzApiManagementNamedValue' artık gizli dizi değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c1187-647">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="c1187-648">Yeni 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementOpenIdConnectProvider' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c1187-648">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="c1187-649">Yeni 'Get-AzApiManagementSubscriptionKey' cmdlet’i eklendi. 'Get-AzApiManagementSubscription' artık abonelik anahtarlarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c1187-649">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="c1187-650">Yeni 'Get-AzApiManagementTenantAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c1187-650">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="c1187-651">Yeni 'Get-AzApiManagementTenantGitAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantGitAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c1187-651">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="c1187-652">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-652">Az.ApplicationInsights</span></span>
* <span data-ttu-id="c1187-653">Parametreler eklendi: 'New-AzApplicationInsights' için 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="c1187-653">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="c1187-654">'Update-AzApplicationInsights' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-654">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="c1187-655">Bağlı Depolama Hesapları için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-655">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c1187-656">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c1187-656">Az.Batch</span></span>
* <span data-ttu-id="c1187-657">Az.Batch, 'Microsoft.Azure.Batch' SDK sürüm 13.0.0 ve 'Microsoft.Azure.Management.Batch' SDK sürüm 9.0.0 kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-657">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="c1187-658">'New-AzBatchCertificate' için yeni '-CertificateKind' parametresi kullanılarak eklenen sertifika türünü seçme yeteneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-658">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="c1187-659">Önceden hep '' olan 'ApplicationPackages' özelliği 'PSApplication' öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-659">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="c1187-660">Uygulamanın içindeki belirli paketler artık 'Get-AzBatchApplicationPackage' kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="c1187-660">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="c1187-661">Örneğin: 'Get-AzBatchApplication -AccountName hesabım -ResourceGroupName kaynakgrubum -ApplicationId uygulamam'.</span><span class="sxs-lookup"><span data-stu-id="c1187-661">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="c1187-662">'New-AzBatchPool' kullanılarak havuz oluşturulurken, 'PSImageReference' öğesinin 'VirtualMachineImageId' özelliği artık yalnızca bir Paylaşılan Görüntü Galerisi görüntüsüne başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="c1187-662">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="c1187-663">'New-AzBatchPool' kullanılarak havuz oluşturulurken, havuz 'PSNetworkConfiguration' öğesinin yeni 'PublicIPAddressConfiguration' özelliği kullanılarak genel IP olmadan sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c1187-663">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="c1187-664">'PSNetworkConfiguration' öğesinin 'PublicIPs' özelliği de 'PSPublicIPAddressConfiguration' içine taşındı.</span><span class="sxs-lookup"><span data-stu-id="c1187-664">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="c1187-665">Bu özellik yalnızca 'IPAddressProvisioningType' değeri 'UserManaged' olduğunda belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="c1187-665">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-666">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-666">Az.Compute</span></span>
* <span data-ttu-id="c1187-667">'Update-AzVM' cmdlet’ine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-667">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="c1187-668">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' ve 'Set-AzVmssOsProfile' cmdlet’leri için Yardım belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-668">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="c1187-669">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c1187-669">Breaking changes</span></span>
    - <span data-ttu-id="c1187-670">FilterExpression parametresi 'Get-AzVMImage' cmdlet’inden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-670">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="c1187-671">AssignIdentity parametresi 'New-AzVmssConfig', 'New-AzVMConfig' ve 'Update-AzVM' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-671">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="c1187-672">AutomaticRepairMaxInstanceRepairsPercent, 'New-AzVmssConfig' ve 'Update-AzVmss' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-672">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="c1187-673">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus ve VirtualMachineScaleSetsColocationStatus özellikleri ProximityPlacementGroup öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-673">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="c1187-674">MaxInstanceRepairsPercent özelliği AutomaticRepairsPolicy öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-674">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="c1187-675">AvailabilitySets, VirtualMachines ve VirtualMachineScaleSets türleri IList<SubResource> türünden IList<SubResourceWithColocationStatus> türüne değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-675">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="c1187-676">'Get-AzVM' cmdlet’inin açıklaması, cmdlet’i daha iyi açıklayacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-676">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-677">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-677">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-678">Yönetilen IR içinde veri akışı çalışma zamanı özelliklerinin CRUD’si desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-678">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c1187-679">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c1187-679">Az.FrontDoor</span></span>
* <span data-ttu-id="c1187-680">Front Door Kural Altyapısı nesnesini oluşturmak, güncelleştirmek, almak ve silmek için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-680">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="c1187-681">Front Door Kural Altyapısı nesnesini oluşturmak için yardımcı cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-681">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="c1187-682">Front Door Yönlendirme Kuralı nesnesine Kural Altyapısı başvurusu eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-682">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="c1187-683">Front Door Arka Uç nesnesine Özel Bağlantı parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-683">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="c1187-684">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="c1187-684">Az.Functions</span></span>
* <span data-ttu-id="c1187-685">''Az.Functions'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-685">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c1187-686">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-686">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-687">Müşteri tarafından yönetilen anahtar disk şifrelemesi desteği sunuldu.</span><span class="sxs-lookup"><span data-stu-id="c1187-687">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="c1187-688">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="c1187-688">Az.HealthcareApis</span></span>
* <span data-ttu-id="c1187-689">Erişim ilkeleri artık varsayılan olarak geçerli sorumluyu kullanmıyor</span><span class="sxs-lookup"><span data-stu-id="c1187-689">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c1187-690">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-690">Az.IotHub</span></span>
* <span data-ttu-id="c1187-691">SQL benzeri bir dil kullanarak bilgi almak üzere bir IoT hub’ında sorgu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-691">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="c1187-692">'Add-AzIotHubDevice' cmdlet’inin alt cihaz olmadan Uç Özellikli Cihaz oluşturamaması sorunu düzeltildi [#11597]</span><span class="sxs-lookup"><span data-stu-id="c1187-692">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="c1187-693">IoT hub’ı, cihaz veya modül için SAS belirteci oluşturmak üzere cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-693">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="c1187-694">Yapılandırma ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-694">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="c1187-695">IoT Edge otomatik dağıtımını büyük ölçekte yönetin.</span><span class="sxs-lookup"><span data-stu-id="c1187-695">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="c1187-696">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c1187-696">New cmdlets are:</span></span>
    - <span data-ttu-id="c1187-697">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="c1187-697">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="c1187-698">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="c1187-698">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="c1187-699">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="c1187-699">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="c1187-700">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="c1187-700">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="c1187-701">IoT Edge dağıtım ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-701">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="c1187-702">Yapılandırma içeriğini belirtilen uç cihaza uygulamak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-702">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-703">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-703">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-704">İki diğer ad kaldırıldı: 'New-AzKeyVaultCertificateAdministratorDetails' ve 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="c1187-704">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="c1187-705">Anahtar kasası oluştururken varsayılan olarak geçici silme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-705">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="c1187-706">Ağ kuralları, bir anahtar kasası oluştururken belirli ağ konumlarından erişilebilirliği yönetecek şekilde ayarlanabilir</span><span class="sxs-lookup"><span data-stu-id="c1187-706">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="c1187-707">Kendi anahtarını getir (BYOK) desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-707">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="c1187-708">'Add-AzKeyVaultKey' anahtar değişim anahtarı oluşturmayı destekler</span><span class="sxs-lookup"><span data-stu-id="c1187-708">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="c1187-709">'Get-AzKeyVaultKey' genel bir anahtarı PEM biçiminde indirmeyi destekler</span><span class="sxs-lookup"><span data-stu-id="c1187-709">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="c1187-710">'Add-AzKeyVaultKey' yardım belgesinin 'KeyOps' bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-710">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-711">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-711">Az.Monitor</span></span>
* <span data-ttu-id="c1187-712">'Set-AzDiagnosticSettings' için saklama ilkesinin tüm kategorilere uygulanmadığı hata düzeltildi [#11589]</span><span class="sxs-lookup"><span data-stu-id="c1187-712">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="c1187-713">Ölçüm uyarısı V2 için WebTest kullanılabilirlik ölçütleri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-713">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="c1187-714">'New-AzMetricAlertRuleV2Criteria': Web testi kullanılabilirlik ölçütü oluşturma seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-714">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="c1187-715">'Add-AzMetricAlertRuleV2': Yeni web testi kullanılabilirlik ölçütünü destekler</span><span class="sxs-lookup"><span data-stu-id="c1187-715">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="c1187-716">PSLogProfile içinde RetentionPolicy için gereksiz tanım kaldırıldı [#7608]</span><span class="sxs-lookup"><span data-stu-id="c1187-716">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="c1187-717">PSEventData içinde tanımlanan gereksiz özellikler kaldırıldı [#11353]</span><span class="sxs-lookup"><span data-stu-id="c1187-717">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="c1187-718">'Get-AzLog', 'Get-AzActivityLog' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-718">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-719">Az.Network</span></span>
* <span data-ttu-id="c1187-720">Bölge varsayılan davranışının değiştirileceğini bildirmek için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-720">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="c1187-721">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="c1187-721">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="c1187-722">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="c1187-722">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="c1187-723">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="c1187-723">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="c1187-724">Yeni üst düzey SecurityPartnerProvider kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-724">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="c1187-725">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-725">New cmdlets added:</span></span>
        - <span data-ttu-id="c1187-726">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c1187-726">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="c1187-727">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c1187-727">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="c1187-728">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c1187-728">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="c1187-729">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c1187-729">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="c1187-730">'PSPrivateLinkResource' üzerinde 'RequiredZoneNames' ve 'PSPrivateEndpointConnection' üzerinde 'GroupId' eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-730">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="c1187-731">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject için SuccessThresholdRoundTripTimeMs parametresinin hatalı türü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-731">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="c1187-732">VirtualWan cmdlet’leri AllowVnetToVnetTraffic bağımsız değişkeninin varsayılan değerini True olarak ayarlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-732">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="c1187-733">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="c1187-733">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="c1187-734">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="c1187-734">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="c1187-735">Özel uç nokta için DNS bölgesi grubunu desteklemek amacıyla yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-735">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="c1187-736">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="c1187-736">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="c1187-737">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="c1187-737">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="c1187-738">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="c1187-738">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="c1187-739">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="c1187-739">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="c1187-740">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="c1187-740">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="c1187-741">'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' ve 'DNSServers' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-741">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="c1187-742">'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' ve 'DnsServer' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-742">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="c1187-743">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-743">Updated cmdlet:</span></span>
        - <span data-ttu-id="c1187-744">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c1187-744">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c1187-745">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-745">Az.OperationalInsights</span></span>
* <span data-ttu-id="c1187-746">Yeni oluşturulan SDK’yı uygulamak için eski kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-746">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="c1187-747">Kullanımdan kaldırılan API’ler nedeniyle silinen cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-747">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="c1187-748">'Get-AzOperationalInsightsSavedSearchResult' (diğer adı 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="c1187-748">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="c1187-749">'Get-AzOperationalInsightsSearchResult' (diğer adı 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="c1187-749">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="c1187-750">'Get-AzOperationalInsightsLinkTarget' (diğer adı 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="c1187-750">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="c1187-751">'Set-AzOperationalInsightsWorkspace' ve 'New-AzOperationalInsightsWorkspace' için parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-751">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="c1187-752">Bağlı Depolama Hesabı için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-752">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="c1187-753">Kümeler ve Bağlı Hizmet için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-753">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-754">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-754">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-755">Azure Site Recovery’de Azure’dan Azure’a sağlayıcı için yakın yerleştirilen grup sanal makinelerini korumak üzere destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-755">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="c1187-756">Azure Site Recovery’de bölgeden bölgeye çoğaltma için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-756">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="c1187-757">Azure Backup’ta Azure Dosya Paylaşımı Kurtarma Noktaları için uzun süreli saklama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-757">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="c1187-758">Azure Backup’ta 'Get-AzRecoveryServicesBackupItem' cmdlet’inin çıkışına disk hariç tutma özellikleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-758">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="c1187-759">Site Recovery hizmeti için Kasa kimlik bilgilerine yönelik özel uç noktalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-759">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-760">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-760">Az.Resources</span></span>
* <span data-ttu-id="c1187-761">Yeni bir Rol Tanımı oluşturulurken görüntüleme gecikmesi hakkında ileti uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-761">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="c1187-762">Kesin tür belirtilmiş nesne çıkışı için ilke cmdlet’leri değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-762">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="c1187-763">'Get-AzResourceLock' cmdlet’i üzerinde kullanılan '-TenantLevel' parametresi kaldırıldı [#11335]</span><span class="sxs-lookup"><span data-stu-id="c1187-763">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="c1187-764">'Remove-AzResourceGroup -Id ResourceId' düzeltildi [#9882]</span><span class="sxs-lookup"><span data-stu-id="c1187-764">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="c1187-765">Kaynak grubu kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="c1187-765">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="c1187-766">Abonelik kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="c1187-766">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="c1187-767">Diğer ad: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="c1187-767">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="c1187-768">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' için '-WhatIf' ve '-Confirm' parametreleri ARM şablonu Durum sonuçlarını kullanmak için geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="c1187-768">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="c1187-769">Dağıtım cmdlet’lerinde 'ApiVersion' parametresi için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-769">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="c1187-770">Dağıtım hataları için iyileştirilmiş hata iletilerini gösterme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-770">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="c1187-771">Dağıtım hataları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-771">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="c1187-772">Dağıtım betiği çıkışına 'error' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-772">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="c1187-773">NuGet Microsoft.Azure.Management.ResourceManager '3.7.1-preview' sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-773">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="c1187-774">DeploymentValidateResult içindeki Error özelliği nuget 3.7.1-preview sürümünden itibaren salt okunur olarak değiştirildiğinden belirli test çalışmaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-774">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="c1187-775">SDK ResourceManager 3.7.1-preview sürümünden GenericResourceExpanded öğesi getirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-775">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="c1187-776">Dağıtım için tüm Get cmdlet’lerine yönelik etiket desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-776">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="c1187-777">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="c1187-777">'New-AzDeployment'</span></span>
    - <span data-ttu-id="c1187-778">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="c1187-778">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="c1187-779">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="c1187-779">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="c1187-780">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="c1187-780">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c1187-781">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1187-781">Az.ServiceFabric</span></span>
* <span data-ttu-id="c1187-782">Yanlış sertifika parmak izini alan --SecretIdentifier parametresini kullanarak sertifika ekleme özelliğindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-782">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-783">Az.Sql</span></span>
* <span data-ttu-id="c1187-784">Şunların performansı iyileştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-784">Enhance performance of:</span></span>
    - <span data-ttu-id="c1187-785">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="c1187-785">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="c1187-786">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="c1187-786">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="c1187-787">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="c1187-787">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="c1187-788">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="c1187-788">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="c1187-789">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="c1187-789">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="c1187-790">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="c1187-790">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="c1187-791">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="c1187-791">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="c1187-792">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="c1187-792">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="c1187-793">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’inden 'RetentionDays' parametresinin istemci tarafı doğrulaması kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-793">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="c1187-794">Sanal ağ içindeki bir depolama hesabına denetim yapılarak Depolama Blob Verileri Katkıda Bulunan rolünün oluşturulması sırasında karşılaşılan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-794">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-795">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-795">Az.Storage</span></span>
* <span data-ttu-id="c1187-796">'Get-AzStorageAccount' hesap alma/listeleme cmdlet’ine '-AsJob' eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-796">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="c1187-797">Anahtar otomatik döndürmesini desteklemek için Depolama hesabı KeyvaultEncryption ile güncelleştirilirken KeyVersion isteğe bağlı hale getirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-797">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="c1187-798">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c1187-798">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="c1187-799">İşlem hattıyla Azure Dosya Dizinini kaldırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-799">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="c1187-800">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="c1187-800">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="c1187-801">Düzeltildi [#9880]: NetWorkRule DefaultAction değer tanımı swagger ile uyumlu olacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-801">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="c1187-802">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="c1187-802">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="c1187-803">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="c1187-803">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="c1187-804">Düzeltildi [#11624]: Sunucu hatasından kaçınmak için NetworkRules eklenirken yinelenen kuralları atla</span><span class="sxs-lookup"><span data-stu-id="c1187-804">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="c1187-805">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="c1187-805">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="c1187-806">Microsoft.Azure.Cosmos.Table SDK 1.0.7 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-806">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="c1187-807">DataLake 2. Nesil Öğeleri listesinde yalnızca bazı öğeler döndürüldüğünde kullanıcıya ContinuationToken ile yeniden listelemesini anımsatmak için uyarı iletisi eklendi,</span><span class="sxs-lookup"><span data-stu-id="c1187-807">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="c1187-808">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="c1187-808">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="c1187-809">Azure Dosyalar Active Directory Domain Services Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-809">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="c1187-810">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c1187-810">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="c1187-811">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c1187-811">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="c1187-812">Depolama hesabının Kerberos anahtarlarını yeni oluşturma veya listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-812">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="c1187-813">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="c1187-813">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="c1187-814">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="c1187-814">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="c1187-815">Yük devretme Depolama hesabı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-815">Supported failover Storage account</span></span>
    - <span data-ttu-id="c1187-816">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="c1187-816">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="c1187-817">'Get-AzStorageBlobCopyState' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-817">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="c1187-818">'Get-AzStorageFileCopyState' ve 'Start-AzStorageBlobCopy' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-818">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="c1187-819">Depolama istemci kitaplığı v12, Kuyruk ve Dosya cmdlet’leriyle tümleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-819">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="c1187-820">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="c1187-820">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="c1187-821">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="c1187-821">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="c1187-822">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="c1187-822">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="c1187-823">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="c1187-823">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="c1187-824">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="c1187-824">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="c1187-825">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="c1187-825">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="c1187-826">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="c1187-826">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="c1187-827">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="c1187-827">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="c1187-828">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="c1187-828">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="c1187-829">CloudFileShare olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="c1187-829">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="c1187-830">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="c1187-830">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="c1187-831">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="c1187-831">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="c1187-832">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="c1187-832">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="c1187-833">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="c1187-833">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="c1187-834">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="c1187-834">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="c1187-835">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c1187-835">Az.TrafficManager</span></span>
* <span data-ttu-id="c1187-836">'DisableAzureTrafficManagerEndpoint' ayrıntılı çıkışındaki hatalı profil adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-836">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-837">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-837">Az.Websites</span></span>
* <span data-ttu-id="c1187-838">'Update-AzWebAppAccessRestrictionConfig' yardımındaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-838">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="c1187-839">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-839">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="c1187-840">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="c1187-840">Highlights since the last release</span></span>
* <span data-ttu-id="c1187-841">Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="c1187-841">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c1187-842">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-842">Az.Accounts</span></span>
* <span data-ttu-id="c1187-843">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="c1187-843">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c1187-844">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-844">Az.ApiManagement</span></span>
* <span data-ttu-id="c1187-845">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-845">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="c1187-846">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-846">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c1187-847">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c1187-847">Az.Cdn</span></span>
* <span data-ttu-id="c1187-848">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-848">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c1187-849">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1187-849">Az.CognitiveServices</span></span>
* <span data-ttu-id="c1187-850">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="c1187-850">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-851">Az.Compute</span></span>
* <span data-ttu-id="c1187-852">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-852">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="c1187-853">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-853">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c1187-854">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-854">Az.IotHub</span></span>
* <span data-ttu-id="c1187-855">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c1187-855">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="c1187-856">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="c1187-856">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="c1187-857">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="c1187-857">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="c1187-858">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-858">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="c1187-859">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c1187-859">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="c1187-860">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="c1187-860">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="c1187-861">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="c1187-861">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="c1187-862">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="c1187-862">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="c1187-863">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c1187-863">New cmdlets are:</span></span>
    - <span data-ttu-id="c1187-864">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c1187-864">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="c1187-865">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c1187-865">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="c1187-866">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c1187-866">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="c1187-867">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c1187-867">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="c1187-868">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-868">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-869">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-869">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-870">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-870">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="c1187-871">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="c1187-871">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="c1187-872">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="c1187-872">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="c1187-873">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-873">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="c1187-874">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="c1187-874">Az.Maintenance</span></span>
* <span data-ttu-id="c1187-875">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="c1187-875">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-876">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-876">Az.Monitor</span></span>
* <span data-ttu-id="c1187-877">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-877">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="c1187-878">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="c1187-878">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="c1187-879">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="c1187-879">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="c1187-880">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="c1187-880">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="c1187-881">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="c1187-881">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="c1187-882">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="c1187-882">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="c1187-883">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="c1187-883">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="c1187-884">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="c1187-884">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-885">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-885">Az.Network</span></span>
* <span data-ttu-id="c1187-886">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-886">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="c1187-887">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="c1187-887">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="c1187-888">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="c1187-888">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="c1187-889">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="c1187-889">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="c1187-890">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="c1187-890">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="c1187-891">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-891">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="c1187-892">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="c1187-892">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="c1187-893">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="c1187-893">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="c1187-894">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-894">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="c1187-895">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-895">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="c1187-896">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="c1187-896">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="c1187-897">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-897">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="c1187-898">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-898">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="c1187-899">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-899">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="c1187-900">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-900">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="c1187-901">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-901">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c1187-902">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-902">Az.PolicyInsights</span></span>
* <span data-ttu-id="c1187-903">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-903">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="c1187-904">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-904">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c1187-905">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1187-905">Az.ServiceFabric</span></span>
* <span data-ttu-id="c1187-906">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-906">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-907">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-907">Az.Sql</span></span>
* <span data-ttu-id="c1187-908">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-908">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="c1187-909">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-909">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-910">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-910">Az.Storage</span></span>
* <span data-ttu-id="c1187-911">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-911">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="c1187-912">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-912">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="c1187-913">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c1187-913">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="c1187-914">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c1187-914">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="c1187-915">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-915">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="c1187-916">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="c1187-916">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="c1187-917">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="c1187-917">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="c1187-918">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="c1187-918">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="c1187-919">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="c1187-919">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="c1187-920">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="c1187-920">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="c1187-921">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="c1187-921">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="c1187-922">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="c1187-922">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="c1187-923">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="c1187-923">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="c1187-924">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-924">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="c1187-925">Genel</span><span class="sxs-lookup"><span data-stu-id="c1187-925">General</span></span>
* <span data-ttu-id="c1187-926">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c1187-926">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="c1187-927">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="c1187-927">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="c1187-928">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c1187-928">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="c1187-929">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="c1187-929">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="c1187-930">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c1187-930">Az.Billing</span></span>
  - <span data-ttu-id="c1187-931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-931">Az.Compute</span></span>
  - <span data-ttu-id="c1187-932">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="c1187-932">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="c1187-933">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1187-933">Az.EventHub</span></span>
  - <span data-ttu-id="c1187-934">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-934">Az.IotHub</span></span>
  - <span data-ttu-id="c1187-935">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-935">Az.KeyVault</span></span>
  - <span data-ttu-id="c1187-936">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-936">Az.Monitor</span></span>
  - <span data-ttu-id="c1187-937">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-937">Az.Network</span></span>
  - <span data-ttu-id="c1187-938">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-938">Az.Resources</span></span>
  - <span data-ttu-id="c1187-939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-939">Az.Storage</span></span>
  - <span data-ttu-id="c1187-940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-940">Az.Websites</span></span>
* <span data-ttu-id="c1187-941">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-941">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="c1187-942">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="c1187-942">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="c1187-943">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](https://aka.ms/InstallASHPowerShell) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="c1187-943">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="c1187-944">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-944">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-945">Az.Accounts</span></span>
* <span data-ttu-id="c1187-946">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="c1187-946">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-947">Az.Compute</span></span>
* <span data-ttu-id="c1187-948">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-948">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="c1187-949">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="c1187-949">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="c1187-950">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-950">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="c1187-951">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-951">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="c1187-952">[#11354]</span><span class="sxs-lookup"><span data-stu-id="c1187-952">[#11354]</span></span>
* <span data-ttu-id="c1187-953">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-953">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="c1187-954">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="c1187-954">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="c1187-955">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="c1187-955">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="c1187-956">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="c1187-956">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="c1187-957">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="c1187-957">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="c1187-958">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-958">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="c1187-959">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-959">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="c1187-960">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-960">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="c1187-961">[#11257]</span><span class="sxs-lookup"><span data-stu-id="c1187-961">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-962">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-962">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-963">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-963">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="c1187-964">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-964">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-965">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-965">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-966">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-966">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="c1187-967">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-967">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c1187-968">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-968">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-969">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-969">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c1187-970">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-970">Az.IotHub</span></span>
* <span data-ttu-id="c1187-971">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-971">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="c1187-972">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c1187-972">New Cmdlets are:</span></span>
    - <span data-ttu-id="c1187-973">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="c1187-973">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="c1187-974">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="c1187-974">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-975">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-975">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-976">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-976">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-977">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-977">Az.Monitor</span></span>
* <span data-ttu-id="c1187-978">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-978">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-979">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-979">Az.Network</span></span>
* <span data-ttu-id="c1187-980">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-980">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="c1187-981">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="c1187-981">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="c1187-982">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="c1187-982">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="c1187-983">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="c1187-983">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="c1187-984">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="c1187-984">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="c1187-985">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-985">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c1187-986">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-986">Az.PolicyInsights</span></span>
* <span data-ttu-id="c1187-987">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-987">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-988">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-988">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-989">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-989">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="c1187-990">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-990">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="c1187-991">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-991">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="c1187-992">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-992">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="c1187-993">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-993">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="c1187-994">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-994">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-995">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-995">Az.Resources</span></span>
* <span data-ttu-id="c1187-996">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="c1187-996">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="c1187-997">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-997">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="c1187-998">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-998">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="c1187-999">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-999">Added example.</span></span>
* <span data-ttu-id="c1187-1000">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="c1187-1000">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="c1187-1001">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="c1187-1001">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1002">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1002">Az.Sql</span></span>
* <span data-ttu-id="c1187-1003">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1003">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="c1187-1004">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1004">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="c1187-1005">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1005">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="c1187-1006">Az.Support</span><span class="sxs-lookup"><span data-stu-id="c1187-1006">Az.Support</span></span>
* <span data-ttu-id="c1187-1007">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-1007">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-1008">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-1008">Az.Websites</span></span>
* <span data-ttu-id="c1187-1009">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1009">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="c1187-1010">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="c1187-1010">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="c1187-1011">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="c1187-1011">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="c1187-1012">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="c1187-1012">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="c1187-1013">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="c1187-1013">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="c1187-1014">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-1014">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-1015">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-1015">Az.Accounts</span></span>
* <span data-ttu-id="c1187-1016">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="c1187-1016">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="c1187-1017">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="c1187-1017">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="c1187-1018">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1018">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c1187-1019">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-1019">Az.ApiManagement</span></span>
* <span data-ttu-id="c1187-1020">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="c1187-1020">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="c1187-1021">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="c1187-1021">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="c1187-1022">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1022">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="c1187-1023">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="c1187-1023">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-1024">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-1024">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-1025">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1025">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c1187-1026">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-1026">Az.IotHub</span></span>
* <span data-ttu-id="c1187-1027">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1027">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="c1187-1028">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c1187-1028">New Cmdlets are:</span></span>
    - <span data-ttu-id="c1187-1029">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c1187-1029">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="c1187-1030">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c1187-1030">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="c1187-1031">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c1187-1031">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="c1187-1032">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c1187-1032">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="c1187-1033">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1033">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="c1187-1034">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c1187-1034">New Cmdlets are:</span></span>
    - <span data-ttu-id="c1187-1035">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="c1187-1035">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="c1187-1036">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="c1187-1036">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="c1187-1037">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="c1187-1037">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="c1187-1038">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="c1187-1038">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="c1187-1039">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1039">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="c1187-1040">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1040">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="c1187-1041">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1041">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="c1187-1042">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c1187-1042">New Cmdlets are:</span></span>
    - <span data-ttu-id="c1187-1043">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="c1187-1043">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="c1187-1044">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="c1187-1044">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="c1187-1045">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1045">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-1046">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-1046">Az.Monitor</span></span>
* <span data-ttu-id="c1187-1047">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="c1187-1047">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-1048">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-1048">Az.Network</span></span>
* <span data-ttu-id="c1187-1049">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1049">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="c1187-1050">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1050">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="c1187-1051">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1051">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="c1187-1052">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1052">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-1053">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-1053">Az.Resources</span></span>
* <span data-ttu-id="c1187-1054">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1054">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="c1187-1055">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="c1187-1055">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="c1187-1056">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="c1187-1056">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="c1187-1057">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="c1187-1057">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="c1187-1058">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1058">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="c1187-1059">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1059">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="c1187-1060">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1060">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="c1187-1061">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1061">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="c1187-1062">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1187-1062">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="c1187-1063">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1187-1063">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="c1187-1064">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1187-1064">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="c1187-1065">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1065">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="c1187-1066">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1187-1066">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="c1187-1067">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1067">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1068">Az.Sql</span></span>
* <span data-ttu-id="c1187-1069">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1069">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="c1187-1070">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1070">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="c1187-1071">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="c1187-1071">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="c1187-1072">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="c1187-1072">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="c1187-1073">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1187-1073">Remove an LTR backup</span></span>
    - <span data-ttu-id="c1187-1074">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="c1187-1074">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="c1187-1075">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1075">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="c1187-1076">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1076">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="c1187-1077">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-1077">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-1078">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-1078">Az.Storage</span></span>
* <span data-ttu-id="c1187-1079">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1079">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="c1187-1080">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="c1187-1080">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="c1187-1081">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1081">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="c1187-1082">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="c1187-1082">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="c1187-1083">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="c1187-1083">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-1084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-1084">Az.Websites</span></span>
* <span data-ttu-id="c1187-1085">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1085">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="c1187-1086">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="c1187-1086">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="c1187-1087">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1087">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="c1187-1088">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="c1187-1088">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="c1187-1089">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1089">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="c1187-1090">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-1090">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c1187-1091">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="c1187-1091">Highlights since the last major release</span></span>
* <span data-ttu-id="c1187-1092">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1092">Updated client side telemetry.</span></span>
* <span data-ttu-id="c1187-1093">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1093">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="c1187-1094">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1094">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c1187-1095">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-1095">Az.Accounts</span></span>
* <span data-ttu-id="c1187-1096">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1096">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-1097">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-1097">Az.Automation</span></span>
* <span data-ttu-id="c1187-1098">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1098">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c1187-1099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1187-1099">Az.CognitiveServices</span></span>
* <span data-ttu-id="c1187-1100">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1100">Updated SDK to 7.0</span></span>
* <span data-ttu-id="c1187-1101">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1101">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-1102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-1102">Az.Compute</span></span>
* <span data-ttu-id="c1187-1103">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1103">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c1187-1104">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c1187-1104">Az.FrontDoor</span></span>
* <span data-ttu-id="c1187-1105">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1105">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c1187-1106">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-1106">Az.IotHub</span></span>
* <span data-ttu-id="c1187-1107">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1107">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="c1187-1108">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c1187-1108">New Cmdlets are:</span></span>
    - <span data-ttu-id="c1187-1109">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c1187-1109">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="c1187-1110">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c1187-1110">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="c1187-1111">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c1187-1111">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="c1187-1112">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c1187-1112">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-1113">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-1113">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-1114">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1114">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-1115">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-1115">Az.Monitor</span></span>
* <span data-ttu-id="c1187-1116">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1116">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="c1187-1117">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1117">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="c1187-1118">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="c1187-1118">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-1119">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-1119">Az.Network</span></span>
* <span data-ttu-id="c1187-1120">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1120">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="c1187-1121">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1121">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="c1187-1122">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1122">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="c1187-1123">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="c1187-1123">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="c1187-1124">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1124">No new cmdlets are added.</span></span> <span data-ttu-id="c1187-1125">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="c1187-1125">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-1126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-1126">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-1127">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1127">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-1128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-1128">Az.Resources</span></span>
* <span data-ttu-id="c1187-1129">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1129">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="c1187-1130">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c1187-1130">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="c1187-1131">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="c1187-1131">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="c1187-1132">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1132">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="c1187-1133">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-1133">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="c1187-1134">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1134">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="c1187-1135">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1135">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="c1187-1136">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-1136">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1137">Az.Sql</span></span>
* <span data-ttu-id="c1187-1138">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1138">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="c1187-1139">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1139">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="c1187-1140">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="c1187-1140">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="c1187-1141">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c1187-1141">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="c1187-1142">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1142">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c1187-1143">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c1187-1143">Az.StorageSync</span></span>
* <span data-ttu-id="c1187-1144">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1144">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="c1187-1145">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-1145">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c1187-1146">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="c1187-1146">Highlights since the last major release</span></span>
* <span data-ttu-id="c1187-1147">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="c1187-1147">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="c1187-1148">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1148">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c1187-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-1149">Az.Accounts</span></span>
* <span data-ttu-id="c1187-1150">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="c1187-1150">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="c1187-1151">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1151">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c1187-1152">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-1152">Az.ApiManagement</span></span>
* <span data-ttu-id="c1187-1153">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="c1187-1153">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="c1187-1154">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="c1187-1154">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="c1187-1155">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1155">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="c1187-1156">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1156">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-1157">Az.Compute</span></span>
* <span data-ttu-id="c1187-1158">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="c1187-1158">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="c1187-1159">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1159">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="c1187-1160">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1160">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="c1187-1161">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-1161">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="c1187-1162">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1162">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-1163">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-1163">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-1164">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1164">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="c1187-1165">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="c1187-1165">Az.DeploymentManager</span></span>
* <span data-ttu-id="c1187-1166">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="c1187-1166">Adds LIST operations for resources</span></span>
* <span data-ttu-id="c1187-1167">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="c1187-1167">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c1187-1168">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-1168">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-1169">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1169">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-1170">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-1170">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-1171">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1171">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-1172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-1172">Az.Network</span></span>
* <span data-ttu-id="c1187-1173">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1173">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="c1187-1174">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="c1187-1174">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="c1187-1175">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1175">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="c1187-1176">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1176">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="c1187-1177">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="c1187-1177">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="c1187-1178">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1178">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="c1187-1179">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1179">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="c1187-1180">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1180">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="c1187-1181">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1181">New cmdlets added:</span></span>
        - <span data-ttu-id="c1187-1182">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1187-1182">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="c1187-1183">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1183">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="c1187-1184">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c1187-1184">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="c1187-1185">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1185">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c1187-1186">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-1186">Az.PolicyInsights</span></span>
* <span data-ttu-id="c1187-1187">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="c1187-1187">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="c1187-1188">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1188">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="c1187-1189">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1189">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="c1187-1190">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1190">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-1191">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-1191">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-1192">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1192">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="c1187-1193">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1193">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-1194">Az.Resources</span></span>
* <span data-ttu-id="c1187-1195">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-1195">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="c1187-1196">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1196">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1197">Az.Sql</span></span>
<span data-ttu-id="c1187-1198">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1198">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-1199">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-1199">Az.Storage</span></span>
* <span data-ttu-id="c1187-1200">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="c1187-1200">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="c1187-1201">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-1201">New-AzStorageAccount</span></span>
* <span data-ttu-id="c1187-1202">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="c1187-1202">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="c1187-1203">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1203">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-1204">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-1204">Az.Websites</span></span>
* <span data-ttu-id="c1187-1205">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="c1187-1205">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="c1187-1206">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1206">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="c1187-1207">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="c1187-1207">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-1208">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-1208">Az.Accounts</span></span>
* <span data-ttu-id="c1187-1209">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1209">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c1187-1210">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c1187-1210">Az.Cdn</span></span>
* <span data-ttu-id="c1187-1211">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="c1187-1211">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-1212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-1212">Az.Compute</span></span>
* <span data-ttu-id="c1187-1213">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1213">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="c1187-1214">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c1187-1214">Az.ContainerInstance</span></span>
* <span data-ttu-id="c1187-1215">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1215">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="c1187-1216">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="c1187-1216">Az.DataBoxEdge</span></span>
* <span data-ttu-id="c1187-1217">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1217">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="c1187-1218">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="c1187-1218">Get the Edge Storage Container</span></span>
* <span data-ttu-id="c1187-1219">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1219">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="c1187-1220">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c1187-1220">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="c1187-1221">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1221">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="c1187-1222">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1187-1222">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="c1187-1223">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1223">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="c1187-1224">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="c1187-1224">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="c1187-1225">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1225">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="c1187-1226">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="c1187-1226">Get the Edge Storage Account</span></span>
* <span data-ttu-id="c1187-1227">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1227">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="c1187-1228">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="c1187-1228">Create new Edge Storage Account</span></span>
* <span data-ttu-id="c1187-1229">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1229">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="c1187-1230">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1187-1230">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="c1187-1231">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="c1187-1231">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="c1187-1232">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="c1187-1232">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="c1187-1233">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1233">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="c1187-1234">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c1187-1234">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-1235">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-1235">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-1236">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1236">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="c1187-1237">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1237">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="c1187-1238">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1238">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="c1187-1239">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="c1187-1239">Az.DevTestLabs</span></span>
* <span data-ttu-id="c1187-1240">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-1240">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c1187-1241">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1187-1241">Az.EventHub</span></span>
* <span data-ttu-id="c1187-1242">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1242">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c1187-1243">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-1243">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-1244">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1244">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="c1187-1245">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c1187-1245">Az.MachineLearning</span></span>
* <span data-ttu-id="c1187-1246">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-1246">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="c1187-1247">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c1187-1247">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="c1187-1248">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="c1187-1248">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="c1187-1249">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c1187-1249">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="c1187-1250">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c1187-1250">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="c1187-1251">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c1187-1251">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="c1187-1252">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="c1187-1252">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="c1187-1253">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="c1187-1253">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-1254">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-1254">Az.Network</span></span>
* <span data-ttu-id="c1187-1255">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1255">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-1256">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-1256">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-1257">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1257">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="c1187-1258">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1258">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="c1187-1259">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1259">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="c1187-1260">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1260">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-1261">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-1261">Az.Resources</span></span>
* <span data-ttu-id="c1187-1262">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1262">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1263">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1263">Az.Sql</span></span>
* <span data-ttu-id="c1187-1264">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1264">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="c1187-1265">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1265">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="c1187-1266">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c1187-1266">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="c1187-1267">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1267">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-1268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-1268">Az.Storage</span></span>
* <span data-ttu-id="c1187-1269">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1269">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="c1187-1270">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1187-1270">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="c1187-1271">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="c1187-1271">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="c1187-1272">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-1272">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="c1187-1273">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-1273">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="c1187-1274">Genel</span><span class="sxs-lookup"><span data-stu-id="c1187-1274">General</span></span>
* <span data-ttu-id="c1187-1275">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1275">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c1187-1276">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-1276">Az.Accounts</span></span>
* <span data-ttu-id="c1187-1277">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="c1187-1277">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="c1187-1278">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="c1187-1278">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c1187-1279">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c1187-1279">Az.Batch</span></span>
* <span data-ttu-id="c1187-1280">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1280">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-1281">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-1281">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-1282">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1282">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c1187-1283">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c1187-1283">Az.FrontDoor</span></span>
* <span data-ttu-id="c1187-1284">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1284">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="c1187-1285">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1285">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="c1187-1286">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="c1187-1286">Az.HealthcareApis</span></span>
* <span data-ttu-id="c1187-1287">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="c1187-1287">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-1288">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-1289">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1289">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="c1187-1290">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="c1187-1290">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="c1187-1291">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1291">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-1292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-1292">Az.Monitor</span></span>
* <span data-ttu-id="c1187-1293">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1293">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="c1187-1294">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="c1187-1294">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="c1187-1295">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="c1187-1295">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-1296">Az.Network</span></span>
* <span data-ttu-id="c1187-1297">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1297">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-1298">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-1298">Az.Resources</span></span>
* <span data-ttu-id="c1187-1299">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1299">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="c1187-1300">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1300">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1301">Az.Sql</span></span>
* <span data-ttu-id="c1187-1302">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1302">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-1303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-1303">Az.Storage</span></span>
* <span data-ttu-id="c1187-1304">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="c1187-1304">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="c1187-1305">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="c1187-1305">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="c1187-1306">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c1187-1306">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="c1187-1307">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="c1187-1307">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="c1187-1308">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="c1187-1308">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="c1187-1309">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1309">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="c1187-1310">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1310">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="c1187-1311">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c1187-1311">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="c1187-1312">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c1187-1312">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="c1187-1313">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1313">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="c1187-1314">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="c1187-1314">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="c1187-1315">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1315">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="c1187-1316">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="c1187-1316">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="c1187-1317">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-1317">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c1187-1318">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="c1187-1318">Highlights since the last major release</span></span>
* <span data-ttu-id="c1187-1319">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="c1187-1319">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="c1187-1320">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="c1187-1320">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-1321">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-1321">Az.Compute</span></span>
* <span data-ttu-id="c1187-1322">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="c1187-1322">VM Reapply feature</span></span>
    - <span data-ttu-id="c1187-1323">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="c1187-1323">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="c1187-1324">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="c1187-1324">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="c1187-1325">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c1187-1325">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="c1187-1326">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="c1187-1326">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="c1187-1327">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1327">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="c1187-1328">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1328">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="c1187-1329">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1329">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="c1187-1330">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1330">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="c1187-1331">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1331">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="c1187-1332">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1332">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="c1187-1333">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="c1187-1333">Az.DataBoxEdge</span></span>
* <span data-ttu-id="c1187-1334">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1334">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="c1187-1335">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="c1187-1335">Get the Order</span></span>
* <span data-ttu-id="c1187-1336">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1336">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="c1187-1337">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="c1187-1337">Create new Order</span></span>
* <span data-ttu-id="c1187-1338">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1338">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="c1187-1339">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="c1187-1339">Remove the Order</span></span>
* <span data-ttu-id="c1187-1340">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="c1187-1340">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="c1187-1341">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="c1187-1341">Now creates Local Share</span></span>
* <span data-ttu-id="c1187-1342">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1342">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="c1187-1343">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="c1187-1343">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="c1187-1344">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1344">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="c1187-1345">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="c1187-1345">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="c1187-1346">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1346">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="c1187-1347">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="c1187-1347">Gets the information about Triggers</span></span>
* <span data-ttu-id="c1187-1348">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1348">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="c1187-1349">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="c1187-1349">Create new Triggers</span></span>
* <span data-ttu-id="c1187-1350">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1350">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="c1187-1351">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="c1187-1351">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-1352">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-1352">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-1353">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1353">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="c1187-1354">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1354">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-1355">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-1355">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-1356">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1356">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c1187-1357">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1187-1357">Az.EventHub</span></span>
* <span data-ttu-id="c1187-1358">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1358">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c1187-1359">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c1187-1359">Az.FrontDoor</span></span>
* <span data-ttu-id="c1187-1360">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1360">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="c1187-1361">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1361">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="c1187-1362">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1362">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="c1187-1363">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="c1187-1363">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-1364">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-1364">Az.Network</span></span>
* <span data-ttu-id="c1187-1365">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1365">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="c1187-1366">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="c1187-1366">Az.PrivateDns</span></span>
* <span data-ttu-id="c1187-1367">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1367">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-1368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-1368">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-1369">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1369">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="c1187-1370">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1370">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="c1187-1371">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1371">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c1187-1372">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c1187-1372">Az.RedisCache</span></span>
* <span data-ttu-id="c1187-1373">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1373">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="c1187-1374">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1374">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="c1187-1375">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1375">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-1376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-1376">Az.Resources</span></span>
- <span data-ttu-id="c1187-1377">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1377">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="c1187-1378">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1378">Updated create policy definition help example</span></span>
- <span data-ttu-id="c1187-1379">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1379">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="c1187-1380">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1380">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="c1187-1381">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1381">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1382">Az.Sql</span></span>
* <span data-ttu-id="c1187-1383">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1383">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="c1187-1384">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1384">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="c1187-1385">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-1385">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="c1187-1386">Genel</span><span class="sxs-lookup"><span data-stu-id="c1187-1386">General</span></span>
* <span data-ttu-id="c1187-1387">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="c1187-1387">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c1187-1388">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-1388">Az.Accounts</span></span>
* <span data-ttu-id="c1187-1389">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c1187-1389">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="c1187-1390">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="c1187-1390">Az.Advisor</span></span>
* <span data-ttu-id="c1187-1391">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1391">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c1187-1392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c1187-1392">Az.Batch</span></span>
* <span data-ttu-id="c1187-1393">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1393">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="c1187-1394">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="c1187-1394">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="c1187-1395">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1395">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="c1187-1396">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1396">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="c1187-1397">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="c1187-1397">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="c1187-1398">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c1187-1398">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="c1187-1399">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="c1187-1399">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="c1187-1400">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1400">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="c1187-1401">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1401">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="c1187-1402">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1402">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="c1187-1403">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="c1187-1403">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="c1187-1404">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="c1187-1404">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="c1187-1405">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1405">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="c1187-1406">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="c1187-1406">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="c1187-1407">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1407">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="c1187-1408">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1408">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="c1187-1409">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1409">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="c1187-1410">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1410">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="c1187-1411">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1411">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="c1187-1412">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1412">This operation is no longer supported.</span></span>
* <span data-ttu-id="c1187-1413">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1413">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="c1187-1414">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1414">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="c1187-1415">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1415">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="c1187-1416">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1416">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="c1187-1417">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1417">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="c1187-1418">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1418">New non-verified images are also now returned.</span></span> <span data-ttu-id="c1187-1419">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1419">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="c1187-1420">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1420">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="c1187-1421">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1421">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="c1187-1422">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1422">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="c1187-1423">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1423">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="c1187-1424">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1424">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="c1187-1425">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1425">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="c1187-1426">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1426">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="c1187-1427">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="c1187-1427">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="c1187-1428">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="c1187-1428">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c1187-1429">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c1187-1429">Az.Cdn</span></span>
* <span data-ttu-id="c1187-1430">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1430">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="c1187-1431">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1431">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-1432">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-1432">Az.Compute</span></span>
* <span data-ttu-id="c1187-1433">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="c1187-1433">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="c1187-1434">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c1187-1434">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="c1187-1435">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c1187-1435">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="c1187-1436">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-1436">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="c1187-1437">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1437">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="c1187-1438">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="c1187-1438">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="c1187-1439">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1439">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="c1187-1440">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c1187-1440">Breaking changes</span></span>
    - <span data-ttu-id="c1187-1441">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="c1187-1441">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="c1187-1442">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="c1187-1442">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-1443">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-1443">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-1444">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1444">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-1445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-1445">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-1446">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="c1187-1446">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="c1187-1447">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="c1187-1447">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="c1187-1448">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="c1187-1448">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="c1187-1449">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="c1187-1449">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="c1187-1450">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="c1187-1450">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="c1187-1451">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="c1187-1451">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c1187-1452">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c1187-1452">Az.FrontDoor</span></span>
* <span data-ttu-id="c1187-1453">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1453">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c1187-1454">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-1454">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-1455">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1455">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="c1187-1456">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1456">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="c1187-1457">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1457">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="c1187-1458">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="c1187-1458">Removed five cmdlets:</span></span>
    - <span data-ttu-id="c1187-1459">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="c1187-1459">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="c1187-1460">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="c1187-1460">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="c1187-1461">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="c1187-1461">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="c1187-1462">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c1187-1462">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="c1187-1463">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c1187-1463">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="c1187-1464">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1464">Added three cmdlets:</span></span>
    - <span data-ttu-id="c1187-1465">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="c1187-1465">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="c1187-1466">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="c1187-1466">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="c1187-1467">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="c1187-1467">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="c1187-1468">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1468">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="c1187-1469">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1469">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="c1187-1470">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1470">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="c1187-1471">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1471">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="c1187-1472">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1472">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="c1187-1473">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1473">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="c1187-1474">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1474">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="c1187-1475">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1475">Added some scenario test cases.</span></span>
* <span data-ttu-id="c1187-1476">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="c1187-1476">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c1187-1477">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-1477">Az.IotHub</span></span>
* <span data-ttu-id="c1187-1478">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="c1187-1478">Breaking changes:</span></span>
    - <span data-ttu-id="c1187-1479">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1479">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="c1187-1480">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1480">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="c1187-1481">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1481">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="c1187-1482">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1482">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="c1187-1483">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1483">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="c1187-1484">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1484">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="c1187-1485">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1485">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="c1187-1486">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1486">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="c1187-1487">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1487">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="c1187-1488">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1488">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="c1187-1489">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1489">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="c1187-1490">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1490">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-1491">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-1491">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-1492">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1492">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="c1187-1493">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1493">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="c1187-1494">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1494">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="c1187-1495">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1495">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="c1187-1496">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1496">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="c1187-1497">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1497">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="c1187-1498">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1498">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="c1187-1499">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1499">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="c1187-1500">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1500">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-1501">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-1501">Az.Resources</span></span>
* <span data-ttu-id="c1187-1502">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1502">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-1503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-1503">Az.Network</span></span>
* <span data-ttu-id="c1187-1504">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1504">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="c1187-1505">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1505">Updated cmdlet:</span></span>
        - <span data-ttu-id="c1187-1506">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1506">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c1187-1507">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1507">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c1187-1508">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1508">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c1187-1509">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1509">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c1187-1510">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1510">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="c1187-1511">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1511">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="c1187-1512">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c1187-1512">New cmdlet:</span></span>
        - <span data-ttu-id="c1187-1513">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="c1187-1513">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="c1187-1514">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1514">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="c1187-1515">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1515">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="c1187-1516">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1516">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="c1187-1517">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1517">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="c1187-1518">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1518">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="c1187-1519">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1519">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="c1187-1520">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1520">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="c1187-1521">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1521">New cmdlets added:</span></span>
        - <span data-ttu-id="c1187-1522">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="c1187-1522">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="c1187-1523">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1187-1523">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="c1187-1524">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1187-1524">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="c1187-1525">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1187-1525">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="c1187-1526">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c1187-1526">Set-AzVirtualHub</span></span>
* <span data-ttu-id="c1187-1527">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1527">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="c1187-1528">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1528">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="c1187-1529">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1529">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="c1187-1530">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1530">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="c1187-1531">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1531">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="c1187-1532">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1532">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="c1187-1533">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1533">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="c1187-1534">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1534">New cmdlets added:</span></span>
        - <span data-ttu-id="c1187-1535">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1535">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="c1187-1536">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1536">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="c1187-1537">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1537">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="c1187-1538">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1538">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="c1187-1539">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1539">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="c1187-1540">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1540">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="c1187-1541">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1541">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="c1187-1542">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1542">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="c1187-1543">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1543">New cmdlets added:</span></span>
        - <span data-ttu-id="c1187-1544">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="c1187-1544">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="c1187-1545">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="c1187-1545">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="c1187-1546">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="c1187-1546">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="c1187-1547">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="c1187-1547">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="c1187-1548">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="c1187-1548">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="c1187-1549">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1187-1549">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="c1187-1550">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1550">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="c1187-1551">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1551">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="c1187-1552">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1552">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="c1187-1553">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1553">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="c1187-1554">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1554">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="c1187-1555">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1555">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="c1187-1556">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1556">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="c1187-1557">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1557">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="c1187-1558">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1558">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="c1187-1559">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="c1187-1559">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="c1187-1560">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1560">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="c1187-1561">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1561">New cmdlets added:</span></span>
        - <span data-ttu-id="c1187-1562">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c1187-1562">New-AzIpGroup</span></span>
        - <span data-ttu-id="c1187-1563">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c1187-1563">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="c1187-1564">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c1187-1564">Get-AzIpGroup</span></span>
        - <span data-ttu-id="c1187-1565">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c1187-1565">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c1187-1566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1187-1566">Az.ServiceFabric</span></span>
* <span data-ttu-id="c1187-1567">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1567">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1568">Az.Sql</span></span>
* <span data-ttu-id="c1187-1569">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1569">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="c1187-1570">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1570">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="c1187-1571">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="c1187-1571">Removed deprecated aliases:</span></span>
* <span data-ttu-id="c1187-1572">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="c1187-1572">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="c1187-1573">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="c1187-1573">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="c1187-1574">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-1574">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="c1187-1575">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-1575">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="c1187-1576">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-1576">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="c1187-1577">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1577">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-1578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-1578">Az.Storage</span></span>
* <span data-ttu-id="c1187-1579">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="c1187-1579">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="c1187-1580">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-1580">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="c1187-1581">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-1581">Set-AzStorageAccount</span></span>
* <span data-ttu-id="c1187-1582">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="c1187-1582">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="c1187-1583">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c1187-1583">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="c1187-1584">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c1187-1584">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="c1187-1585">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-1585">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="c1187-1586">Genel</span><span class="sxs-lookup"><span data-stu-id="c1187-1586">General</span></span>
* <span data-ttu-id="c1187-1587">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="c1187-1587">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c1187-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-1588">Az.Accounts</span></span>
* <span data-ttu-id="c1187-1589">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1589">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c1187-1590">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-1590">Az.ApiManagement</span></span>
* <span data-ttu-id="c1187-1591">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1591">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="c1187-1592">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1592">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-1593">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-1593">Az.Automation</span></span>
* <span data-ttu-id="c1187-1594">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1594">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c1187-1595">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c1187-1595">Az.Batch</span></span>
* <span data-ttu-id="c1187-1596">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="c1187-1596">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-1597">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-1597">Az.Compute</span></span>
* <span data-ttu-id="c1187-1598">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1598">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="c1187-1599">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1599">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="c1187-1600">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1600">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="c1187-1601">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1601">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-1602">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-1602">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-1603">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="c1187-1603">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="c1187-1604">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="c1187-1604">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="c1187-1605">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1605">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-1606">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-1606">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-1607">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1607">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="c1187-1608">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="c1187-1608">Az.HealthcareApis</span></span>
* <span data-ttu-id="c1187-1609">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1609">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="c1187-1610">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1610">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="c1187-1611">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1611">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="c1187-1612">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1612">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c1187-1613">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-1613">Az.IotHub</span></span>
* <span data-ttu-id="c1187-1614">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="c1187-1614">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="c1187-1615">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="c1187-1615">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-1616">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-1616">Az.Monitor</span></span>
* <span data-ttu-id="c1187-1617">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1617">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="c1187-1618">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1187-1618">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="c1187-1619">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="c1187-1619">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="c1187-1620">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1620">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-1621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-1621">Az.Network</span></span>
* <span data-ttu-id="c1187-1622">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1622">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="c1187-1623">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1623">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="c1187-1624">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1624">New cmdlets added:</span></span>
        - <span data-ttu-id="c1187-1625">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="c1187-1625">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="c1187-1626">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1626">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c1187-1627">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1627">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="c1187-1628">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1628">Updated cmdlets:</span></span>
        - <span data-ttu-id="c1187-1629">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-1629">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c1187-1630">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-1630">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c1187-1631">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-1631">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="c1187-1632">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1632">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="c1187-1633">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="c1187-1633">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="c1187-1634">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="c1187-1634">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="c1187-1635">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="c1187-1635">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c1187-1636">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c1187-1636">Az.RedisCache</span></span>
* <span data-ttu-id="c1187-1637">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1637">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1638">Az.Sql</span></span>
* <span data-ttu-id="c1187-1639">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1639">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-1640">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-1640">Az.Storage</span></span>
* <span data-ttu-id="c1187-1641">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1641">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="c1187-1642">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="c1187-1642">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="c1187-1643">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c1187-1643">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="c1187-1644">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="c1187-1644">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="c1187-1645">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-1645">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c1187-1646">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c1187-1646">Az.StorageSync</span></span>
* <span data-ttu-id="c1187-1647">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1647">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-1648">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-1648">Az.Websites</span></span>
* <span data-ttu-id="c1187-1649">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="c1187-1649">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="c1187-1650">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-1650">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="c1187-1651">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-1651">Az.ApiManagement</span></span>
* <span data-ttu-id="c1187-1652">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1652">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="c1187-1653">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1653">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="c1187-1654">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1187-1654">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-1655">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-1655">Az.Automation</span></span>
* <span data-ttu-id="c1187-1656">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1656">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="c1187-1657">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1657">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="c1187-1658">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1658">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-1659">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-1659">Az.Compute</span></span>
* <span data-ttu-id="c1187-1660">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1660">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="c1187-1661">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1661">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="c1187-1662">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1662">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="c1187-1663">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1663">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="c1187-1664">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1664">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="c1187-1665">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1665">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="c1187-1666">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1666">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="c1187-1667">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1667">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="c1187-1668">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1668">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-1669">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-1669">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-1670">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="c1187-1670">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="c1187-1671">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1671">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c1187-1672">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-1672">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-1673">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="c1187-1673">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c1187-1674">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-1674">Az.IotHub</span></span>
* <span data-ttu-id="c1187-1675">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1675">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="c1187-1676">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1676">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="c1187-1677">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c1187-1677">New cmdlets are:</span></span>
    - <span data-ttu-id="c1187-1678">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c1187-1678">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="c1187-1679">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c1187-1679">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="c1187-1680">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c1187-1680">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="c1187-1681">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c1187-1681">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-1682">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-1682">Az.Monitor</span></span>
* <span data-ttu-id="c1187-1683">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="c1187-1683">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="c1187-1684">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="c1187-1684">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="c1187-1685">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="c1187-1685">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="c1187-1686">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="c1187-1686">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="c1187-1687">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1687">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="c1187-1688">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1688">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="c1187-1689">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1689">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="c1187-1690">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="c1187-1690">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="c1187-1691">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1691">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="c1187-1692">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="c1187-1692">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="c1187-1693">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1693">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="c1187-1694">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="c1187-1694">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="c1187-1695">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1695">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="c1187-1696">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="c1187-1696">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="c1187-1697">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="c1187-1697">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="c1187-1698">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="c1187-1698">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="c1187-1699">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="c1187-1699">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="c1187-1700">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="c1187-1700">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="c1187-1701">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1701">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="c1187-1702">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1702">Overall improved help files</span></span>
* <span data-ttu-id="c1187-1703">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1703">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-1704">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-1704">Az.Network</span></span>
* <span data-ttu-id="c1187-1705">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1705">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="c1187-1706">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1706">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="c1187-1707">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1707">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="c1187-1708">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1708">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="c1187-1709">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1709">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="c1187-1710">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1710">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="c1187-1711">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1711">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="c1187-1712">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1712">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="c1187-1713">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1713">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="c1187-1714">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1714">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="c1187-1715">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1715">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="c1187-1716">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="c1187-1716">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="c1187-1717">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-1717">New cmdlets</span></span>
        - <span data-ttu-id="c1187-1718">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c1187-1718">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="c1187-1719">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1719">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="c1187-1720">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1720">Updated cmdlet:</span></span>
        - <span data-ttu-id="c1187-1721">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="c1187-1721">New-VpnSite</span></span>
        - <span data-ttu-id="c1187-1722">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="c1187-1722">Update-VpnSite</span></span>
        - <span data-ttu-id="c1187-1723">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1723">New-VpnConnection</span></span>
        - <span data-ttu-id="c1187-1724">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1724">Update-VpnConnection</span></span>
* <span data-ttu-id="c1187-1725">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1725">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-1726">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-1726">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-1727">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1727">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="c1187-1728">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1728">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-1729">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-1729">Az.Resources</span></span>
* <span data-ttu-id="c1187-1730">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1730">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c1187-1731">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1187-1731">Az.ServiceFabric</span></span>
* <span data-ttu-id="c1187-1732">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1732">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="c1187-1733">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="c1187-1733">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="c1187-1734">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c1187-1734">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c1187-1735">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c1187-1735">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="c1187-1736">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c1187-1736">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="c1187-1737">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c1187-1737">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="c1187-1738">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c1187-1738">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c1187-1739">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c1187-1739">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c1187-1740">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c1187-1740">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="c1187-1741">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c1187-1741">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="c1187-1742">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c1187-1742">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="c1187-1743">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c1187-1743">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c1187-1744">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c1187-1744">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="c1187-1745">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c1187-1745">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="c1187-1746">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="c1187-1746">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="c1187-1747">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1747">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c1187-1748">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c1187-1748">Az.SignalR</span></span>
* <span data-ttu-id="c1187-1749">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1749">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1750">Az.Sql</span></span>
* <span data-ttu-id="c1187-1751">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1751">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="c1187-1752">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1752">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="c1187-1753">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-1753">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="c1187-1754">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1754">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="c1187-1755">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1755">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-1756">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-1756">Az.Storage</span></span>
* <span data-ttu-id="c1187-1757">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1757">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="c1187-1758">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1758">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="c1187-1759">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c1187-1759">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="c1187-1760">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c1187-1760">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="c1187-1761">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1761">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="c1187-1762">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c1187-1762">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="c1187-1763">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1763">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="c1187-1764">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c1187-1764">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="c1187-1765">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c1187-1765">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="c1187-1766">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c1187-1766">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="c1187-1767">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c1187-1767">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-1768">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-1768">Az.Websites</span></span>
* <span data-ttu-id="c1187-1769">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="c1187-1769">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="c1187-1770">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="c1187-1770">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="c1187-1771">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1771">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="c1187-1772">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-1772">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="c1187-1773">Genel</span><span class="sxs-lookup"><span data-stu-id="c1187-1773">General</span></span>
* <span data-ttu-id="c1187-1774">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1774">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c1187-1775">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-1775">Az.Accounts</span></span>
* <span data-ttu-id="c1187-1776">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="c1187-1776">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="c1187-1777">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c1187-1777">Az.Aks</span></span>
* <span data-ttu-id="c1187-1778">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1778">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="c1187-1779">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="c1187-1779">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c1187-1780">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-1780">Az.ApiManagement</span></span>
* <span data-ttu-id="c1187-1781">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="c1187-1782">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1782">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="c1187-1783">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1783">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="c1187-1784">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="c1187-1784">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="c1187-1785">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1785">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c1187-1786">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c1187-1786">Az.Batch</span></span>
* <span data-ttu-id="c1187-1787">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1787">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c1187-1788">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c1187-1788">Az.Cdn</span></span>
* <span data-ttu-id="c1187-1789">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1789">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-1790">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-1790">Az.Compute</span></span>
* <span data-ttu-id="c1187-1791">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1791">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="c1187-1792">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1792">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="c1187-1793">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1793">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="c1187-1794">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1794">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="c1187-1795">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="c1187-1795">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="c1187-1796">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1796">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="c1187-1797">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1797">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="c1187-1798">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1798">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-1799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-1799">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-1800">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1800">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="c1187-1801">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1801">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="c1187-1802">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1802">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="c1187-1803">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1803">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-1804">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-1804">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-1805">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1805">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c1187-1806">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1187-1806">Az.EventHub</span></span>
* <span data-ttu-id="c1187-1807">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="c1187-1807">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="c1187-1808">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="c1187-1808">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="c1187-1809">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1809">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="c1187-1810">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="c1187-1810">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="c1187-1811">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c1187-1811">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c1187-1812">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1812">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-1813">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-1813">Az.Monitor</span></span>
* <span data-ttu-id="c1187-1814">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1814">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-1815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-1815">Az.Network</span></span>
* <span data-ttu-id="c1187-1816">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1816">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="c1187-1817">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1817">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="c1187-1818">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1818">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="c1187-1819">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="c1187-1819">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="c1187-1820">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="c1187-1820">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="c1187-1821">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1821">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="c1187-1822">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1822">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c1187-1823">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-1823">Az.OperationalInsights</span></span>
* <span data-ttu-id="c1187-1824">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1824">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="c1187-1825">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1825">Added example</span></span>
    - <span data-ttu-id="c1187-1826">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1826">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="c1187-1827">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1827">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="c1187-1828">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1828">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-1829">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-1829">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-1830">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1830">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-1831">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-1831">Az.Resources</span></span>
* <span data-ttu-id="c1187-1832">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1832">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="c1187-1833">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1833">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="c1187-1834">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="c1187-1834">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="c1187-1835">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1835">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c1187-1836">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1187-1836">Az.ServiceBus</span></span>
* <span data-ttu-id="c1187-1837">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="c1187-1837">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="c1187-1838">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="c1187-1838">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="c1187-1839">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1839">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c1187-1840">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1187-1840">Az.ServiceFabric</span></span>
* <span data-ttu-id="c1187-1841">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1841">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="c1187-1842">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="c1187-1842">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="c1187-1843">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="c1187-1843">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="c1187-1844">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1844">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="c1187-1845">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="c1187-1845">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="c1187-1846">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-1846">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1847">Az.Sql</span></span>
* <span data-ttu-id="c1187-1848">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1848">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-1849">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-1849">Az.Storage</span></span>
* <span data-ttu-id="c1187-1850">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1850">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="c1187-1851">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="c1187-1851">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="c1187-1852">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c1187-1852">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="c1187-1853">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c1187-1853">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="c1187-1854">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="c1187-1854">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="c1187-1855">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c1187-1855">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-1856">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-1856">Az.Websites</span></span>
* <span data-ttu-id="c1187-1857">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1857">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="c1187-1858">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-1858">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-1859">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-1859">Az.Accounts</span></span>
* <span data-ttu-id="c1187-1860">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1860">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="c1187-1861">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-1861">Az.ApplicationInsights</span></span>
* <span data-ttu-id="c1187-1862">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1862">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-1863">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-1863">Az.Automation</span></span>
* <span data-ttu-id="c1187-1864">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1864">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c1187-1865">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1187-1865">Az.CognitiveServices</span></span>
* <span data-ttu-id="c1187-1866">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1866">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-1867">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-1867">Az.Compute</span></span>
* <span data-ttu-id="c1187-1868">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1868">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="c1187-1869">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c1187-1869">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c1187-1870">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1870">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="c1187-1871">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="c1187-1871">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-1872">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-1872">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-1873">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1873">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="c1187-1874">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1874">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c1187-1875">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1187-1875">Az.EventHub</span></span>
* <span data-ttu-id="c1187-1876">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="c1187-1876">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="c1187-1877">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1877">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-1878">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-1878">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-1879">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1879">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c1187-1880">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c1187-1880">Az.LogicApp</span></span>
* <span data-ttu-id="c1187-1881">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="c1187-1881">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="c1187-1882">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1882">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="c1187-1883">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="c1187-1883">Az.ManagedServices</span></span>
* <span data-ttu-id="c1187-1884">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="c1187-1884">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-1885">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-1885">Az.Network</span></span>
* <span data-ttu-id="c1187-1886">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1886">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="c1187-1887">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-1887">New cmdlets</span></span>
        - <span data-ttu-id="c1187-1888">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1187-1888">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c1187-1889">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c1187-1889">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c1187-1890">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1890">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c1187-1891">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1891">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c1187-1892">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1892">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c1187-1893">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-1893">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c1187-1894">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="c1187-1894">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="c1187-1895">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c1187-1895">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="c1187-1896">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="c1187-1896">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="c1187-1897">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1897">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="c1187-1898">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1898">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="c1187-1899">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1899">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="c1187-1900">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-1900">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="c1187-1901">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1901">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="c1187-1902">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1902">Updated cmdlets</span></span>
        - <span data-ttu-id="c1187-1903">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-1903">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c1187-1904">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-1904">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c1187-1905">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-1905">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="c1187-1906">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1906">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c1187-1907">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1907">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="c1187-1908">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-1908">Updated cmdlet:</span></span>
        - <span data-ttu-id="c1187-1909">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-1909">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="c1187-1910">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-1910">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="c1187-1911">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-1911">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="c1187-1912">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1912">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="c1187-1913">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1913">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="c1187-1914">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="c1187-1914">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c1187-1915">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-1915">Az.OperationalInsights</span></span>
* <span data-ttu-id="c1187-1916">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1916">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="c1187-1917">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1917">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-1918">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-1918">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-1919">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1919">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="c1187-1920">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1920">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="c1187-1921">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1921">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="c1187-1922">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1922">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="c1187-1923">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1923">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="c1187-1924">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1924">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="c1187-1925">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1925">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="c1187-1926">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1926">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="c1187-1927">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1927">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="c1187-1928">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1928">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-1929">Az.Resources</span></span>
- <span data-ttu-id="c1187-1930">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-1930">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="c1187-1931">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1931">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c1187-1932">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1187-1932">Az.ServiceBus</span></span>
* <span data-ttu-id="c1187-1933">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="c1187-1933">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="c1187-1934">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1934">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1935">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1935">Az.Sql</span></span>
* <span data-ttu-id="c1187-1936">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1936">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="c1187-1937">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1937">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="c1187-1938">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1938">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-1939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-1939">Az.Storage</span></span>
* <span data-ttu-id="c1187-1940">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1940">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c1187-1941">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c1187-1941">Az.StorageSync</span></span>
* <span data-ttu-id="c1187-1942">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1942">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="c1187-1943">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1943">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-1944">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-1944">Az.Websites</span></span>
* <span data-ttu-id="c1187-1945">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1945">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="c1187-1946">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1946">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="c1187-1947">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1947">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="c1187-1948">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-1948">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-1949">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-1949">Az.Accounts</span></span>
* <span data-ttu-id="c1187-1950">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1950">Add support for profile cmdlets</span></span>
* <span data-ttu-id="c1187-1951">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1951">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="c1187-1952">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1952">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="c1187-1953">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="c1187-1953">Az.Advisor</span></span>
* <span data-ttu-id="c1187-1954">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-1954">GA release of Az.Advisor</span></span>
* <span data-ttu-id="c1187-1955">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="c1187-1955">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c1187-1956">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-1956">Az.ApiManagement</span></span>
* <span data-ttu-id="c1187-1957">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1957">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="c1187-1958">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="c1187-1958">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="c1187-1959">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1959">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="c1187-1960">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="c1187-1960">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="c1187-1961">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="c1187-1961">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="c1187-1962">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="c1187-1962">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="c1187-1963">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1963">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-1964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-1964">Az.Automation</span></span>
* <span data-ttu-id="c1187-1965">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1965">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-1966">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-1966">Az.Compute</span></span>
* <span data-ttu-id="c1187-1967">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1967">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-1968">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-1968">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-1969">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-1969">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c1187-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c1187-1970">Az.EventGrid</span></span>
* <span data-ttu-id="c1187-1971">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1971">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c1187-1972">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-1972">Az.IotHub</span></span>
* <span data-ttu-id="c1187-1973">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-1973">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-1974">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-1974">Az.Network</span></span>
* <span data-ttu-id="c1187-1975">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1975">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="c1187-1976">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1976">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c1187-1977">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-1977">Az.PolicyInsights</span></span>
* <span data-ttu-id="c1187-1978">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1978">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="c1187-1979">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="c1187-1979">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c1187-1980">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-1980">Az.OperationalInsights</span></span>
* <span data-ttu-id="c1187-1981">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1981">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-1982">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-1982">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-1983">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c1187-1983">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-1984">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-1984">Az.Resources</span></span>
    - <span data-ttu-id="c1187-1985">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c1187-1985">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="c1187-1986">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1986">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="c1187-1987">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1987">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="c1187-1988">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1988">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c1187-1989">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1187-1989">Az.ServiceBus</span></span>
* <span data-ttu-id="c1187-1990">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-1990">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-1991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-1991">Az.Sql</span></span>
* <span data-ttu-id="c1187-1992">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-1992">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="c1187-1993">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-1993">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="c1187-1994">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c1187-1994">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="c1187-1995">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c1187-1995">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="c1187-1996">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c1187-1996">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="c1187-1997">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c1187-1997">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="c1187-1998">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c1187-1998">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="c1187-1999">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c1187-1999">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="c1187-2000">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-2000">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-2001">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-2001">Az.Storage</span></span>
* <span data-ttu-id="c1187-2002">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-2002">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="c1187-2003">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c1187-2003">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="c1187-2004">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2004">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="c1187-2005">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="c1187-2005">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="c1187-2006">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2006">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="c1187-2007">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-2007">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="c1187-2008">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-2008">Set-AzStorageAccount</span></span>
* <span data-ttu-id="c1187-2009">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2009">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="c1187-2010">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c1187-2010">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="c1187-2011">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c1187-2011">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c1187-2012">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c1187-2012">Az.StorageSync</span></span>
* <span data-ttu-id="c1187-2013">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="c1187-2013">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="c1187-2014">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2014">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-2015">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-2015">Az.Accounts</span></span>
* <span data-ttu-id="c1187-2016">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2016">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="c1187-2017">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="c1187-2017">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="c1187-2018">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2018">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="c1187-2019">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c1187-2019">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="c1187-2020">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="c1187-2020">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2021">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2021">Az.Compute</span></span>
* <span data-ttu-id="c1187-2022">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-2022">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="c1187-2023">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2023">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="c1187-2024">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="c1187-2024">Az.Dns</span></span>
* <span data-ttu-id="c1187-2025">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2025">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c1187-2026">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c1187-2026">Az.EventGrid</span></span>
* <span data-ttu-id="c1187-2027">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2027">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="c1187-2028">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="c1187-2028">New cmdlets:</span></span>
    - <span data-ttu-id="c1187-2029">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c1187-2029">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="c1187-2030">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1187-2030">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="c1187-2031">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c1187-2031">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="c1187-2032">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="c1187-2032">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="c1187-2033">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c1187-2033">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="c1187-2034">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1187-2034">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="c1187-2035">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="c1187-2035">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="c1187-2036">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="c1187-2036">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="c1187-2037">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="c1187-2037">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="c1187-2038">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="c1187-2038">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="c1187-2039">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="c1187-2039">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="c1187-2040">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1187-2040">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="c1187-2041">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="c1187-2041">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="c1187-2042">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="c1187-2042">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="c1187-2043">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="c1187-2043">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="c1187-2044">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1187-2044">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="c1187-2045">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-2045">Updated cmdlets:</span></span>
    - <span data-ttu-id="c1187-2046">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="c1187-2046">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="c1187-2047">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="c1187-2047">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="c1187-2048">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="c1187-2048">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="c1187-2049">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="c1187-2049">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="c1187-2050">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-2050">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="c1187-2051">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="c1187-2051">Event subscription expiration date,</span></span>
            - <span data-ttu-id="c1187-2052">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="c1187-2052">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="c1187-2053">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="c1187-2053">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="c1187-2054">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="c1187-2054">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="c1187-2055">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="c1187-2055">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="c1187-2056">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="c1187-2056">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="c1187-2057">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c1187-2057">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="c1187-2058">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="c1187-2058">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="c1187-2059">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="c1187-2059">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c1187-2060">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c1187-2060">Az.FrontDoor</span></span>
* <span data-ttu-id="c1187-2061">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="c1187-2061">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="c1187-2062">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="c1187-2062">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="c1187-2063">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="c1187-2063">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="c1187-2064">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="c1187-2064">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-2065">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2065">Az.Network</span></span>
* <span data-ttu-id="c1187-2066">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="c1187-2066">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="c1187-2067">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2067">New cmdlets</span></span>
        - <span data-ttu-id="c1187-2068">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="c1187-2068">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="c1187-2069">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="c1187-2069">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="c1187-2070">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2070">New cmdlets</span></span>
        - <span data-ttu-id="c1187-2071">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="c1187-2071">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="c1187-2072">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="c1187-2072">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="c1187-2073">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2073">New cmdlets</span></span>
        - <span data-ttu-id="c1187-2074">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c1187-2074">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c1187-2075">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c1187-2075">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c1187-2076">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c1187-2076">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c1187-2077">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-2077">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="c1187-2078">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-2078">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="c1187-2079">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="c1187-2079">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="c1187-2080">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2080">New cmdlets</span></span>
        - <span data-ttu-id="c1187-2081">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1187-2081">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c1187-2082">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1187-2082">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c1187-2083">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1187-2083">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c1187-2084">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="c1187-2084">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="c1187-2085">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="c1187-2085">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="c1187-2086">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2086">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="c1187-2087">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2087">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="c1187-2088">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2088">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="c1187-2089">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2089">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="c1187-2090">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2090">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="c1187-2091">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2091">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="c1187-2092">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2092">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="c1187-2093">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2093">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="c1187-2094">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2094">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="c1187-2095">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2095">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="c1187-2096">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2096">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="c1187-2097">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2097">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="c1187-2098">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2098">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="c1187-2099">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-2099">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="c1187-2100">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2100">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="c1187-2101">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2101">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="c1187-2102">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c1187-2102">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="c1187-2103">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c1187-2103">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="c1187-2104">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2104">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="c1187-2105">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2105">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="c1187-2106">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2106">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="c1187-2107">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2107">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c1187-2108">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-2108">Az.OperationalInsights</span></span>
* <span data-ttu-id="c1187-2109">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2109">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-2110">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2110">Az.Resources</span></span>
* <span data-ttu-id="c1187-2111">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="c1187-2111">Support for additional Template Export options</span></span>
    - <span data-ttu-id="c1187-2112">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2112">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="c1187-2113">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2113">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="c1187-2114">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2114">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c1187-2115">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1187-2115">Az.ServiceFabric</span></span>
* <span data-ttu-id="c1187-2116">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2116">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-2117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2117">Az.Sql</span></span>
* <span data-ttu-id="c1187-2118">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2118">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="c1187-2119">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2119">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="c1187-2120">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2120">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="c1187-2121">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c1187-2121">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="c1187-2122">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c1187-2122">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="c1187-2123">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c1187-2123">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="c1187-2124">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c1187-2124">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="c1187-2125">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c1187-2125">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-2126">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-2126">Az.Storage</span></span>
* <span data-ttu-id="c1187-2127">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="c1187-2127">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="c1187-2128">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-2128">New-AzStorageAccount</span></span>
* <span data-ttu-id="c1187-2129">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2129">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="c1187-2130">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c1187-2130">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-2131">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-2131">Az.Websites</span></span>
* <span data-ttu-id="c1187-2132">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="c1187-2132">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="c1187-2133">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="c1187-2133">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="c1187-2134">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2134">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="c1187-2135">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c1187-2135">Az.Cdn</span></span>
* <span data-ttu-id="c1187-2136">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2136">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2137">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2137">Az.Compute</span></span>
* <span data-ttu-id="c1187-2138">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2138">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="c1187-2139">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="c1187-2139">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c1187-2140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1187-2140">Az.EventHub</span></span>
* <span data-ttu-id="c1187-2141">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c1187-2141">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="c1187-2142">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c1187-2142">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-2143">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2143">Az.Network</span></span>
* <span data-ttu-id="c1187-2144">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2144">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="c1187-2145">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2145">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c1187-2146">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-2146">Az.PolicyInsights</span></span>
* <span data-ttu-id="c1187-2147">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2147">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-2148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2148">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-2149">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2149">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c1187-2150">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1187-2150">Az.ServiceBus</span></span>
* <span data-ttu-id="c1187-2151">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="c1187-2151">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c1187-2152">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1187-2152">Az.ServiceFabric</span></span>
* <span data-ttu-id="c1187-2153">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2153">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="c1187-2154">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2154">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2155">Az.Sql</span></span>
* <span data-ttu-id="c1187-2156">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2156">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="c1187-2157">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-2157">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="c1187-2158">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-2158">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="c1187-2159">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2159">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-2160">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-2160">Az.Websites</span></span>
* <span data-ttu-id="c1187-2161">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2161">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="c1187-2162">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2162">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="c1187-2163">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-2163">Az.ApiManagement</span></span>
* <span data-ttu-id="c1187-2164">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-2164">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="c1187-2165">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="c1187-2165">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="c1187-2166">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="c1187-2166">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="c1187-2167">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="c1187-2167">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="c1187-2168">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1187-2168">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="c1187-2169">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="c1187-2169">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="c1187-2170">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="c1187-2170">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="c1187-2171">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c1187-2171">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="c1187-2172">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-2172">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="c1187-2173">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="c1187-2173">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="c1187-2174">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="c1187-2174">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="c1187-2175">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="c1187-2175">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="c1187-2176">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c1187-2176">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="c1187-2177">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-2177">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="c1187-2178">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="c1187-2178">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="c1187-2179">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="c1187-2179">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="c1187-2180">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="c1187-2180">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="c1187-2181">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c1187-2181">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="c1187-2182">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="c1187-2182">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="c1187-2183">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="c1187-2183">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="c1187-2184">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-2184">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="c1187-2185">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c1187-2185">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="c1187-2186">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="c1187-2186">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="c1187-2187">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2187">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="c1187-2188">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2188">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="c1187-2189">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2189">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="c1187-2190">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="c1187-2190">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="c1187-2191">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c1187-2191">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="c1187-2192">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2192">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="c1187-2193">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2193">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="c1187-2194">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2194">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="c1187-2195">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="c1187-2195">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="c1187-2196">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2196">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="c1187-2197">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2197">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="c1187-2198">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="c1187-2198">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="c1187-2199">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="c1187-2199">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="c1187-2200">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="c1187-2200">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="c1187-2201">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2201">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="c1187-2202">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2202">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="c1187-2203">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2203">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="c1187-2204">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="c1187-2204">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="c1187-2205">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="c1187-2205">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="c1187-2206">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="c1187-2206">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="c1187-2207">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="c1187-2207">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="c1187-2208">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2208">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="c1187-2209">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="c1187-2209">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="c1187-2210">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="c1187-2210">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="c1187-2211">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="c1187-2211">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="c1187-2212">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2212">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="c1187-2213">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="c1187-2213">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="c1187-2214">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="c1187-2214">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="c1187-2215">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="c1187-2215">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="c1187-2216">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="c1187-2216">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="c1187-2217">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2217">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="c1187-2218">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="c1187-2218">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="c1187-2219">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="c1187-2219">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="c1187-2220">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2220">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="c1187-2221">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="c1187-2221">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="c1187-2222">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="c1187-2222">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="c1187-2223">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2223">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="c1187-2224">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2224">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="c1187-2225">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="c1187-2225">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="c1187-2226">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="c1187-2226">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="c1187-2227">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2227">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="c1187-2228">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2228">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="c1187-2229">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="c1187-2229">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="c1187-2230">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="c1187-2230">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="c1187-2231">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="c1187-2231">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="c1187-2232">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="c1187-2232">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="c1187-2233">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="c1187-2233">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="c1187-2234">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="c1187-2234">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="c1187-2235">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="c1187-2235">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="c1187-2236">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="c1187-2236">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="c1187-2237">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="c1187-2237">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="c1187-2238">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="c1187-2238">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="c1187-2239">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="c1187-2239">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="c1187-2240">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="c1187-2240">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-2241">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-2241">Az.Automation</span></span>
* <span data-ttu-id="c1187-2242">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2242">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="c1187-2243">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2243">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="c1187-2244">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2244">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="c1187-2245">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2245">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="c1187-2246">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2246">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="c1187-2247">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2247">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="c1187-2248">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-2248">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2249">Az.Compute</span></span>
* <span data-ttu-id="c1187-2250">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2250">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="c1187-2251">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="c1187-2251">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-2252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-2252">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-2253">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2253">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-2254">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-2254">Az.Monitor</span></span>
* <span data-ttu-id="c1187-2255">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2255">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-2256">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2256">Az.Network</span></span>
* <span data-ttu-id="c1187-2257">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2257">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="c1187-2258">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="c1187-2258">Updated cmdlet:</span></span>
        - <span data-ttu-id="c1187-2259">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1187-2259">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="c1187-2260">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2260">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-2261">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2261">Az.Resources</span></span>
* <span data-ttu-id="c1187-2262">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2262">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-2263">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2263">Az.Sql</span></span>
* <span data-ttu-id="c1187-2264">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="c1187-2264">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="c1187-2265">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2265">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-2266">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-2266">Az.Accounts</span></span>
* <span data-ttu-id="c1187-2267">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="c1187-2267">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c1187-2268">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2268">Az.CognitiveServices</span></span>
* <span data-ttu-id="c1187-2269">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="c1187-2269">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="c1187-2270">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="c1187-2270">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2271">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2271">Az.Compute</span></span>
* <span data-ttu-id="c1187-2272">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="c1187-2272">Proximity placement group feature.</span></span>
    - <span data-ttu-id="c1187-2273">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c1187-2273">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="c1187-2274">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-2274">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="c1187-2275">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2275">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="c1187-2276">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="c1187-2276">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="c1187-2277">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2277">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="c1187-2278">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c1187-2278">Breaking changes</span></span>
    - <span data-ttu-id="c1187-2279">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2279">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="c1187-2280">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2280">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="c1187-2281">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="c1187-2281">Az.DeploymentManager</span></span>
* <span data-ttu-id="c1187-2282">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="c1187-2282">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="c1187-2283">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="c1187-2283">Az.Dns</span></span>
* <span data-ttu-id="c1187-2284">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="c1187-2284">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="c1187-2285">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="c1187-2285">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="c1187-2286">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="c1187-2286">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c1187-2287">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c1187-2287">Az.FrontDoor</span></span>
* <span data-ttu-id="c1187-2288">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="c1187-2288">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="c1187-2289">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="c1187-2289">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="c1187-2290">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-2290">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-2291">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="c1187-2291">Removed two cmdlets:</span></span>
    - <span data-ttu-id="c1187-2292">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c1187-2292">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="c1187-2293">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c1187-2293">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="c1187-2294">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2294">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="c1187-2295">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="c1187-2295">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="c1187-2296">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="c1187-2296">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="c1187-2297">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="c1187-2297">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-2298">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-2298">Az.Monitor</span></span>
* <span data-ttu-id="c1187-2299">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2299">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="c1187-2300">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="c1187-2300">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="c1187-2301">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="c1187-2301">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="c1187-2302">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="c1187-2302">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="c1187-2303">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="c1187-2303">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="c1187-2304">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="c1187-2304">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="c1187-2305">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="c1187-2305">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="c1187-2306">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c1187-2306">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c1187-2307">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c1187-2307">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c1187-2308">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c1187-2308">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c1187-2309">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c1187-2309">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c1187-2310">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c1187-2310">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c1187-2311">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="c1187-2311">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="c1187-2312">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2312">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-2313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2313">Az.Network</span></span>
* <span data-ttu-id="c1187-2314">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="c1187-2314">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="c1187-2315">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2315">New cmdlets</span></span>
        - <span data-ttu-id="c1187-2316">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c1187-2316">New-AzNatGateway</span></span>
        - <span data-ttu-id="c1187-2317">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c1187-2317">Get-AzNatGateway</span></span>
        - <span data-ttu-id="c1187-2318">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c1187-2318">Set-AzNatGateway</span></span>
        - <span data-ttu-id="c1187-2319">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c1187-2319">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="c1187-2320">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2320">Updated cmdlets</span></span>
        - <span data-ttu-id="c1187-2321">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="c1187-2321">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="c1187-2322">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="c1187-2322">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="c1187-2323">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="c1187-2323">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="c1187-2324">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2324">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="c1187-2325">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2325">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c1187-2326">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-2326">Az.PolicyInsights</span></span>
* <span data-ttu-id="c1187-2327">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-2327">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="c1187-2328">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c1187-2328">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="c1187-2329">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="c1187-2329">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-2330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2330">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-2331">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-2331">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="c1187-2332">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="c1187-2332">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="c1187-2333">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="c1187-2333">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="c1187-2334">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="c1187-2334">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="c1187-2335">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="c1187-2335">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="c1187-2336">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="c1187-2336">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="c1187-2337">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c1187-2337">Az.Relay</span></span>
* <span data-ttu-id="c1187-2338">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="c1187-2338">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c1187-2339">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1187-2339">Az.ServiceBus</span></span>
* <span data-ttu-id="c1187-2340">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2340">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-2341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-2341">Az.Storage</span></span>
* <span data-ttu-id="c1187-2342">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="c1187-2342">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="c1187-2343">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="c1187-2343">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="c1187-2344">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="c1187-2344">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="c1187-2345">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-2345">New-AzStorageAccount</span></span>
* <span data-ttu-id="c1187-2346">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="c1187-2346">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="c1187-2347">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-2347">New-AzStorageAccount</span></span>
    - <span data-ttu-id="c1187-2348">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-2348">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="c1187-2349">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-2349">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-2350">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-2350">Az.Websites</span></span>
* <span data-ttu-id="c1187-2351">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="c1187-2351">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="c1187-2352">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2352">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="c1187-2353">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2353">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c1187-2354">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="c1187-2354">Highlights since the last major release</span></span>
* <span data-ttu-id="c1187-2355">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-2355">General availability of `Az` module</span></span>
* <span data-ttu-id="c1187-2356">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c1187-2356">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c1187-2357">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c1187-2357">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c1187-2358">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2358">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c1187-2359">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2359">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c1187-2360">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2360">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c1187-2361">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2361">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c1187-2362">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-2362">Az.Accounts</span></span>
* <span data-ttu-id="c1187-2363">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2363">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c1187-2364">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c1187-2364">Az.Batch</span></span>
* <span data-ttu-id="c1187-2365">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2365">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c1187-2366">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c1187-2366">Az.Cdn</span></span>
* <span data-ttu-id="c1187-2367">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2367">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c1187-2368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2368">Az.CognitiveServices</span></span>
* <span data-ttu-id="c1187-2369">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2370">Az.Compute</span></span>
* <span data-ttu-id="c1187-2371">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2371">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="c1187-2372">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c1187-2373">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2373">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-2374">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-2374">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-2375">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2375">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-2376">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-2376">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-2377">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2377">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c1187-2378">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c1187-2378">Az.EventGrid</span></span>
* <span data-ttu-id="c1187-2379">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2379">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c1187-2380">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1187-2380">Az.EventHub</span></span>
* <span data-ttu-id="c1187-2381">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2381">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c1187-2382">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1187-2382">Az.HDInsight</span></span>
* <span data-ttu-id="c1187-2383">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c1187-2384">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-2384">Az.IotHub</span></span>
* <span data-ttu-id="c1187-2385">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2385">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-2386">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-2386">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-2387">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2387">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c1187-2388">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2388">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="c1187-2389">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c1187-2389">Az.MachineLearning</span></span>
* <span data-ttu-id="c1187-2390">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2390">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="c1187-2391">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c1187-2391">Az.Media</span></span>
* <span data-ttu-id="c1187-2392">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2392">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-2393">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-2393">Az.Monitor</span></span>
  * <span data-ttu-id="c1187-2394">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2394">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="c1187-2395">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="c1187-2395">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="c1187-2396">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="c1187-2396">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="c1187-2397">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c1187-2397">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="c1187-2398">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c1187-2398">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="c1187-2399">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c1187-2399">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="c1187-2400">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2400">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-2401">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2401">Az.Network</span></span>
* <span data-ttu-id="c1187-2402">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2402">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c1187-2403">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2403">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="c1187-2404">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="c1187-2404">Az.NotificationHubs</span></span>
* <span data-ttu-id="c1187-2405">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2405">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c1187-2406">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-2406">Az.OperationalInsights</span></span>
* <span data-ttu-id="c1187-2407">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2407">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="c1187-2408">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c1187-2408">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="c1187-2409">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2409">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-2410">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2410">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-2411">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2411">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c1187-2412">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="c1187-2412">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="c1187-2413">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2413">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="c1187-2414">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2414">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c1187-2415">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c1187-2415">Az.RedisCache</span></span>
* <span data-ttu-id="c1187-2416">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2416">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-2417">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2417">Az.Resources</span></span>
* <span data-ttu-id="c1187-2418">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2418">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-2419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2419">Az.Sql</span></span>
* <span data-ttu-id="c1187-2420">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2420">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="c1187-2421">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2421">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c1187-2422">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2422">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="c1187-2423">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2423">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="c1187-2424">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2424">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="c1187-2425">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-2425">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="c1187-2426">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2426">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-2427">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-2427">Az.Websites</span></span>
* <span data-ttu-id="c1187-2428">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2428">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="c1187-2429">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2429">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c1187-2430">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2430">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="c1187-2431">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2431">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="c1187-2432">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2432">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c1187-2433">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="c1187-2433">Highlights since the last major release</span></span>
* <span data-ttu-id="c1187-2434">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-2434">General availability of `Az` module</span></span>
* <span data-ttu-id="c1187-2435">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c1187-2435">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c1187-2436">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c1187-2436">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c1187-2437">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2437">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c1187-2438">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2438">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c1187-2439">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2439">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c1187-2440">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2440">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c1187-2441">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-2441">Az.Accounts</span></span>
* <span data-ttu-id="c1187-2442">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2442">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c1187-2443">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2443">Az.AnalysisServices</span></span>
* <span data-ttu-id="c1187-2444">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1187-2444">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="c1187-2445">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="c1187-2445">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-2446">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-2446">Az.Automation</span></span>
* <span data-ttu-id="c1187-2447">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2447">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="c1187-2448">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-2448">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="c1187-2449">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c1187-2449">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2450">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2450">Az.Compute</span></span>
* <span data-ttu-id="c1187-2451">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2451">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="c1187-2452">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2452">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="c1187-2453">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c1187-2453">Az.ContainerInstance</span></span>
* <span data-ttu-id="c1187-2454">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2454">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-2455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-2455">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-2456">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2456">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="c1187-2457">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2457">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-2458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2458">Az.Resources</span></span>
* <span data-ttu-id="c1187-2459">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2459">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="c1187-2460">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2460">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="c1187-2461">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2461">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="c1187-2462">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="c1187-2462">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="c1187-2463">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2463">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="c1187-2464">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="c1187-2464">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-2465">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2465">Az.Sql</span></span>
* <span data-ttu-id="c1187-2466">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-2466">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-2467">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-2467">Az.Storage</span></span>
* <span data-ttu-id="c1187-2468">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="c1187-2468">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="c1187-2469">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c1187-2469">New-AzStorageContext</span></span>
* <span data-ttu-id="c1187-2470">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="c1187-2470">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="c1187-2471">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c1187-2471">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="c1187-2472">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c1187-2472">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="c1187-2473">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1187-2473">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="c1187-2474">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1187-2474">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="c1187-2475">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="c1187-2475">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="c1187-2476">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c1187-2476">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="c1187-2477">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c1187-2477">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="c1187-2478">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c1187-2478">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="c1187-2479">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c1187-2479">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="c1187-2480">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2480">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c1187-2481">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="c1187-2481">Highlights since the last major release</span></span>
* <span data-ttu-id="c1187-2482">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-2482">General availability of `Az` module</span></span>
* <span data-ttu-id="c1187-2483">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c1187-2483">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c1187-2484">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c1187-2484">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c1187-2485">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2485">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c1187-2486">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2486">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c1187-2487">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2487">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c1187-2488">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2488">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-2489">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-2489">Az.Automation</span></span>
* <span data-ttu-id="c1187-2490">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="c1187-2490">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="c1187-2491">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="c1187-2491">Dynamic grouping</span></span>
    * <span data-ttu-id="c1187-2492">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="c1187-2492">Pre-Post script</span></span>
    * <span data-ttu-id="c1187-2493">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="c1187-2493">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2494">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2494">Az.Compute</span></span>
* <span data-ttu-id="c1187-2495">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="c1187-2495">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="c1187-2496">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2496">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-2497">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-2497">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-2498">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2498">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-2499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2499">Az.Network</span></span>
* <span data-ttu-id="c1187-2500">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2500">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="c1187-2501">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2501">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-2502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2502">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-2503">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2503">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="c1187-2504">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2504">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-2505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2505">Az.Resources</span></span>
* <span data-ttu-id="c1187-2506">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2506">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="c1187-2507">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2507">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-2508">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2508">Az.Sql</span></span>
* <span data-ttu-id="c1187-2509">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2509">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-2510">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-2510">Az.Storage</span></span>
* <span data-ttu-id="c1187-2511">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="c1187-2511">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="c1187-2512">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c1187-2512">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c1187-2513">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c1187-2513">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c1187-2514">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c1187-2514">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c1187-2515">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="c1187-2515">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="c1187-2516">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="c1187-2516">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="c1187-2517">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="c1187-2517">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-2518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-2518">Az.Websites</span></span>
* <span data-ttu-id="c1187-2519">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2519">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="c1187-2520">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2520">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-2521">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-2521">Az.Accounts</span></span>
* <span data-ttu-id="c1187-2522">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2522">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="c1187-2523">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2523">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-2524">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-2524">Az.Automation</span></span>
* <span data-ttu-id="c1187-2525">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2525">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="c1187-2526">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2526">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="c1187-2527">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="c1187-2527">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c1187-2528">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c1187-2528">Az.Cdn</span></span>
* <span data-ttu-id="c1187-2529">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-2529">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2530">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2530">Az.Compute</span></span>
* <span data-ttu-id="c1187-2531">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2531">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-2532">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-2532">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-2533">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2533">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c1187-2534">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c1187-2534">Az.LogicApp</span></span>
* <span data-ttu-id="c1187-2535">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="c1187-2535">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-2536">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2536">Az.Network</span></span>
* <span data-ttu-id="c1187-2537">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2537">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-2538">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2538">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-2539">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2539">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="c1187-2540">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="c1187-2540">SDK Update</span></span>
* <span data-ttu-id="c1187-2541">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-2541">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="c1187-2542">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2542">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-2543">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2543">Az.Resources</span></span>
* <span data-ttu-id="c1187-2544">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2544">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="c1187-2545">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="c1187-2545">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="c1187-2546">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2546">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="c1187-2547">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="c1187-2547">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="c1187-2548">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2548">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="c1187-2549">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="c1187-2549">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-2550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2550">Az.Sql</span></span>
* <span data-ttu-id="c1187-2551">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-2551">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="c1187-2552">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-2552">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-2553">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-2553">Az.Storage</span></span>
* <span data-ttu-id="c1187-2554">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1187-2554">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="c1187-2555">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2555">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="c1187-2556">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2556">Az.AnalysisServices</span></span>
* <span data-ttu-id="c1187-2557">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-2557">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-2558">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-2558">Az.Automation</span></span>
* <span data-ttu-id="c1187-2559">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2559">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="c1187-2560">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2560">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="c1187-2561">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2561">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c1187-2562">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2562">Az.CognitiveServices</span></span>
* <span data-ttu-id="c1187-2563">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2563">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2564">Az.Compute</span></span>
* <span data-ttu-id="c1187-2565">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2565">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="c1187-2566">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2566">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="c1187-2567">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2567">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="c1187-2568">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="c1187-2568">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-2569">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-2569">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-2570">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2570">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c1187-2571">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c1187-2571">Az.EventHub</span></span>
* <span data-ttu-id="c1187-2572">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2572">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-2573">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-2573">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-2574">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2574">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c1187-2575">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c1187-2575">Az.LogicApp</span></span>
* <span data-ttu-id="c1187-2576">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2576">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="c1187-2577">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2577">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="c1187-2578">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2578">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="c1187-2579">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c1187-2579">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c1187-2580">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c1187-2580">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c1187-2581">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c1187-2581">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c1187-2582">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c1187-2582">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="c1187-2583">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="c1187-2583">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="c1187-2584">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1187-2584">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c1187-2585">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1187-2585">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c1187-2586">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1187-2586">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c1187-2587">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1187-2587">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="c1187-2588">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2588">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c1187-2589">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-2589">Az.Monitor</span></span>
* <span data-ttu-id="c1187-2590">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2590">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-2591">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2591">Az.Network</span></span>
* <span data-ttu-id="c1187-2592">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2592">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c1187-2593">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-2593">Az.OperationalInsights</span></span>
* <span data-ttu-id="c1187-2594">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="c1187-2594">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="c1187-2595">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2595">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="c1187-2596">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2596">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-2597">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2597">Az.Resources</span></span>
* <span data-ttu-id="c1187-2598">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2598">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c1187-2599">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2599">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="c1187-2600">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2600">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="c1187-2601">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2601">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-2602">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2602">Az.Sql</span></span>
* <span data-ttu-id="c1187-2603">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2603">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="c1187-2604">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2604">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-2605">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-2605">Az.Websites</span></span>
* <span data-ttu-id="c1187-2606">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2606">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="c1187-2607">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2607">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-2608">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-2608">Az.Accounts</span></span>
* <span data-ttu-id="c1187-2609">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c1187-2609">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c1187-2610">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2610">Az.AnalysisServices</span></span>
<span data-ttu-id="c1187-2611">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="c1187-2611">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2612">Az.Compute</span></span>
* <span data-ttu-id="c1187-2613">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2613">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="c1187-2614">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2614">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="c1187-2615">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2615">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-2616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2616">Az.RecoveryServices</span></span>
<span data-ttu-id="c1187-2617">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="c1187-2617">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-2618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2618">Az.Resources</span></span>
* <span data-ttu-id="c1187-2619">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2619">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="c1187-2620">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="c1187-2620">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c1187-2621">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2621">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="c1187-2622">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="c1187-2622">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-2623">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2623">Az.Sql</span></span>
* <span data-ttu-id="c1187-2624">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1187-2624">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="c1187-2625">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2625">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="c1187-2626">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2626">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="c1187-2627">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2627">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-2628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-2628">Az.Accounts</span></span>
* <span data-ttu-id="c1187-2629">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="c1187-2629">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c1187-2630">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2630">Az.AnalysisServices</span></span>
* <span data-ttu-id="c1187-2631">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="c1187-2631">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-2632">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2632">Az.RecoveryServices</span></span>
* <span data-ttu-id="c1187-2633">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="c1187-2633">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="c1187-2634">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2634">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-2635">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-2635">Az.Accounts</span></span>
* <span data-ttu-id="c1187-2636">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2636">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c1187-2637">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2637">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c1187-2638">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2638">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="c1187-2639">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c1187-2639">Az.Aks</span></span>
* <span data-ttu-id="c1187-2640">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2640">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c1187-2641">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-2641">Az.Automation</span></span>
* <span data-ttu-id="c1187-2642">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2642">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="c1187-2643">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2643">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c1187-2644">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c1187-2644">Az.Cdn</span></span>
* <span data-ttu-id="c1187-2645">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2645">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2646">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2646">Az.Compute</span></span>
* <span data-ttu-id="c1187-2647">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2647">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="c1187-2648">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2648">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="c1187-2649">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2649">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="c1187-2650">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c1187-2650">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c1187-2651">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2651">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c1187-2652">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1187-2652">Az.DataFactory</span></span>
* <span data-ttu-id="c1187-2653">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2653">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-2654">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-2654">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-2655">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2655">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="c1187-2656">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="c1187-2656">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="c1187-2657">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2657">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c1187-2658">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-2658">Az.IotHub</span></span>
* <span data-ttu-id="c1187-2659">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2659">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c1187-2660">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-2660">Az.KeyVault</span></span>
* <span data-ttu-id="c1187-2661">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2661">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-2662">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2662">Az.Network</span></span>
* <span data-ttu-id="c1187-2663">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2663">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-2664">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2664">Az.Resources</span></span>
* <span data-ttu-id="c1187-2665">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2665">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="c1187-2666">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2666">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="c1187-2667">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2667">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="c1187-2668">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2668">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="c1187-2669">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2669">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="c1187-2670">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2670">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="c1187-2671">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="c1187-2671">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c1187-2672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1187-2672">Az.ServiceFabric</span></span>
* <span data-ttu-id="c1187-2673">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="c1187-2673">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="c1187-2674">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2674">Fix some error messages.</span></span>
* <span data-ttu-id="c1187-2675">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2675">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="c1187-2676">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2676">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c1187-2677">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c1187-2677">Az.SignalR</span></span>
* <span data-ttu-id="c1187-2678">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2678">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-2679">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2679">Az.Sql</span></span>
* <span data-ttu-id="c1187-2680">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2680">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c1187-2681">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2681">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="c1187-2682">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2682">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="c1187-2683">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="c1187-2683">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-2684">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-2684">Az.Storage</span></span>
* <span data-ttu-id="c1187-2685">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2685">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c1187-2686">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-2686">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="c1187-2687">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c1187-2687">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="c1187-2688">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c1187-2688">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="c1187-2689">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c1187-2689">Az.TrafficManager</span></span>
* <span data-ttu-id="c1187-2690">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2690">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-2691">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-2691">Az.Websites</span></span>
* <span data-ttu-id="c1187-2692">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2692">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c1187-2693">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2693">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="c1187-2694">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2694">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="c1187-2695">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="c1187-2695">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c1187-2696">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-2696">Az.Accounts</span></span>
* <span data-ttu-id="c1187-2697">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2697">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2698">Az.Compute</span></span>
* <span data-ttu-id="c1187-2699">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="c1187-2699">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="c1187-2700">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2700">Updated the description of ID in help files</span></span>
* <span data-ttu-id="c1187-2701">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="c1187-2701">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-2702">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-2702">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-2703">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2703">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="c1187-2704">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2704">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c1187-2705">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c1187-2705">Az.EventGrid</span></span>
* <span data-ttu-id="c1187-2706">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2706">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="c1187-2707">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2707">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="c1187-2708">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-2708">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c1187-2709">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="c1187-2709">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c1187-2710">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="c1187-2710">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c1187-2711">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="c1187-2711">Dead letter endpoint.</span></span>
    - <span data-ttu-id="c1187-2712">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-2712">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c1187-2713">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="c1187-2713">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c1187-2714">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="c1187-2714">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c1187-2715">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="c1187-2715">Dead letter endpoint.</span></span>
* <span data-ttu-id="c1187-2716">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2716">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="c1187-2717">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-2717">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c1187-2718">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c1187-2718">Az.IotHub</span></span>
* <span data-ttu-id="c1187-2719">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2719">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c1187-2720">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c1187-2720">Az.LogicApp</span></span>
* <span data-ttu-id="c1187-2721">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="c1187-2721">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-2722">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2722">Az.Resources</span></span>
* <span data-ttu-id="c1187-2723">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2723">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="c1187-2724">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="c1187-2724">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="c1187-2725">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2725">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c1187-2726">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2726">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="c1187-2727">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2727">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="c1187-2728">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="c1187-2728">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c1187-2729">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c1187-2729">Az.SignalR</span></span>
* <span data-ttu-id="c1187-2730">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="c1187-2730">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-2731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2731">Az.Sql</span></span>
* <span data-ttu-id="c1187-2732">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="c1187-2732">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c1187-2733">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-2733">Az.Storage</span></span>
* <span data-ttu-id="c1187-2734">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="c1187-2734">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="c1187-2735">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c1187-2735">New-AzStorageContext</span></span>
* <span data-ttu-id="c1187-2736">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2736">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="c1187-2737">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c1187-2737">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-2738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-2738">Az.Websites</span></span>
* <span data-ttu-id="c1187-2739">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2739">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="c1187-2740">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="c1187-2740">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="c1187-2741">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="c1187-2741">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="c1187-2742">Genel</span><span class="sxs-lookup"><span data-stu-id="c1187-2742">General</span></span>

- <span data-ttu-id="c1187-2743">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-2743">General Availability of Az Module</span></span>
- <span data-ttu-id="c1187-2744">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="c1187-2744">Online help for each module</span></span>
- <span data-ttu-id="c1187-2745">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="c1187-2745">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="c1187-2746">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2746">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="c1187-2747">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c1187-2747">Az.Accounts</span></span>
- <span data-ttu-id="c1187-2748">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c1187-2748">Changed from Az.Profile</span></span>
- <span data-ttu-id="c1187-2749">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2749">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c1187-2750">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-2750">Az.ApiManagement</span></span>
- <span data-ttu-id="c1187-2751">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="c1187-2751">Fixes for #7002</span></span>
- <span data-ttu-id="c1187-2752">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2752">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="c1187-2753">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c1187-2753">Az.Batch</span></span>
- <span data-ttu-id="c1187-2754">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2754">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="c1187-2755">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="c1187-2755">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="c1187-2756">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2756">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="c1187-2757">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c1187-2757">Az.Billing</span></span>
- <span data-ttu-id="c1187-2758">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2758">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="c1187-2759">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2759">Az.CognitivServices</span></span>
- <span data-ttu-id="c1187-2760">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2760">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="c1187-2761">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-2761">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c1187-2762">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c1187-2762">Az.ContainerInstance</span></span>
- <span data-ttu-id="c1187-2763">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2763">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="c1187-2764">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c1187-2764">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="c1187-2765">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2765">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c1187-2766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-2766">Az.DataLakeStore</span></span>
- <span data-ttu-id="c1187-2767">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="c1187-2768">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c1187-2768">Az.Monitor</span></span>
- <span data-ttu-id="c1187-2769">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2769">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="c1187-2770">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1187-2770">Az.KeyVault</span></span>
- <span data-ttu-id="c1187-2771">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-2771">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="c1187-2772">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c1187-2772">Az.MachineLearning</span></span>
- <span data-ttu-id="c1187-2773">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2773">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="c1187-2774">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c1187-2774">Az.Media</span></span>
- <span data-ttu-id="c1187-2775">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c1187-2775">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c1187-2776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2776">Az.Network</span></span>
<span data-ttu-id="c1187-2777">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2777">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="c1187-2778">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="c1187-2778">New cmdlets added:</span></span>
        - <span data-ttu-id="c1187-2779">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1187-2779">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c1187-2780">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1187-2780">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c1187-2781">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1187-2781">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c1187-2782">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1187-2782">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c1187-2783">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1187-2783">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c1187-2784">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c1187-2784">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="c1187-2785">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c1187-2785">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="c1187-2786">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1187-2786">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="c1187-2787">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2787">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="c1187-2788">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1187-2788">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="c1187-2789">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1187-2789">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c1187-2790">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1187-2790">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c1187-2791">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-2791">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="c1187-2792">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-2792">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="c1187-2793">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2793">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="c1187-2794">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2794">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="c1187-2795">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c1187-2795">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c1187-2796">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c1187-2796">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c1187-2797">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c1187-2797">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="c1187-2798">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2798">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="c1187-2799">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2799">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="c1187-2800">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-2800">Az.OperationalInsights</span></span>
- <span data-ttu-id="c1187-2801">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2801">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="c1187-2802">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c1187-2802">Az.Profile</span></span>
- <span data-ttu-id="c1187-2803">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2803">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-2804">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2804">Az.RecoveryServices</span></span>
- <span data-ttu-id="c1187-2805">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2805">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="c1187-2806">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2806">Az.Resources</span></span>
- <span data-ttu-id="c1187-2807">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2807">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c1187-2808">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1187-2808">Az.ServiceFabric</span></span>
- <span data-ttu-id="c1187-2809">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="c1187-2809">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="c1187-2810">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2810">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="c1187-2811">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c1187-2811">Az.SIgnalR</span></span>
- <span data-ttu-id="c1187-2812">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="c1187-2812">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="c1187-2813">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2813">Az.Sql</span></span>
- <span data-ttu-id="c1187-2814">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2814">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="c1187-2815">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2815">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="c1187-2816">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="c1187-2817">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-2817">Az.Storage</span></span>
- <span data-ttu-id="c1187-2818">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2818">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c1187-2819">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-2819">Az.Websites</span></span>
- <span data-ttu-id="c1187-2820">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c1187-2820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="c1187-2821">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="c1187-2821">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="c1187-2822">Genel</span><span class="sxs-lookup"><span data-stu-id="c1187-2822">General</span></span>

* <span data-ttu-id="c1187-2823">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c1187-2823">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="c1187-2824">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2824">Az.Compute</span></span>

* <span data-ttu-id="c1187-2825">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2825">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c1187-2826">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-2826">Az.DataLakeStore</span></span>

* <span data-ttu-id="c1187-2827">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2827">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="c1187-2828">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c1187-2828">Az.FrontDoor</span></span>

* <span data-ttu-id="c1187-2829">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2829">Fixed some broken links</span></span>
    - <span data-ttu-id="c1187-2830">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2830">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="c1187-2831">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2831">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c1187-2832">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2832">Az.RecoveryServices</span></span>

* <span data-ttu-id="c1187-2833">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2833">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="c1187-2834">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2834">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="c1187-2835">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2835">Az.Resources</span></span>

* <span data-ttu-id="c1187-2836">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c1187-2836">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="c1187-2837">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2837">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="c1187-2838">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2838">Az.Sql</span></span>

* <span data-ttu-id="c1187-2839">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c1187-2839">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="c1187-2840">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2840">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="c1187-2841">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2841">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="c1187-2842">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c1187-2842">Az.Storage</span></span>

* <span data-ttu-id="c1187-2843">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2843">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="c1187-2844">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2844">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="c1187-2845">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c1187-2845">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c1187-2846">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2846">Support Static Website configuration</span></span>
    - <span data-ttu-id="c1187-2847">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c1187-2847">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="c1187-2848">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c1187-2848">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c1187-2849">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-2849">Az.Websites</span></span>

* <span data-ttu-id="c1187-2850">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c1187-2850">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="c1187-2851">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2851">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="c1187-2852">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1187-2852">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="c1187-2853">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="c1187-2853">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c1187-2854">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c1187-2854">Az.ApiManagement</span></span>
* <span data-ttu-id="c1187-2855">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="c1187-2855">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="c1187-2856">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c1187-2856">Az.Automation</span></span>
* <span data-ttu-id="c1187-2857">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="c1187-2857">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="c1187-2858">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2858">Added Update Management cmdlets</span></span>
* <span data-ttu-id="c1187-2859">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2859">Added Source Control cmdlets</span></span>
* <span data-ttu-id="c1187-2860">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2860">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="c1187-2861">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2861">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="c1187-2862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2862">Az.Compute</span></span>
* <span data-ttu-id="c1187-2863">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2863">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="c1187-2864">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="c1187-2864">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c1187-2865">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c1187-2865">Az.ContainerInstance</span></span>
* <span data-ttu-id="c1187-2866">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="c1187-2866">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="c1187-2867">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c1187-2867">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c1187-2868">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2868">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c1187-2869">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2869">Az.Network</span></span>
* <span data-ttu-id="c1187-2870">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2870">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="c1187-2871">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2871">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="c1187-2872">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2872">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="c1187-2873">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2873">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="c1187-2874">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c1187-2874">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c1187-2875">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2875">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="c1187-2876">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="c1187-2876">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="c1187-2877">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c1187-2877">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c1187-2878">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2878">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="c1187-2879">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="c1187-2879">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="c1187-2880">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c1187-2880">Az.Relay</span></span>
* <span data-ttu-id="c1187-2881">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2881">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="c1187-2882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2882">Az.Resources</span></span>
* <span data-ttu-id="c1187-2883">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2883">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="c1187-2884">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2884">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="c1187-2885">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="c1187-2885">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c1187-2886">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1187-2886">Az.ServiceFabric</span></span>
* <span data-ttu-id="c1187-2887">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2887">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="c1187-2888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-2888">Az.Sql</span></span>
* <span data-ttu-id="c1187-2889">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2889">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="c1187-2890">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c1187-2890">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c1187-2891">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c1187-2891">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c1187-2892">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c1187-2892">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c1187-2893">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c1187-2893">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c1187-2894">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c1187-2894">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c1187-2895">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c1187-2895">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c1187-2896">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c1187-2896">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c1187-2897">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c1187-2897">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="c1187-2898">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2898">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="c1187-2899">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2899">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="c1187-2900">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2900">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="c1187-2901">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c1187-2901">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c1187-2902">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c1187-2902">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c1187-2903">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c1187-2903">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="c1187-2904">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c1187-2904">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="c1187-2905">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2905">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="c1187-2906">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="c1187-2906">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c1187-2907">Genel</span><span class="sxs-lookup"><span data-stu-id="c1187-2907">General</span></span>
* <span data-ttu-id="c1187-2908">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="c1187-2908">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="c1187-2909">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c1187-2909">Az.Profile</span></span>
* <span data-ttu-id="c1187-2910">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2910">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="c1187-2911">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2911">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="c1187-2912">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2912">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="c1187-2913">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2913">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="c1187-2914">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2914">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="c1187-2915">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2915">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="c1187-2916">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2916">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="c1187-2917">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2917">Az.CognitiveServices</span></span>
* <span data-ttu-id="c1187-2918">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2918">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2919">Az.Compute</span></span>
* <span data-ttu-id="c1187-2920">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2920">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="c1187-2921">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="c1187-2921">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="c1187-2922">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2922">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-2923">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-2923">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-2924">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2924">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="c1187-2925">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2925">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="c1187-2926">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="c1187-2926">Az.Insights</span></span>
* <span data-ttu-id="c1187-2927">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2927">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="c1187-2928">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="c1187-2928">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="c1187-2929">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2929">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="c1187-2930">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="c1187-2930">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-2931">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2931">Az.Network</span></span>
* <span data-ttu-id="c1187-2932">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="c1187-2932">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="c1187-2933">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1187-2933">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="c1187-2934">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c1187-2934">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="c1187-2935">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c1187-2935">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="c1187-2936">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c1187-2936">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c1187-2937">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c1187-2937">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c1187-2938">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c1187-2938">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c1187-2939">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c1187-2939">Az.PolicyInsights</span></span>
* <span data-ttu-id="c1187-2940">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2940">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-2941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2941">Az.Resources</span></span>
* <span data-ttu-id="c1187-2942">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="c1187-2942">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="c1187-2943">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="c1187-2943">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c1187-2944">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1187-2944">Az.ServiceBus</span></span>
* <span data-ttu-id="c1187-2945">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2945">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c1187-2946">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1187-2946">Az.ServiceFabric</span></span>
* <span data-ttu-id="c1187-2947">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2947">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="c1187-2948">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2948">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="c1187-2949">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="c1187-2949">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="c1187-2950">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="c1187-2950">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="c1187-2951">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2951">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="c1187-2952">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="c1187-2952">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="c1187-2953">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c1187-2953">Az.Profile</span></span>
* <span data-ttu-id="c1187-2954">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="c1187-2954">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="c1187-2955">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2955">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2956">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2956">Az.Compute</span></span>
* <span data-ttu-id="c1187-2957">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2957">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="c1187-2958">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2958">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c1187-2959">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c1187-2959">Az.DataLakeStore</span></span>
* <span data-ttu-id="c1187-2960">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="c1187-2960">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c1187-2961">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="c1187-2961">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c1187-2962">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="c1187-2962">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c1187-2963">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c1187-2963">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c1187-2964">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="c1187-2964">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-2965">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2965">Az.Network</span></span>
* <span data-ttu-id="c1187-2966">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-2966">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c1187-2967">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2967">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-2968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-2968">Az.Resources</span></span>
* <span data-ttu-id="c1187-2969">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2969">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c1187-2970">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2970">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="c1187-2971">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="c1187-2971">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c1187-2972">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="c1187-2972">Azure.Storage</span></span>
* <span data-ttu-id="c1187-2973">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="c1187-2973">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c1187-2974">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c1187-2974">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c1187-2975">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c1187-2975">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c1187-2976">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="c1187-2976">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c1187-2977">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c1187-2977">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c1187-2978">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c1187-2978">Az.CognitiveServices</span></span>
* <span data-ttu-id="c1187-2979">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="c1187-2979">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c1187-2980">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c1187-2980">Az.Compute</span></span>
* <span data-ttu-id="c1187-2981">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2981">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c1187-2982">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2982">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="c1187-2983">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-2983">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="c1187-2984">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c1187-2984">Az.DataFactoryV2</span></span>
* <span data-ttu-id="c1187-2985">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2985">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c1187-2986">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c1187-2986">Az.Network</span></span>
* <span data-ttu-id="c1187-2987">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="c1187-2987">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c1187-2988">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2988">new cmdlets added</span></span>
    - <span data-ttu-id="c1187-2989">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1187-2989">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="c1187-2990">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1187-2990">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="c1187-2991">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1187-2991">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="c1187-2992">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c1187-2992">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="c1187-2993">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-2993">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="c1187-2994">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1187-2994">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c1187-2995">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2995">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c1187-2996">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2996">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="c1187-2997">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-2997">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c1187-2998">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c1187-2998">Az.RedisCache</span></span>
* <span data-ttu-id="c1187-2999">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="c1187-2999">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c1187-3000">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-3000">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="c1187-3001">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c1187-3001">Az.Resources</span></span>
* <span data-ttu-id="c1187-3002">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c1187-3002">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c1187-3003">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-3003">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="c1187-3004">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c1187-3004">Az.Sql</span></span>
* <span data-ttu-id="c1187-3005">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c1187-3005">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c1187-3006">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c1187-3006">Az.Websites</span></span>
* <span data-ttu-id="c1187-3007">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="c1187-3007">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c1187-3008">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="c1187-3008">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="c1187-3009">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="c1187-3009">0.2.0 - September 2018</span></span>
 <span data-ttu-id="c1187-3010">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="c1187-3010">Initial Release</span></span>
