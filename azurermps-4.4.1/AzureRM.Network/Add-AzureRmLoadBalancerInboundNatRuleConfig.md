---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: ee0a001894570c66145ac7f75d12451df5faaab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763106"
---
# <span data-ttu-id="1e07c-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e07c-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="1e07c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e07c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e07c-103">Bir yük dengeleyicisine gelen NAT kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="1e07c-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e07c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e07c-104">SYNTAX</span></span>

### <span data-ttu-id="1e07c-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="1e07c-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e07c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1e07c-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e07c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e07c-107">DESCRIPTION</span></span>
<span data-ttu-id="1e07c-108">**Add-Azurermloadbalancerınboundnatruleconfig** cmdlet 'ı bir Azure yük dengeleyicisine gelen ağ adresi ÇEVIRISI (NAT) kuralı yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="1e07c-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="1e07c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e07c-109">EXAMPLES</span></span>

### <span data-ttu-id="1e07c-110">Örnek 1: yük dengeleyicisine gelen NAT kural yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="1e07c-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="1e07c-111">İlk komut MyloadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="1e07c-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="1e07c-112">İkinci komut, yük dengeleyiciyi, yük dengeleyicisine gelen NAT kuralı yapılandırmasını ekleyen **-AzureRmLoadBalancerInboundNatRuleConfig öğesini eklemek** $SLB için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1e07c-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="1e07c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e07c-113">PARAMETERS</span></span>

### <span data-ttu-id="1e07c-114">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="1e07c-114">-BackendPort</span></span>
<span data-ttu-id="1e07c-115">Bir kural yapılandırmasıyla eşleşen trafiğin arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e07c-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e07c-116">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="1e07c-116">-EnableFloatingIP</span></span>
<span data-ttu-id="1e07c-117">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e07c-117">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="1e07c-118">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="1e07c-118">-FrontendIpConfiguration</span></span>
<span data-ttu-id="1e07c-119">Gelen NAT kuralı yapılandırmasıyla ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e07c-119">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e07c-120">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="1e07c-120">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="1e07c-121">Ön uç IP adresi yapılandırması için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e07c-121">Specifies an ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e07c-122">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="1e07c-122">-FrontendPort</span></span>
<span data-ttu-id="1e07c-123">Bir kural yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e07c-123">Specifies the front-end port that is matched by a rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e07c-124">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="1e07c-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1e07c-125">Bir yük dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e07c-125">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e07c-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e07c-126">-LoadBalancer</span></span>
<span data-ttu-id="1e07c-127">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e07c-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="1e07c-128">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine gelen NAT kural yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="1e07c-128">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e07c-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e07c-129">-Name</span></span>
<span data-ttu-id="1e07c-130">Eklenecek gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e07c-130">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="1e07c-131">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="1e07c-131">-Protocol</span></span>
<span data-ttu-id="1e07c-132">Gelen NAT kuralıyla eşleşen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e07c-132">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="1e07c-133">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="1e07c-133">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e07c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e07c-134">-DefaultProfile</span></span>
<span data-ttu-id="1e07c-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e07c-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e07c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e07c-136">CommonParameters</span></span>
<span data-ttu-id="1e07c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e07c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e07c-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e07c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e07c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e07c-139">INPUTS</span></span>

### <span data-ttu-id="1e07c-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e07c-140">PSLoadBalancer</span></span>
<span data-ttu-id="1e07c-141">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1e07c-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="1e07c-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e07c-142">OUTPUTS</span></span>

### <span data-ttu-id="1e07c-143">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e07c-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1e07c-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e07c-144">NOTES</span></span>

## <span data-ttu-id="1e07c-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e07c-145">RELATED LINKS</span></span>

[<span data-ttu-id="1e07c-146">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e07c-146">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="1e07c-147">Get-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="1e07c-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1e07c-148">New-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="1e07c-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1e07c-149">Remove-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="1e07c-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1e07c-150">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e07c-150">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="1e07c-151">Set-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="1e07c-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


