---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: acc741bc038e7fe3a9612e2bc6b4e9abe6bab800
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592058"
---
# <span data-ttu-id="1ae83-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ae83-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="1ae83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ae83-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae83-103">Bir yük dengeleyici kuralı yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1ae83-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ae83-104">SYNTAX</span></span>

### <span data-ttu-id="1ae83-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="1ae83-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ae83-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1ae83-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ae83-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ae83-107">DESCRIPTION</span></span>
<span data-ttu-id="1ae83-108">**Set-AzureRmLoadBalancerRuleConfig** cmdlet 'i, yük dengeleyici kuralı yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1ae83-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="1ae83-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ae83-109">EXAMPLES</span></span>

### <span data-ttu-id="1ae83-110">Örnek 1: Yük Dengeleme kuralı yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="1ae83-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="1ae83-111">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1ae83-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="1ae83-112">İkinci komut, seri düzen işlecini kullanarak, yeni bir kural olan Add-AzureRmLoadBalancerRuleConfig öğesini eklemek için $slb.</span><span class="sxs-lookup"><span data-stu-id="1ae83-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="1ae83-113">Üçüncü komut, yükleme dengeleyicisine, yeni kural yapılandırmasını ayarlayan **-AzureRmLoadBalancerRuleConfig** değerini geçirir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="1ae83-114">Yapılandırma, önceki komut tarafından etkinleştirilen bir kayan IP adresini etkinleştirmemektedir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="1ae83-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ae83-115">PARAMETERS</span></span>

### <span data-ttu-id="1ae83-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1ae83-116">-BackendAddressPool</span></span>
<span data-ttu-id="1ae83-117">Bir yük dengeleyici kuralıyla ilişkilendirilecek **Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="1ae83-118">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="1ae83-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="1ae83-119">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek bir **Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1ae83-120">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="1ae83-120">-BackendPort</span></span>
<span data-ttu-id="1ae83-121">Bu kural yapılandırmasıyla eşleşen trafik için arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="1ae83-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae83-122">-DefaultProfile</span></span>
<span data-ttu-id="1ae83-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ae83-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ae83-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="1ae83-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="1ae83-125">Arka uç havuzundaki VM 'Ler için SNAT 'yi, Yük Dengeleme kuralının ön uç alanında belirtilen Publicıp adresini kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="1ae83-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="1ae83-126">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="1ae83-126">-EnableFloatingIP</span></span>
<span data-ttu-id="1ae83-127">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="1ae83-128">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="1ae83-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="1ae83-129">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1ae83-130">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="1ae83-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="1ae83-131">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-131">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="1ae83-132">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="1ae83-132">-FrontendPort</span></span>
<span data-ttu-id="1ae83-133">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1ae83-134">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="1ae83-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1ae83-135">Bir yük dengeleyicide konuşmaları durumunu geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="1ae83-136">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1ae83-136">-LoadBalancer</span></span>
<span data-ttu-id="1ae83-137">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-137">Specifies a load balancer.</span></span>
<span data-ttu-id="1ae83-138">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin hedef durum kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1ae83-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="1ae83-139">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="1ae83-139">-LoadDistribution</span></span>
<span data-ttu-id="1ae83-140">Bir yük dağılımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-140">Specifies a load distribution.</span></span>
<span data-ttu-id="1ae83-141">Bu parametre için kabul edilebilir değerler: SourceIP ve Sourceıpprotocol.</span><span class="sxs-lookup"><span data-stu-id="1ae83-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="1ae83-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ae83-142">-Name</span></span>
<span data-ttu-id="1ae83-143">Bir yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-143">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="1ae83-144">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="1ae83-144">-Probe</span></span>
<span data-ttu-id="1ae83-145">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1ae83-146">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="1ae83-146">-ProbeId</span></span>
<span data-ttu-id="1ae83-147">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1ae83-148">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="1ae83-148">-Protocol</span></span>
<span data-ttu-id="1ae83-149">Bir yük dengeleyici kuralıyla eşleştirilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae83-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="1ae83-150">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="1ae83-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="1ae83-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae83-151">CommonParameters</span></span>
<span data-ttu-id="1ae83-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ae83-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae83-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae83-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae83-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ae83-154">INPUTS</span></span>

### <span data-ttu-id="1ae83-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1ae83-155">PSLoadBalancer</span></span>
<span data-ttu-id="1ae83-156">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1ae83-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="1ae83-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ae83-157">OUTPUTS</span></span>

### <span data-ttu-id="1ae83-158">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1ae83-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1ae83-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ae83-159">NOTES</span></span>

## <span data-ttu-id="1ae83-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ae83-160">RELATED LINKS</span></span>

[<span data-ttu-id="1ae83-161">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ae83-161">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="1ae83-162">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ae83-162">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="1ae83-163">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ae83-163">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="1ae83-164">Yeni-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ae83-164">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="1ae83-165">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ae83-165">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

