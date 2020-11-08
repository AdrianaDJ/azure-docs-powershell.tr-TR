---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278535"
---
# <span data-ttu-id="6eb20-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6eb20-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="6eb20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb20-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb20-103">Yük Dengeleyici için bir kural yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6eb20-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="6eb20-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6eb20-104">SYNTAX</span></span>

### <span data-ttu-id="6eb20-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6eb20-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eb20-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="6eb20-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eb20-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6eb20-107">DESCRIPTION</span></span>
<span data-ttu-id="6eb20-108">**New-AzLoadBalancerRuleConfig** cmdlet 'ı bir Azure yük dengeleyicisi için bir kural yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6eb20-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="6eb20-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6eb20-109">EXAMPLES</span></span>

### <span data-ttu-id="6eb20-110">Örnek 1: Azure Yük Dengeleyici için bir kural yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="6eb20-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
```powershell
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" `
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd `
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port `
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration `
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp `
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP `
    -LoadDistribution SourceIP
```

<span data-ttu-id="6eb20-111">İlk üç komut, bir genel IP, ön uç ve kural yapılandırması için ileri komutunda bir yoklama ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6eb20-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="6eb20-112">İleri komutu belirli belirtimlerle birlikte MyLBrule adlı yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6eb20-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="6eb20-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6eb20-113">PARAMETERS</span></span>

### <span data-ttu-id="6eb20-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6eb20-114">-BackendAddressPool</span></span>
<span data-ttu-id="6eb20-115">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek **Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6eb20-116">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="6eb20-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="6eb20-117">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek bir **Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6eb20-118">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="6eb20-118">-BackendPort</span></span>
<span data-ttu-id="6eb20-119">Bu yük dengeleyici kuralı yapılandırması tarafından eşleştirilen trafik için arka uç bağlantı noktası 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6eb20-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb20-120">-DefaultProfile</span></span>
<span data-ttu-id="6eb20-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6eb20-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb20-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="6eb20-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="6eb20-123">Arka uç havuzundaki VM 'Ler için SNAT 'yi, Yük Dengeleme kuralının ön uç alanında belirtilen Publicıp adresini kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="6eb20-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="6eb20-124">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="6eb20-124">-EnableFloatingIP</span></span>
<span data-ttu-id="6eb20-125">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6eb20-126">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="6eb20-126">-EnableTcpReset</span></span>
<span data-ttu-id="6eb20-127">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="6eb20-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="6eb20-128">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6eb20-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="6eb20-129">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="6eb20-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6eb20-130">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6eb20-131">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="6eb20-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6eb20-132">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6eb20-133">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="6eb20-133">-FrontendPort</span></span>
<span data-ttu-id="6eb20-134">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6eb20-135">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="6eb20-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6eb20-136">Bir yük dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="6eb20-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="6eb20-137">-LoadDistribution</span></span>
<span data-ttu-id="6eb20-138">Bir yük dağılımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-138">Specifies a load distribution.</span></span>
<span data-ttu-id="6eb20-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6eb20-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6eb20-140">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="6eb20-140">Default</span></span>
- <span data-ttu-id="6eb20-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="6eb20-141">SourceIP</span></span>
- <span data-ttu-id="6eb20-142">Sourceıpprotocol</span><span class="sxs-lookup"><span data-stu-id="6eb20-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="6eb20-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="6eb20-143">-Name</span></span>
<span data-ttu-id="6eb20-144">Bu cmdlet 'in oluşturduğu Yük Dengeleme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6eb20-145">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="6eb20-145">-Probe</span></span>
<span data-ttu-id="6eb20-146">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6eb20-147">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="6eb20-147">-ProbeId</span></span>
<span data-ttu-id="6eb20-148">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6eb20-149">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="6eb20-149">-Protocol</span></span>
<span data-ttu-id="6eb20-150">Yük dengeleyici kuralı yapılandırmasıyla eşleşen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="6eb20-151">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="6eb20-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="6eb20-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="6eb20-152">-Confirm</span></span>
<span data-ttu-id="6eb20-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6eb20-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eb20-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eb20-154">-WhatIf</span></span>
<span data-ttu-id="6eb20-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6eb20-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6eb20-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6eb20-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eb20-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb20-157">CommonParameters</span></span>
<span data-ttu-id="6eb20-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6eb20-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb20-159">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eb20-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb20-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6eb20-160">INPUTS</span></span>

### <span data-ttu-id="6eb20-161">System. String</span><span class="sxs-lookup"><span data-stu-id="6eb20-161">System.String</span></span>

### <span data-ttu-id="6eb20-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6eb20-162">System.Int32</span></span>

### <span data-ttu-id="6eb20-163">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="6eb20-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="6eb20-164">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6eb20-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="6eb20-165">Microsoft. Azure. Commands. Network. modeller. Psaraştırması</span><span class="sxs-lookup"><span data-stu-id="6eb20-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="6eb20-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6eb20-166">OUTPUTS</span></span>

### <span data-ttu-id="6eb20-167">Microsoft. Azure. Commands. Network. modeller. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="6eb20-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="6eb20-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6eb20-168">NOTES</span></span>

## <span data-ttu-id="6eb20-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6eb20-169">RELATED LINKS</span></span>

[<span data-ttu-id="6eb20-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6eb20-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6eb20-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6eb20-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6eb20-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6eb20-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6eb20-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6eb20-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


