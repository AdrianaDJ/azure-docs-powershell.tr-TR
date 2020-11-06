---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 871982993492ba8eb06d818759e31d3c3500c1d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590149"
---
# <span data-ttu-id="6412b-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6412b-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="6412b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6412b-102">SYNOPSIS</span></span>
<span data-ttu-id="6412b-103">Yük Dengeleyici için bir kural yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6412b-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6412b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6412b-104">SYNTAX</span></span>

### <span data-ttu-id="6412b-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6412b-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6412b-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="6412b-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6412b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6412b-107">DESCRIPTION</span></span>
<span data-ttu-id="6412b-108">**Yeni-AzureRmLoadBalancerRuleConfig** cmdlet 'ı bir Azure yük dengeleyicisi için bir kural yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6412b-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="6412b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6412b-109">EXAMPLES</span></span>

### <span data-ttu-id="6412b-110">1: Azure Yük Dengeleyici için bir kural yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="6412b-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="6412b-111">İlk üç komut, bir genel IP, ön uç ve kural yapılandırması için ileri komutunda bir yoklama ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6412b-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="6412b-112">İleri komutu belirli belirtimlerle birlikte MyLBrule adlı yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6412b-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="6412b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6412b-113">PARAMETERS</span></span>

### <span data-ttu-id="6412b-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6412b-114">-BackendAddressPool</span></span>
<span data-ttu-id="6412b-115">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek **Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6412b-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6412b-116">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="6412b-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="6412b-117">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek bir **Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6412b-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6412b-118">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="6412b-118">-BackendPort</span></span>
<span data-ttu-id="6412b-119">Bu yük dengeleyici kuralı yapılandırması tarafından eşleştirilen trafik için arka uç bağlantı noktası 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6412b-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6412b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6412b-120">-DefaultProfile</span></span>
<span data-ttu-id="6412b-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6412b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6412b-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="6412b-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="6412b-123">Arka uç havuzundaki VM 'Ler için SNAT 'yi, Yük Dengeleme kuralının ön uç alanında belirtilen Publicıp adresini kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="6412b-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="6412b-124">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="6412b-124">-EnableFloatingIP</span></span>
<span data-ttu-id="6412b-125">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6412b-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6412b-126">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="6412b-126">-EnableTcpReset</span></span>
<span data-ttu-id="6412b-127">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="6412b-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="6412b-128">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6412b-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="6412b-129">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="6412b-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6412b-130">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6412b-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6412b-131">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="6412b-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6412b-132">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6412b-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6412b-133">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="6412b-133">-FrontendPort</span></span>
<span data-ttu-id="6412b-134">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6412b-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6412b-135">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="6412b-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6412b-136">Bir yük dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="6412b-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="6412b-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="6412b-137">-LoadDistribution</span></span>
<span data-ttu-id="6412b-138">Bir yük dağılımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6412b-138">Specifies a load distribution.</span></span>
<span data-ttu-id="6412b-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6412b-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6412b-140">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="6412b-140">Default</span></span>
- <span data-ttu-id="6412b-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="6412b-141">SourceIP</span></span>
- <span data-ttu-id="6412b-142">Sourceıpprotocol</span><span class="sxs-lookup"><span data-stu-id="6412b-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="6412b-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="6412b-143">-Name</span></span>
<span data-ttu-id="6412b-144">Bu cmdlet 'in oluşturduğu Yük Dengeleme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6412b-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6412b-145">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="6412b-145">-Probe</span></span>
<span data-ttu-id="6412b-146">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="6412b-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6412b-147">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="6412b-147">-ProbeId</span></span>
<span data-ttu-id="6412b-148">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6412b-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6412b-149">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="6412b-149">-Protocol</span></span>
<span data-ttu-id="6412b-150">Yük dengeleyici kuralı yapılandırmasıyla eşleşen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6412b-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="6412b-151">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="6412b-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="6412b-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="6412b-152">-Confirm</span></span>
<span data-ttu-id="6412b-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6412b-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6412b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6412b-154">-WhatIf</span></span>
<span data-ttu-id="6412b-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6412b-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6412b-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6412b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6412b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6412b-157">CommonParameters</span></span>
<span data-ttu-id="6412b-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6412b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6412b-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6412b-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6412b-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6412b-160">INPUTS</span></span>

### <span data-ttu-id="6412b-161">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6412b-161">None</span></span>

## <span data-ttu-id="6412b-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6412b-162">OUTPUTS</span></span>

### <span data-ttu-id="6412b-163">Microsoft. Azure. Commands. Network. modeller. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="6412b-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="6412b-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6412b-164">NOTES</span></span>

## <span data-ttu-id="6412b-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6412b-165">RELATED LINKS</span></span>

[<span data-ttu-id="6412b-166">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6412b-166">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6412b-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6412b-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6412b-168">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6412b-168">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6412b-169">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6412b-169">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


