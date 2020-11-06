---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 004180f2369616654741df960a56a9f9c5bb6047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589245"
---
# <span data-ttu-id="b3660-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b3660-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="b3660-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3660-102">SYNOPSIS</span></span>
<span data-ttu-id="b3660-103">Bir yük dengeleyici için gelen NAT kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b3660-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3660-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3660-104">SYNTAX</span></span>

### <span data-ttu-id="b3660-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="b3660-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3660-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b3660-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3660-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3660-107">DESCRIPTION</span></span>
<span data-ttu-id="b3660-108">**Set-Azurermloadbalancerınboundnatruleconfig** cmdlet 'i, bir Azure yük dengeleyicisi için gelen ağ adresi ÇEVIRI (NAT) kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b3660-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="b3660-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3660-109">EXAMPLES</span></span>

### <span data-ttu-id="b3660-110">Örnek 1: yük dengeleyicide gelen NAT kural yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="b3660-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="b3660-111">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b3660-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="b3660-112">İkinci $slb komut, bir gelen NAT kural yapılandırması ekleyen-AzureRmLoadBalancerInboundNatRuleConfig öğesini ekleme</span><span class="sxs-lookup"><span data-stu-id="b3660-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="b3660-113">Üçüncü komut, yük dengeleyiciden gelen NAT kuralı yapılandırmasını kaydeden ve güncelleştiren **-Azurermloadbalancerınboundnatruleconfig** 'i geçirir.</span><span class="sxs-lookup"><span data-stu-id="b3660-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="b3660-114">Kural yapılandırmasının, önceki komut tarafından etkinleştirilen kayan IP 'yi etkinleştirmeden ayarlandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="b3660-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="b3660-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3660-115">PARAMETERS</span></span>

### <span data-ttu-id="b3660-116">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="b3660-116">-BackendPort</span></span>
<span data-ttu-id="b3660-117">Bu kural yapılandırmasıyla eşleşen trafik için arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3660-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="b3660-118">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="b3660-118">-EnableFloatingIP</span></span>
<span data-ttu-id="b3660-119">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3660-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="b3660-120">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="b3660-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b3660-121">Gelen NAT kuralı yapılandırmasıyla ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3660-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="b3660-122">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="b3660-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="b3660-123">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3660-123">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="b3660-124">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="b3660-124">-FrontendPort</span></span>
<span data-ttu-id="b3660-125">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3660-125">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b3660-126">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="b3660-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b3660-127">Bir yük dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3660-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="b3660-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3660-128">-LoadBalancer</span></span>
<span data-ttu-id="b3660-129">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3660-129">Specifies a load balancer.</span></span>
<span data-ttu-id="b3660-130">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin gelen NAT kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b3660-130">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b3660-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3660-131">-Name</span></span>
<span data-ttu-id="b3660-132">Gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3660-132">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="b3660-133">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="b3660-133">-Protocol</span></span>
<span data-ttu-id="b3660-134">Gelen NAT kuralı yapılandırmasıyla eşleşen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3660-134">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="b3660-135">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="b3660-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="b3660-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3660-136">-DefaultProfile</span></span>
<span data-ttu-id="b3660-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3660-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3660-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3660-138">CommonParameters</span></span>
<span data-ttu-id="b3660-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3660-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3660-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3660-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3660-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3660-141">INPUTS</span></span>

### <span data-ttu-id="b3660-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3660-142">PSLoadBalancer</span></span>
<span data-ttu-id="b3660-143">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b3660-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b3660-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3660-144">OUTPUTS</span></span>

### <span data-ttu-id="b3660-145">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3660-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b3660-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3660-146">NOTES</span></span>

## <span data-ttu-id="b3660-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3660-147">RELATED LINKS</span></span>

[<span data-ttu-id="b3660-148">Add-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="b3660-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b3660-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3660-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b3660-150">Get-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="b3660-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b3660-151">New-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="b3660-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b3660-152">Remove-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="b3660-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


