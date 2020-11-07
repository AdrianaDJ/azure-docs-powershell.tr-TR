---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 1cfee59f1432cee5355ae562f8cc732a640d8c2b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932094"
---
# <span data-ttu-id="800cf-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="800cf-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="800cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="800cf-102">SYNOPSIS</span></span>
<span data-ttu-id="800cf-103">Bir yük dengeleyicisine gelen NAT kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="800cf-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="800cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="800cf-104">SYNTAX</span></span>

### <span data-ttu-id="800cf-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="800cf-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="800cf-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="800cf-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="800cf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="800cf-107">DESCRIPTION</span></span>
<span data-ttu-id="800cf-108">**Add-AzLoadBalancerInboundNatRuleConfig** cmdlet 'i, bir Azure yük dengeleyicisine gelen ağ adresi ÇEVIRISI (NAT) kuralı yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="800cf-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="800cf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="800cf-109">EXAMPLES</span></span>

### <span data-ttu-id="800cf-110">Örnek 1: yük dengeleyicisine gelen NAT kural yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="800cf-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="800cf-111">İlk komut MyloadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="800cf-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="800cf-112">İkinci komut, yük dengeleyiciden gelen NAT kuralı yapılandırmasını ekleyen **-AzLoadBalancerInboundNatRuleConfig** öğesini $SLB</span><span class="sxs-lookup"><span data-stu-id="800cf-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="800cf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="800cf-113">PARAMETERS</span></span>

### <span data-ttu-id="800cf-114">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="800cf-114">-BackendPort</span></span>
<span data-ttu-id="800cf-115">Bir kural yapılandırmasıyla eşleşen trafiğin arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="800cf-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="800cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800cf-116">-DefaultProfile</span></span>
<span data-ttu-id="800cf-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="800cf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="800cf-118">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="800cf-118">-EnableFloatingIP</span></span>
<span data-ttu-id="800cf-119">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="800cf-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="800cf-120">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="800cf-120">-EnableTcpReset</span></span>
<span data-ttu-id="800cf-121">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="800cf-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="800cf-122">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="800cf-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="800cf-123">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="800cf-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="800cf-124">Gelen NAT kuralı yapılandırmasıyla ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="800cf-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="800cf-125">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="800cf-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="800cf-126">Ön uç IP adresi yapılandırması için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="800cf-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="800cf-127">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="800cf-127">-FrontendPort</span></span>
<span data-ttu-id="800cf-128">Bir kural yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="800cf-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="800cf-129">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="800cf-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="800cf-130">Bir yük dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="800cf-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="800cf-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="800cf-131">-LoadBalancer</span></span>
<span data-ttu-id="800cf-132">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="800cf-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="800cf-133">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine gelen NAT kural yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="800cf-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="800cf-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="800cf-134">-Name</span></span>
<span data-ttu-id="800cf-135">Eklenecek gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="800cf-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="800cf-136">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="800cf-136">-Protocol</span></span>
<span data-ttu-id="800cf-137">Gelen NAT kuralıyla eşleşen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="800cf-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="800cf-138">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="800cf-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="800cf-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="800cf-139">-Confirm</span></span>
<span data-ttu-id="800cf-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="800cf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="800cf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="800cf-141">-WhatIf</span></span>
<span data-ttu-id="800cf-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="800cf-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="800cf-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="800cf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="800cf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800cf-144">CommonParameters</span></span>
<span data-ttu-id="800cf-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="800cf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800cf-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="800cf-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800cf-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="800cf-147">INPUTS</span></span>

### <span data-ttu-id="800cf-148">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="800cf-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="800cf-149">System. String</span><span class="sxs-lookup"><span data-stu-id="800cf-149">System.String</span></span>

### <span data-ttu-id="800cf-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="800cf-150">System.Int32</span></span>

### <span data-ttu-id="800cf-151">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="800cf-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="800cf-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="800cf-152">OUTPUTS</span></span>

### <span data-ttu-id="800cf-153">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="800cf-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="800cf-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="800cf-154">NOTES</span></span>

## <span data-ttu-id="800cf-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="800cf-155">RELATED LINKS</span></span>

[<span data-ttu-id="800cf-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="800cf-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="800cf-157">Get-Azloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="800cf-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="800cf-158">New-Azloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="800cf-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="800cf-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="800cf-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="800cf-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="800cf-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="800cf-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="800cf-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)

