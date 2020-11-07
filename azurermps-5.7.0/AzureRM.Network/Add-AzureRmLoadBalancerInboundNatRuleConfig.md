---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 8e055df66c0623fbddbed8379cb25f165efb7081
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763035"
---
# <span data-ttu-id="23e0c-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="23e0c-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="23e0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="23e0c-103">Bir yük dengeleyicisine gelen NAT kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="23e0c-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23e0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23e0c-104">SYNTAX</span></span>

### <span data-ttu-id="23e0c-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="23e0c-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23e0c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="23e0c-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23e0c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="23e0c-107">DESCRIPTION</span></span>
<span data-ttu-id="23e0c-108">**Add-Azurermloadbalancerınboundnatruleconfig** cmdlet 'ı bir Azure yük dengeleyicisine gelen ağ adresi ÇEVIRISI (NAT) kuralı yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="23e0c-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="23e0c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23e0c-109">EXAMPLES</span></span>

### <span data-ttu-id="23e0c-110">Örnek 1: yük dengeleyicisine gelen NAT kural yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="23e0c-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="23e0c-111">İlk komut MyloadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="23e0c-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="23e0c-112">İkinci komut, yük dengeleyiciyi, yük dengeleyicisine gelen NAT kuralı yapılandırmasını ekleyen **-AzureRmLoadBalancerInboundNatRuleConfig öğesini eklemek** $SLB için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="23e0c-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="23e0c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23e0c-113">PARAMETERS</span></span>

### <span data-ttu-id="23e0c-114">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="23e0c-114">-BackendPort</span></span>
<span data-ttu-id="23e0c-115">Bir kural yapılandırmasıyla eşleşen trafiğin arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23e0c-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e0c-116">-DefaultProfile</span></span>
<span data-ttu-id="23e0c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23e0c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0c-118">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="23e0c-118">-EnableFloatingIP</span></span>
<span data-ttu-id="23e0c-119">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="23e0c-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0c-120">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="23e0c-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="23e0c-121">Gelen NAT kuralı yapılandırmasıyla ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23e0c-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0c-122">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="23e0c-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="23e0c-123">Ön uç IP adresi yapılandırması için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="23e0c-123">Specifies an ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0c-124">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="23e0c-124">-FrontendPort</span></span>
<span data-ttu-id="23e0c-125">Bir kural yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23e0c-125">Specifies the front-end port that is matched by a rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0c-126">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="23e0c-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="23e0c-127">Bir yük dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="23e0c-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0c-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="23e0c-128">-LoadBalancer</span></span>
<span data-ttu-id="23e0c-129">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23e0c-129">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="23e0c-130">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine gelen NAT kural yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="23e0c-130">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23e0c-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="23e0c-131">-Name</span></span>
<span data-ttu-id="23e0c-132">Eklenecek gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23e0c-132">Specifies the name of the inbound NAT rule configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0c-133">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="23e0c-133">-Protocol</span></span>
<span data-ttu-id="23e0c-134">Gelen NAT kuralıyla eşleşen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="23e0c-134">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="23e0c-135">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="23e0c-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e0c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e0c-136">CommonParameters</span></span>
<span data-ttu-id="23e0c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23e0c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e0c-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23e0c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e0c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23e0c-139">INPUTS</span></span>

### <span data-ttu-id="23e0c-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="23e0c-140">PSLoadBalancer</span></span>
<span data-ttu-id="23e0c-141">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="23e0c-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="23e0c-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23e0c-142">OUTPUTS</span></span>

### <span data-ttu-id="23e0c-143">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="23e0c-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="23e0c-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23e0c-144">NOTES</span></span>

## <span data-ttu-id="23e0c-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23e0c-145">RELATED LINKS</span></span>

[<span data-ttu-id="23e0c-146">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="23e0c-146">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="23e0c-147">Get-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="23e0c-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="23e0c-148">New-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="23e0c-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="23e0c-149">Remove-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="23e0c-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="23e0c-150">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="23e0c-150">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="23e0c-151">Set-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="23e0c-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


