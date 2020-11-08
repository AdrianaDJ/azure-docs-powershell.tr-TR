---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 34a1cde8eb68ead4689f0c63071473395c087876
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097975"
---
# <span data-ttu-id="3281c-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3281c-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="3281c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3281c-102">SYNOPSIS</span></span>
<span data-ttu-id="3281c-103">Bir yük dengeleyicinin kural yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3281c-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="3281c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3281c-104">SYNTAX</span></span>

### <span data-ttu-id="3281c-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3281c-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3281c-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="3281c-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3281c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3281c-107">DESCRIPTION</span></span>
<span data-ttu-id="3281c-108">**Set-AzLoadBalancerRuleConfig** cmdlet 'i, yük dengeleyicinin bir kural yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3281c-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="3281c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3281c-109">EXAMPLES</span></span>

### <span data-ttu-id="3281c-110">Örnek 1: Yük Dengeleme kuralı yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="3281c-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="3281c-111">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3281c-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="3281c-112">İkinci komut $slb ' de yük dengeleyiciyi, NewRule adlı bir kuralı ekleyen-AzLoadBalancerRuleConfig öğesini eklemek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="3281c-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="3281c-113">Üçüncü komut yük dengeleyicın **Ayarla-AzLoadBalancerRuleConfig** 'e geçer ve yeni kural yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3281c-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="3281c-114">Yapılandırma, önceki komut tarafından etkinleştirilen bir kayan IP adresini etkinleştirmemektedir.</span><span class="sxs-lookup"><span data-stu-id="3281c-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="3281c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3281c-115">PARAMETERS</span></span>

### <span data-ttu-id="3281c-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3281c-116">-BackendAddressPool</span></span>
<span data-ttu-id="3281c-117">Bir yük dengeleyici kuralıyla ilişkilendirilecek **Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-118">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="3281c-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="3281c-119">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek bir **Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-120">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="3281c-120">-BackendPort</span></span>
<span data-ttu-id="3281c-121">Bu kural yapılandırmasıyla eşleşen trafik için arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3281c-122">-DefaultProfile</span></span>
<span data-ttu-id="3281c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3281c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="3281c-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="3281c-125">Arka uç havuzundaki VM 'Ler için SNAT 'yi, Yük Dengeleme kuralının ön uç alanında belirtilen Publicıp adresini kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="3281c-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-126">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="3281c-126">-EnableFloatingIP</span></span>
<span data-ttu-id="3281c-127">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3281c-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-128">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="3281c-128">-EnableTcpReset</span></span>
<span data-ttu-id="3281c-129">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="3281c-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="3281c-130">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3281c-130">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-131">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="3281c-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="3281c-132">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-133">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="3281c-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="3281c-134">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-134">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-135">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="3281c-135">-FrontendPort</span></span>
<span data-ttu-id="3281c-136">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-137">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="3281c-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3281c-138">Bir yük dengeleyicide konuşmaları durumunu geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3281c-139">-LoadBalancer</span></span>
<span data-ttu-id="3281c-140">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-140">Specifies a load balancer.</span></span>
<span data-ttu-id="3281c-141">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin bir kural yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3281c-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="3281c-142">-LoadDistribution</span></span>
<span data-ttu-id="3281c-143">Bir yük dağılımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-143">Specifies a load distribution.</span></span>
<span data-ttu-id="3281c-144">Bu parametre için kabul edilebilir değerler: SourceIP ve Sourceıpprotocol.</span><span class="sxs-lookup"><span data-stu-id="3281c-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="3281c-145">-Name</span></span>
<span data-ttu-id="3281c-146">Bir yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-146">Specifies the name of a load balancer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-147">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="3281c-147">-Probe</span></span>
<span data-ttu-id="3281c-148">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-149">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="3281c-149">-ProbeId</span></span>
<span data-ttu-id="3281c-150">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-151">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="3281c-151">-Protocol</span></span>
<span data-ttu-id="3281c-152">Bir yük dengeleyici kuralıyla eşleştirilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3281c-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="3281c-153">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="3281c-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="3281c-154">-Confirm</span></span>
<span data-ttu-id="3281c-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3281c-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3281c-156">-WhatIf</span></span>
<span data-ttu-id="3281c-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3281c-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3281c-158">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3281c-158">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3281c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3281c-159">CommonParameters</span></span>
<span data-ttu-id="3281c-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3281c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3281c-161">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3281c-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3281c-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3281c-162">INPUTS</span></span>

### <span data-ttu-id="3281c-163">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3281c-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="3281c-164">System. String</span><span class="sxs-lookup"><span data-stu-id="3281c-164">System.String</span></span>

### <span data-ttu-id="3281c-165">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3281c-165">System.Int32</span></span>

### <span data-ttu-id="3281c-166">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="3281c-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="3281c-167">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3281c-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="3281c-168">Microsoft. Azure. Commands. Network. modeller. Psaraştırması</span><span class="sxs-lookup"><span data-stu-id="3281c-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="3281c-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3281c-169">OUTPUTS</span></span>

### <span data-ttu-id="3281c-170">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3281c-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3281c-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3281c-171">NOTES</span></span>

## <span data-ttu-id="3281c-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3281c-172">RELATED LINKS</span></span>

[<span data-ttu-id="3281c-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3281c-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3281c-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3281c-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3281c-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3281c-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3281c-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3281c-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3281c-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3281c-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

