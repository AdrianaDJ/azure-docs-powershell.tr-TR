---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 2b9c835e99a088a075656cd985004663e5ef094a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589235"
---
# <span data-ttu-id="fdc53-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fdc53-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="fdc53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdc53-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc53-103">Bir yük dengeleyici kuralı yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fdc53-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdc53-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fdc53-104">SYNTAX</span></span>

### <span data-ttu-id="fdc53-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="fdc53-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdc53-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fdc53-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdc53-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fdc53-107">DESCRIPTION</span></span>
<span data-ttu-id="fdc53-108">**Set-AzureRmLoadBalancerRuleConfig** cmdlet 'i, yük dengeleyici kuralı yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fdc53-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="fdc53-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fdc53-109">EXAMPLES</span></span>

### <span data-ttu-id="fdc53-110">Örnek 1: Yük Dengeleme kuralı yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="fdc53-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="fdc53-111">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fdc53-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="fdc53-112">İkinci komut, seri düzen işlecini kullanarak, yeni bir kural olan Add-AzureRmLoadBalancerRuleConfig öğesini eklemek için $slb.</span><span class="sxs-lookup"><span data-stu-id="fdc53-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="fdc53-113">Üçüncü komut, yükleme dengeleyicisine, yeni kural yapılandırmasını ayarlayan **-AzureRmLoadBalancerRuleConfig** değerini geçirir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="fdc53-114">Yapılandırma, önceki komut tarafından etkinleştirilen bir kayan IP adresini etkinleştirmemektedir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="fdc53-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fdc53-115">PARAMETERS</span></span>

### <span data-ttu-id="fdc53-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fdc53-116">-BackendAddressPool</span></span>
<span data-ttu-id="fdc53-117">Bir yük dengeleyici kuralıyla ilişkilendirilecek **Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc53-118">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="fdc53-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="fdc53-119">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek bir **Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fdc53-120">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="fdc53-120">-BackendPort</span></span>
<span data-ttu-id="fdc53-121">Bu kural yapılandırmasıyla eşleşen trafik için arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="fdc53-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="fdc53-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="fdc53-123">Arka uç havuzundaki VM 'Ler için SNAT 'yi, Yük Dengeleme kuralının ön uç alanında belirtilen Publicıp adresini kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="fdc53-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="fdc53-124">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="fdc53-124">-EnableFloatingIP</span></span>
<span data-ttu-id="fdc53-125">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="fdc53-126">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="fdc53-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="fdc53-127">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fdc53-128">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="fdc53-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="fdc53-129">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="fdc53-130">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="fdc53-130">-FrontendPort</span></span>
<span data-ttu-id="fdc53-131">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fdc53-132">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="fdc53-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="fdc53-133">Bir yük dengeleyicide konuşmaları durumunu geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="fdc53-134">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fdc53-134">-LoadBalancer</span></span>
<span data-ttu-id="fdc53-135">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-135">Specifies a load balancer.</span></span>
<span data-ttu-id="fdc53-136">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin hedef durum kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fdc53-136">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="fdc53-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="fdc53-137">-LoadDistribution</span></span>
<span data-ttu-id="fdc53-138">Bir yük dağılımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-138">Specifies a load distribution.</span></span>
<span data-ttu-id="fdc53-139">Bu parametre için kabul edilebilir değerler: SourceIP ve Sourceıpprotocol.</span><span class="sxs-lookup"><span data-stu-id="fdc53-139">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc53-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="fdc53-140">-Name</span></span>
<span data-ttu-id="fdc53-141">Bir yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-141">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="fdc53-142">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="fdc53-142">-Probe</span></span>
<span data-ttu-id="fdc53-143">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdc53-144">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="fdc53-144">-ProbeId</span></span>
<span data-ttu-id="fdc53-145">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fdc53-146">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="fdc53-146">-Protocol</span></span>
<span data-ttu-id="fdc53-147">Bir yük dengeleyici kuralıyla eşleştirilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdc53-147">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="fdc53-148">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="fdc53-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="fdc53-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc53-149">-DefaultProfile</span></span>
<span data-ttu-id="fdc53-150">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fdc53-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdc53-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc53-151">CommonParameters</span></span>
<span data-ttu-id="fdc53-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fdc53-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc53-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdc53-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc53-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fdc53-154">INPUTS</span></span>

### <span data-ttu-id="fdc53-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fdc53-155">PSLoadBalancer</span></span>
<span data-ttu-id="fdc53-156">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fdc53-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="fdc53-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fdc53-157">OUTPUTS</span></span>

### <span data-ttu-id="fdc53-158">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fdc53-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fdc53-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fdc53-159">NOTES</span></span>

## <span data-ttu-id="fdc53-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fdc53-160">RELATED LINKS</span></span>

[<span data-ttu-id="fdc53-161">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fdc53-161">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="fdc53-162">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fdc53-162">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="fdc53-163">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fdc53-163">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="fdc53-164">Yeni-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fdc53-164">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="fdc53-165">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fdc53-165">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


