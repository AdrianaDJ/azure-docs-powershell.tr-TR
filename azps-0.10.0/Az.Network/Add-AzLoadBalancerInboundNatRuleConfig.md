---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6a699907b70256995973bfdbde4e11b08c594669
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935634"
---
# <span data-ttu-id="6ee1b-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6ee1b-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="6ee1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ee1b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee1b-103">Bir yük dengeleyicisine gelen NAT kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="6ee1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ee1b-104">SYNTAX</span></span>

### <span data-ttu-id="6ee1b-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="6ee1b-105">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ee1b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6ee1b-106">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ee1b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ee1b-107">DESCRIPTION</span></span>
<span data-ttu-id="6ee1b-108">**Add-AzLoadBalancerInboundNatRuleConfig** cmdlet 'i, bir Azure yük dengeleyicisine gelen ağ adresi ÇEVIRISI (NAT) kuralı yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="6ee1b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ee1b-109">EXAMPLES</span></span>

### <span data-ttu-id="6ee1b-110">Örnek 1: yük dengeleyicisine gelen NAT kural yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="6ee1b-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="6ee1b-111">İlk komut MyloadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="6ee1b-112">İkinci komut, yük dengeleyiciden gelen NAT kuralı yapılandırmasını ekleyen **-AzLoadBalancerInboundNatRuleConfig** öğesini $SLB</span><span class="sxs-lookup"><span data-stu-id="6ee1b-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="6ee1b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ee1b-113">PARAMETERS</span></span>

### <span data-ttu-id="6ee1b-114">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="6ee1b-114">-BackendPort</span></span>
<span data-ttu-id="6ee1b-115">Bir kural yapılandırmasıyla eşleşen trafiğin arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="6ee1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee1b-116">-DefaultProfile</span></span>
<span data-ttu-id="6ee1b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ee1b-118">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="6ee1b-118">-EnableFloatingIP</span></span>
<span data-ttu-id="6ee1b-119">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6ee1b-120">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="6ee1b-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6ee1b-121">Gelen NAT kuralı yapılandırmasıyla ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="6ee1b-122">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="6ee1b-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6ee1b-123">Ön uç IP adresi yapılandırması için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-123">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6ee1b-124">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="6ee1b-124">-FrontendPort</span></span>
<span data-ttu-id="6ee1b-125">Bir kural yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-125">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="6ee1b-126">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="6ee1b-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6ee1b-127">Bir yük dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="6ee1b-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ee1b-128">-LoadBalancer</span></span>
<span data-ttu-id="6ee1b-129">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-129">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="6ee1b-130">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine gelen NAT kural yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-130">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="6ee1b-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ee1b-131">-Name</span></span>
<span data-ttu-id="6ee1b-132">Eklenecek gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-132">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="6ee1b-133">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="6ee1b-133">-Protocol</span></span>
<span data-ttu-id="6ee1b-134">Gelen NAT kuralıyla eşleşen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-134">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="6ee1b-135">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="6ee1b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee1b-136">CommonParameters</span></span>
<span data-ttu-id="6ee1b-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ee1b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee1b-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ee1b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee1b-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ee1b-139">INPUTS</span></span>

### <span data-ttu-id="6ee1b-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ee1b-140">PSLoadBalancer</span></span>
<span data-ttu-id="6ee1b-141">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6ee1b-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="6ee1b-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ee1b-142">OUTPUTS</span></span>

### <span data-ttu-id="6ee1b-143">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ee1b-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6ee1b-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ee1b-144">NOTES</span></span>

## <span data-ttu-id="6ee1b-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ee1b-145">RELATED LINKS</span></span>

[<span data-ttu-id="6ee1b-146">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ee1b-146">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6ee1b-147">Get-Azloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="6ee1b-147">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6ee1b-148">New-Azloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="6ee1b-148">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6ee1b-149">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6ee1b-149">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6ee1b-150">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6ee1b-150">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="6ee1b-151">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6ee1b-151">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


