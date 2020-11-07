---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: f566c2b9ac771071a9eb72673edb7e5218656c9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936532"
---
# <span data-ttu-id="6d00f-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d00f-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="6d00f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d00f-102">SYNOPSIS</span></span>
<span data-ttu-id="6d00f-103">Bir yük dengeleyici kuralı yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6d00f-103">Sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="6d00f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d00f-104">SYNTAX</span></span>

### <span data-ttu-id="6d00f-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="6d00f-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d00f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6d00f-106">SetByResource</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d00f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d00f-107">DESCRIPTION</span></span>
<span data-ttu-id="6d00f-108">**Set-AzLoadBalancerRuleConfig** cmdlet 'i, yük dengeleyici kuralı yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6d00f-108">The **Set-AzLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="6d00f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d00f-109">EXAMPLES</span></span>

### <span data-ttu-id="6d00f-110">Örnek 1: Yük Dengeleme kuralı yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="6d00f-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="6d00f-111">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6d00f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="6d00f-112">İkinci komut $slb ' de yük dengeleyiciyi, NewRule adlı bir kuralı ekleyen-AzLoadBalancerRuleConfig öğesini eklemek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="6d00f-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="6d00f-113">Üçüncü komut yük dengeleyicın **Ayarla-AzLoadBalancerRuleConfig** 'e geçer ve yeni kural yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6d00f-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="6d00f-114">Yapılandırma, önceki komut tarafından etkinleştirilen bir kayan IP adresini etkinleştirmemektedir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="6d00f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d00f-115">PARAMETERS</span></span>

### <span data-ttu-id="6d00f-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6d00f-116">-BackendAddressPool</span></span>
<span data-ttu-id="6d00f-117">Bir yük dengeleyici kuralıyla ilişkilendirilecek **Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d00f-118">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="6d00f-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="6d00f-119">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek bir **Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6d00f-120">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="6d00f-120">-BackendPort</span></span>
<span data-ttu-id="6d00f-121">Bu kural yapılandırmasıyla eşleşen trafik için arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="6d00f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d00f-122">-DefaultProfile</span></span>
<span data-ttu-id="6d00f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d00f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d00f-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="6d00f-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="6d00f-125">Arka uç havuzundaki VM 'Ler için SNAT 'yi, Yük Dengeleme kuralının ön uç alanında belirtilen Publicıp adresini kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="6d00f-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="6d00f-126">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="6d00f-126">-EnableFloatingIP</span></span>
<span data-ttu-id="6d00f-127">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6d00f-128">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="6d00f-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6d00f-129">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6d00f-130">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="6d00f-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6d00f-131">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-131">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6d00f-132">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="6d00f-132">-FrontendPort</span></span>
<span data-ttu-id="6d00f-133">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6d00f-134">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="6d00f-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6d00f-135">Bir yük dengeleyicide konuşmaları durumunu geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="6d00f-136">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d00f-136">-LoadBalancer</span></span>
<span data-ttu-id="6d00f-137">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-137">Specifies a load balancer.</span></span>
<span data-ttu-id="6d00f-138">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin hedef durum kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6d00f-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="6d00f-139">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="6d00f-139">-LoadDistribution</span></span>
<span data-ttu-id="6d00f-140">Bir yük dağılımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-140">Specifies a load distribution.</span></span>
<span data-ttu-id="6d00f-141">Bu parametre için kabul edilebilir değerler: SourceIP ve Sourceıpprotocol.</span><span class="sxs-lookup"><span data-stu-id="6d00f-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d00f-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d00f-142">-Name</span></span>
<span data-ttu-id="6d00f-143">Bir yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-143">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="6d00f-144">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="6d00f-144">-Probe</span></span>
<span data-ttu-id="6d00f-145">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d00f-146">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="6d00f-146">-ProbeId</span></span>
<span data-ttu-id="6d00f-147">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6d00f-148">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="6d00f-148">-Protocol</span></span>
<span data-ttu-id="6d00f-149">Bir yük dengeleyici kuralıyla eşleştirilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d00f-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="6d00f-150">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="6d00f-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d00f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d00f-151">CommonParameters</span></span>
<span data-ttu-id="6d00f-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d00f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d00f-153">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d00f-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d00f-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d00f-154">INPUTS</span></span>

### <span data-ttu-id="6d00f-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d00f-155">PSLoadBalancer</span></span>
<span data-ttu-id="6d00f-156">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6d00f-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="6d00f-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d00f-157">OUTPUTS</span></span>

### <span data-ttu-id="6d00f-158">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d00f-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6d00f-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d00f-159">NOTES</span></span>

## <span data-ttu-id="6d00f-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d00f-160">RELATED LINKS</span></span>

[<span data-ttu-id="6d00f-161">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d00f-161">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6d00f-162">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d00f-162">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6d00f-163">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d00f-163">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6d00f-164">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d00f-164">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6d00f-165">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d00f-165">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


