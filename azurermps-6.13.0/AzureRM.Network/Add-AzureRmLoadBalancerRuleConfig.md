---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ed21aec1be522ac145fe255065b650ca4c09dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764947"
---
# <span data-ttu-id="0b942-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b942-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="0b942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b942-102">SYNOPSIS</span></span>
<span data-ttu-id="0b942-103">Yük dengeleyicisine bir kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="0b942-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b942-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b942-104">SYNTAX</span></span>

### <span data-ttu-id="0b942-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b942-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b942-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="0b942-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b942-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b942-107">DESCRIPTION</span></span>
<span data-ttu-id="0b942-108">**Add-AzureRmLoadBalancerRuleConfig** cmdlet 'ı bir Azure yük dengeleyicisine bir kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="0b942-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="0b942-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b942-109">EXAMPLES</span></span>

### <span data-ttu-id="0b942-110">Örnek 1: yük dengeleyicisine kural yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="0b942-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="0b942-111">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="0b942-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="0b942-112">İkinci $slb komut, (NewRule adlı kural yapılandırmasını ekleyen **-AzureRmLoadBalancerRuleConfig öğesini ekleme**</span><span class="sxs-lookup"><span data-stu-id="0b942-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="0b942-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b942-113">PARAMETERS</span></span>

### <span data-ttu-id="0b942-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0b942-114">-BackendAddressPool</span></span>
<span data-ttu-id="0b942-115">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b942-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0b942-116">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="0b942-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="0b942-117">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek bir **Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b942-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0b942-118">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="0b942-118">-BackendPort</span></span>
<span data-ttu-id="0b942-119">Yük dengeleyici kuralı yapılandırması ile eşleşen trafik için arka uç bağlantı noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b942-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0b942-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b942-120">-DefaultProfile</span></span>
<span data-ttu-id="0b942-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b942-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b942-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="0b942-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="0b942-123">Arka uç havuzundaki VM 'Ler için SNAT 'yi, Yük Dengeleme kuralının ön uç alanında belirtilen Publicıp adresini kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0b942-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="0b942-124">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="0b942-124">-EnableFloatingIP</span></span>
<span data-ttu-id="0b942-125">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b942-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="0b942-126">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="0b942-126">-EnableTcpReset</span></span>
<span data-ttu-id="0b942-127">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="0b942-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="0b942-128">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0b942-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="0b942-129">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="0b942-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="0b942-130">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b942-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0b942-131">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="0b942-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="0b942-132">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b942-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="0b942-133">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="0b942-133">-FrontendPort</span></span>
<span data-ttu-id="0b942-134">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b942-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0b942-135">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="0b942-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0b942-136">Yükleme dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b942-136">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="0b942-137">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b942-137">-LoadBalancer</span></span>
<span data-ttu-id="0b942-138">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b942-138">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="0b942-139">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine bir kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="0b942-139">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b942-140">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="0b942-140">-LoadDistribution</span></span>
<span data-ttu-id="0b942-141">Bir yük dağılımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b942-141">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="0b942-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b942-142">-Name</span></span>
<span data-ttu-id="0b942-143">Yük dengeleyici kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b942-143">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0b942-144">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="0b942-144">-Probe</span></span>
<span data-ttu-id="0b942-145">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b942-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0b942-146">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="0b942-146">-ProbeId</span></span>
<span data-ttu-id="0b942-147">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b942-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0b942-148">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="0b942-148">-Protocol</span></span>
<span data-ttu-id="0b942-149">Bir yük dengeleyici kuralıyla eşleşen Protokolü büyütür.</span><span class="sxs-lookup"><span data-stu-id="0b942-149">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="0b942-150">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="0b942-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="0b942-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b942-151">-Confirm</span></span>
<span data-ttu-id="0b942-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b942-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b942-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b942-153">-WhatIf</span></span>
<span data-ttu-id="0b942-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b942-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b942-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b942-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b942-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b942-156">CommonParameters</span></span>
<span data-ttu-id="0b942-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b942-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b942-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b942-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b942-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b942-159">INPUTS</span></span>

### <span data-ttu-id="0b942-160">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b942-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="0b942-161">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0b942-161">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="0b942-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b942-162">OUTPUTS</span></span>

### <span data-ttu-id="0b942-163">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b942-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0b942-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b942-164">NOTES</span></span>

## <span data-ttu-id="0b942-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b942-165">RELATED LINKS</span></span>

[<span data-ttu-id="0b942-166">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0b942-166">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="0b942-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b942-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="0b942-168">Yeni-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b942-168">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="0b942-169">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b942-169">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="0b942-170">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b942-170">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


