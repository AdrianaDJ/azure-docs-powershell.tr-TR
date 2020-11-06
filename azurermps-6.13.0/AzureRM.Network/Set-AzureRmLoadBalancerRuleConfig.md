---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: a584d473354fd900b117f5661dc738b239f3a92d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591345"
---
# <span data-ttu-id="720b7-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="720b7-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="720b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="720b7-102">SYNOPSIS</span></span>
<span data-ttu-id="720b7-103">Bir yük dengeleyici kuralı yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="720b7-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="720b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="720b7-104">SYNTAX</span></span>

### <span data-ttu-id="720b7-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="720b7-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="720b7-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="720b7-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="720b7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="720b7-107">DESCRIPTION</span></span>
<span data-ttu-id="720b7-108">**Set-AzureRmLoadBalancerRuleConfig** cmdlet 'i, yük dengeleyici kuralı yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="720b7-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="720b7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="720b7-109">EXAMPLES</span></span>

### <span data-ttu-id="720b7-110">Örnek 1: Yük Dengeleme kuralı yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="720b7-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="720b7-111">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="720b7-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="720b7-112">İkinci komut, seri düzen işlecini kullanarak, yeni bir kural olan Add-AzureRmLoadBalancerRuleConfig öğesini eklemek için $slb.</span><span class="sxs-lookup"><span data-stu-id="720b7-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="720b7-113">Üçüncü komut, yükleme dengeleyicisine, yeni kural yapılandırmasını ayarlayan **-AzureRmLoadBalancerRuleConfig** değerini geçirir.</span><span class="sxs-lookup"><span data-stu-id="720b7-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="720b7-114">Yapılandırma, önceki komut tarafından etkinleştirilen bir kayan IP adresini etkinleştirmemektedir.</span><span class="sxs-lookup"><span data-stu-id="720b7-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="720b7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="720b7-115">PARAMETERS</span></span>

### <span data-ttu-id="720b7-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="720b7-116">-BackendAddressPool</span></span>
<span data-ttu-id="720b7-117">Bir yük dengeleyici kuralıyla ilişkilendirilecek **Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="720b7-118">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="720b7-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="720b7-119">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek bir **Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="720b7-120">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="720b7-120">-BackendPort</span></span>
<span data-ttu-id="720b7-121">Bu kural yapılandırmasıyla eşleşen trafik için arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="720b7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="720b7-122">-DefaultProfile</span></span>
<span data-ttu-id="720b7-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="720b7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="720b7-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="720b7-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="720b7-125">Arka uç havuzundaki VM 'Ler için SNAT 'yi, Yük Dengeleme kuralının ön uç alanında belirtilen Publicıp adresini kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="720b7-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="720b7-126">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="720b7-126">-EnableFloatingIP</span></span>
<span data-ttu-id="720b7-127">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="720b7-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="720b7-128">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="720b7-128">-EnableTcpReset</span></span>
<span data-ttu-id="720b7-129">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="720b7-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="720b7-130">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="720b7-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="720b7-131">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="720b7-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="720b7-132">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="720b7-133">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="720b7-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="720b7-134">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="720b7-135">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="720b7-135">-FrontendPort</span></span>
<span data-ttu-id="720b7-136">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="720b7-137">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="720b7-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="720b7-138">Bir yük dengeleyicide konuşmaları durumunu geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="720b7-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="720b7-139">-LoadBalancer</span></span>
<span data-ttu-id="720b7-140">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-140">Specifies a load balancer.</span></span>
<span data-ttu-id="720b7-141">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin hedef durum kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="720b7-141">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="720b7-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="720b7-142">-LoadDistribution</span></span>
<span data-ttu-id="720b7-143">Bir yük dağılımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-143">Specifies a load distribution.</span></span>
<span data-ttu-id="720b7-144">Bu parametre için kabul edilebilir değerler: SourceIP ve Sourceıpprotocol.</span><span class="sxs-lookup"><span data-stu-id="720b7-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="720b7-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="720b7-145">-Name</span></span>
<span data-ttu-id="720b7-146">Bir yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="720b7-147">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="720b7-147">-Probe</span></span>
<span data-ttu-id="720b7-148">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="720b7-149">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="720b7-149">-ProbeId</span></span>
<span data-ttu-id="720b7-150">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="720b7-151">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="720b7-151">-Protocol</span></span>
<span data-ttu-id="720b7-152">Bir yük dengeleyici kuralıyla eşleştirilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b7-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="720b7-153">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="720b7-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="720b7-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="720b7-154">-Confirm</span></span>
<span data-ttu-id="720b7-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="720b7-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="720b7-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="720b7-156">-WhatIf</span></span>
<span data-ttu-id="720b7-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="720b7-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="720b7-158">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="720b7-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="720b7-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="720b7-159">CommonParameters</span></span>
<span data-ttu-id="720b7-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="720b7-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="720b7-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="720b7-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="720b7-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="720b7-162">INPUTS</span></span>

### <span data-ttu-id="720b7-163">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="720b7-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="720b7-164">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="720b7-164">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="720b7-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="720b7-165">OUTPUTS</span></span>

### <span data-ttu-id="720b7-166">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="720b7-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="720b7-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="720b7-167">NOTES</span></span>

## <span data-ttu-id="720b7-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="720b7-168">RELATED LINKS</span></span>

[<span data-ttu-id="720b7-169">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="720b7-169">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="720b7-170">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="720b7-170">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="720b7-171">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="720b7-171">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="720b7-172">Yeni-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="720b7-172">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="720b7-173">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="720b7-173">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


