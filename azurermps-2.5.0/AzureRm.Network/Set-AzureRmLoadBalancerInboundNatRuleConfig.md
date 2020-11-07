---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: e79ff19e23d7e599dd783e4bb9c4c12d13f943f3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939885"
---
# <span data-ttu-id="e880c-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e880c-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="e880c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e880c-102">SYNOPSIS</span></span>
<span data-ttu-id="e880c-103">Bir yük dengeleyici için gelen NAT kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e880c-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e880c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e880c-104">SYNTAX</span></span>

### <span data-ttu-id="e880c-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="e880c-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e880c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e880c-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e880c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e880c-107">DESCRIPTION</span></span>
<span data-ttu-id="e880c-108">**Set-Azurermloadbalancerınboundnatruleconfig** cmdlet 'i, bir Azure yük dengeleyicisi için gelen ağ adresi ÇEVIRI (NAT) kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e880c-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e880c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e880c-109">EXAMPLES</span></span>

### <span data-ttu-id="e880c-110">Örnek 1: yük dengeleyicide gelen NAT kural yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="e880c-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="e880c-111">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e880c-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="e880c-112">İkinci $slb komut, bir gelen NAT kural yapılandırması ekleyen-AzureRmLoadBalancerInboundNatRuleConfig öğesini ekleme</span><span class="sxs-lookup"><span data-stu-id="e880c-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="e880c-113">Üçüncü komut, yük dengeleyiciden gelen NAT kuralı yapılandırmasını kaydeden ve güncelleştiren **-Azurermloadbalancerınboundnatruleconfig** 'i geçirir.</span><span class="sxs-lookup"><span data-stu-id="e880c-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="e880c-114">Kural yapılandırmasının, önceki komut tarafından etkinleştirilen kayan IP 'yi etkinleştirmeden ayarlandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e880c-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="e880c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e880c-115">PARAMETERS</span></span>

### <span data-ttu-id="e880c-116">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="e880c-116">-BackendPort</span></span>
<span data-ttu-id="e880c-117">Bu kural yapılandırmasıyla eşleşen trafik için arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e880c-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="e880c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e880c-118">-DefaultProfile</span></span>
<span data-ttu-id="e880c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e880c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e880c-120">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="e880c-120">-EnableFloatingIP</span></span>
<span data-ttu-id="e880c-121">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e880c-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="e880c-122">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="e880c-122">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e880c-123">Gelen NAT kuralı yapılandırmasıyla ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e880c-123">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="e880c-124">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="e880c-124">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="e880c-125">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e880c-125">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="e880c-126">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="e880c-126">-FrontendPort</span></span>
<span data-ttu-id="e880c-127">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e880c-127">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e880c-128">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="e880c-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e880c-129">Bir yük dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="e880c-129">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="e880c-130">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e880c-130">-LoadBalancer</span></span>
<span data-ttu-id="e880c-131">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="e880c-131">Specifies a load balancer.</span></span>
<span data-ttu-id="e880c-132">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin gelen NAT kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e880c-132">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="e880c-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="e880c-133">-Name</span></span>
<span data-ttu-id="e880c-134">Gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e880c-134">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="e880c-135">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="e880c-135">-Protocol</span></span>
<span data-ttu-id="e880c-136">Gelen NAT kuralı yapılandırmasıyla eşleşen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e880c-136">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="e880c-137">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="e880c-137">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="e880c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e880c-138">CommonParameters</span></span>
<span data-ttu-id="e880c-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e880c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e880c-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e880c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e880c-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e880c-141">INPUTS</span></span>

### <span data-ttu-id="e880c-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e880c-142">PSLoadBalancer</span></span>
<span data-ttu-id="e880c-143">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e880c-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e880c-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e880c-144">OUTPUTS</span></span>

### <span data-ttu-id="e880c-145">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e880c-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e880c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e880c-146">NOTES</span></span>

## <span data-ttu-id="e880c-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e880c-147">RELATED LINKS</span></span>

[<span data-ttu-id="e880c-148">Add-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="e880c-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e880c-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e880c-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="e880c-150">Get-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="e880c-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e880c-151">New-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="e880c-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e880c-152">Remove-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="e880c-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


