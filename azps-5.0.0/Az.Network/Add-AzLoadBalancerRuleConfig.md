---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277044"
---
# <span data-ttu-id="b83f9-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b83f9-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="b83f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b83f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b83f9-103">Yük dengeleyicisine bir kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="b83f9-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="b83f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b83f9-104">SYNTAX</span></span>

### <span data-ttu-id="b83f9-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b83f9-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b83f9-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="b83f9-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b83f9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b83f9-107">DESCRIPTION</span></span>
<span data-ttu-id="b83f9-108">**Add-AzLoadBalancerRuleConfig** cmdlet 'ı bir Azure yük dengeleyicisine bir kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="b83f9-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="b83f9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b83f9-109">EXAMPLES</span></span>

### <span data-ttu-id="b83f9-110">Örnek 1: yük dengeleyicisine kural yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="b83f9-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="b83f9-111">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b83f9-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="b83f9-112">İkinci $slb komut, (NewRule adlı kural yapılandırmasını ekleyen **-AzLoadBalancerRuleConfig öğesini ekleme**</span><span class="sxs-lookup"><span data-stu-id="b83f9-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="b83f9-113">Üçüncü komut, yeni yük dengeleyici kuralı yapılandırması ile Azure 'daki yük dengeleyiciyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="b83f9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b83f9-114">PARAMETERS</span></span>

### <span data-ttu-id="b83f9-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b83f9-115">-BackendAddressPool</span></span>
<span data-ttu-id="b83f9-116">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b83f9-117">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="b83f9-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="b83f9-118">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek bir **Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b83f9-119">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="b83f9-119">-BackendPort</span></span>
<span data-ttu-id="b83f9-120">Yük dengeleyici kuralı yapılandırması ile eşleşen trafik için arka uç bağlantı noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b83f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b83f9-121">-DefaultProfile</span></span>
<span data-ttu-id="b83f9-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b83f9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b83f9-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="b83f9-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="b83f9-124">Arka uç havuzundaki VM 'Ler için SNAT 'yi, Yük Dengeleme kuralının ön uç alanında belirtilen Publicıp adresini kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="b83f9-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="b83f9-125">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="b83f9-125">-EnableFloatingIP</span></span>
<span data-ttu-id="b83f9-126">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="b83f9-127">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="b83f9-127">-EnableTcpReset</span></span>
<span data-ttu-id="b83f9-128">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="b83f9-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="b83f9-129">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b83f9-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b83f9-130">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="b83f9-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b83f9-131">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b83f9-132">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="b83f9-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="b83f9-133">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="b83f9-134">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="b83f9-134">-FrontendPort</span></span>
<span data-ttu-id="b83f9-135">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b83f9-136">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="b83f9-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b83f9-137">Yükleme dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="b83f9-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b83f9-138">-LoadBalancer</span></span>
<span data-ttu-id="b83f9-139">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="b83f9-140">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine bir kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="b83f9-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b83f9-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="b83f9-141">-LoadDistribution</span></span>
<span data-ttu-id="b83f9-142">Bir yük dağılımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="b83f9-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="b83f9-143">-Name</span></span>
<span data-ttu-id="b83f9-144">Yük dengeleyici kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b83f9-145">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="b83f9-145">-Probe</span></span>
<span data-ttu-id="b83f9-146">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b83f9-147">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="b83f9-147">-ProbeId</span></span>
<span data-ttu-id="b83f9-148">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b83f9-149">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="b83f9-149">-Protocol</span></span>
<span data-ttu-id="b83f9-150">Bir yük dengeleyici kuralıyla eşleştirilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="b83f9-151">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="b83f9-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="b83f9-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="b83f9-152">-Confirm</span></span>
<span data-ttu-id="b83f9-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b83f9-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b83f9-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b83f9-154">-WhatIf</span></span>
<span data-ttu-id="b83f9-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b83f9-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b83f9-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b83f9-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b83f9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b83f9-157">CommonParameters</span></span>
<span data-ttu-id="b83f9-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b83f9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b83f9-159">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b83f9-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b83f9-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b83f9-160">INPUTS</span></span>

### <span data-ttu-id="b83f9-161">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b83f9-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b83f9-162">System. String</span><span class="sxs-lookup"><span data-stu-id="b83f9-162">System.String</span></span>

### <span data-ttu-id="b83f9-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b83f9-163">System.Int32</span></span>

### <span data-ttu-id="b83f9-164">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="b83f9-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="b83f9-165">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b83f9-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="b83f9-166">Microsoft. Azure. Commands. Network. modeller. Psaraştırması</span><span class="sxs-lookup"><span data-stu-id="b83f9-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="b83f9-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b83f9-167">OUTPUTS</span></span>

### <span data-ttu-id="b83f9-168">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b83f9-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b83f9-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b83f9-169">NOTES</span></span>

## <span data-ttu-id="b83f9-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b83f9-170">RELATED LINKS</span></span>

[<span data-ttu-id="b83f9-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b83f9-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b83f9-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b83f9-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b83f9-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b83f9-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b83f9-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b83f9-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b83f9-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b83f9-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


