---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: c7d0d5879b4c0ca7ee92a9f22d062241e1cb89a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590125"
---
# <span data-ttu-id="6ac4f-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6ac4f-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="6ac4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ac4f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac4f-103">Bir yük dengeleyici için gelen NAT kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ac4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ac4f-104">SYNTAX</span></span>

### <span data-ttu-id="6ac4f-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ac4f-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ac4f-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="6ac4f-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ac4f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ac4f-107">DESCRIPTION</span></span>
<span data-ttu-id="6ac4f-108">**Set-Azurermloadbalancerınboundnatruleconfig** cmdlet 'i, bir Azure yük dengeleyicisi için gelen ağ adresi ÇEVIRI (NAT) kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="6ac4f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ac4f-109">EXAMPLES</span></span>

### <span data-ttu-id="6ac4f-110">Örnek 1: yük dengeleyicide gelen NAT kural yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="6ac4f-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="6ac4f-111">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="6ac4f-112">İkinci $slb komut, bir gelen NAT kural yapılandırması ekleyen-AzureRmLoadBalancerInboundNatRuleConfig öğesini ekleme</span><span class="sxs-lookup"><span data-stu-id="6ac4f-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="6ac4f-113">Üçüncü komut, yük dengeleyiciden gelen NAT kuralı yapılandırmasını kaydeden ve güncelleştiren **-Azurermloadbalancerınboundnatruleconfig** 'i geçirir.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="6ac4f-114">Kural yapılandırmasının, önceki komut tarafından etkinleştirilen kayan IP 'yi etkinleştirmeden ayarlandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="6ac4f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ac4f-115">PARAMETERS</span></span>

### <span data-ttu-id="6ac4f-116">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="6ac4f-116">-BackendPort</span></span>
<span data-ttu-id="6ac4f-117">Bu kural yapılandırmasıyla eşleşen trafik için arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="6ac4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac4f-118">-DefaultProfile</span></span>
<span data-ttu-id="6ac4f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac4f-120">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="6ac4f-120">-EnableFloatingIP</span></span>
<span data-ttu-id="6ac4f-121">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6ac4f-122">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="6ac4f-122">-EnableTcpReset</span></span>
<span data-ttu-id="6ac4f-123">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="6ac4f-124">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="6ac4f-125">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="6ac4f-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6ac4f-126">Gelen NAT kuralı yapılandırmasıyla ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="6ac4f-127">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="6ac4f-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6ac4f-128">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6ac4f-129">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="6ac4f-129">-FrontendPort</span></span>
<span data-ttu-id="6ac4f-130">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6ac4f-131">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="6ac4f-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6ac4f-132">Bir yük dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="6ac4f-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ac4f-133">-LoadBalancer</span></span>
<span data-ttu-id="6ac4f-134">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-134">Specifies a load balancer.</span></span>
<span data-ttu-id="6ac4f-135">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin gelen NAT kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="6ac4f-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ac4f-136">-Name</span></span>
<span data-ttu-id="6ac4f-137">Gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="6ac4f-138">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="6ac4f-138">-Protocol</span></span>
<span data-ttu-id="6ac4f-139">Gelen NAT kuralı yapılandırmasıyla eşleşen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="6ac4f-140">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="6ac4f-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ac4f-141">-Confirm</span></span>
<span data-ttu-id="6ac4f-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ac4f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ac4f-143">-WhatIf</span></span>
<span data-ttu-id="6ac4f-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ac4f-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ac4f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac4f-146">CommonParameters</span></span>
<span data-ttu-id="6ac4f-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ac4f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac4f-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac4f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac4f-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ac4f-149">INPUTS</span></span>

### <span data-ttu-id="6ac4f-150">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ac4f-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="6ac4f-151">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6ac4f-151">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="6ac4f-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ac4f-152">OUTPUTS</span></span>

### <span data-ttu-id="6ac4f-153">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ac4f-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6ac4f-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ac4f-154">NOTES</span></span>

## <span data-ttu-id="6ac4f-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ac4f-155">RELATED LINKS</span></span>

[<span data-ttu-id="6ac4f-156">Add-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="6ac4f-156">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6ac4f-157">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ac4f-157">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="6ac4f-158">Get-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="6ac4f-158">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6ac4f-159">New-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="6ac4f-159">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6ac4f-160">Remove-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="6ac4f-160">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


