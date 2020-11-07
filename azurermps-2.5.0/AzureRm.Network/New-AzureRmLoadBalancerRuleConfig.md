---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: f3e256def28dff292efc5ba4278dc4f56b3ec721
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940052"
---
# <span data-ttu-id="6582d-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6582d-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="6582d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6582d-102">SYNOPSIS</span></span>
<span data-ttu-id="6582d-103">Yük Dengeleyici için bir kural yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6582d-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6582d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6582d-104">SYNTAX</span></span>

### <span data-ttu-id="6582d-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="6582d-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6582d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6582d-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6582d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6582d-107">DESCRIPTION</span></span>
<span data-ttu-id="6582d-108">**Yeni-AzureRmLoadBalancerRuleConfig** cmdlet 'ı bir Azure yük dengeleyicisi için bir kural yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6582d-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="6582d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6582d-109">EXAMPLES</span></span>

### <span data-ttu-id="6582d-110">1: Azure Yük Dengeleyici için bir kural yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="6582d-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
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

<span data-ttu-id="6582d-111">İlk üç komut, bir genel IP, ön uç ve kural yapılandırması için ileri komutunda bir yoklama ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6582d-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="6582d-112">İleri komutu belirli belirtimlerle birlikte MyLBrule adlı yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6582d-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="6582d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6582d-113">PARAMETERS</span></span>

### <span data-ttu-id="6582d-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6582d-114">-BackendAddressPool</span></span>
<span data-ttu-id="6582d-115">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek **Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6582d-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6582d-116">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="6582d-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="6582d-117">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek bir **Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6582d-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6582d-118">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="6582d-118">-BackendPort</span></span>
<span data-ttu-id="6582d-119">Bu yük dengeleyici kuralı yapılandırması tarafından eşleştirilen trafik için arka uç bağlantı noktası 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6582d-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6582d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6582d-120">-DefaultProfile</span></span>
<span data-ttu-id="6582d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6582d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6582d-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="6582d-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="6582d-123">Arka uç havuzundaki VM 'Ler için SNAT 'yi, Yük Dengeleme kuralının ön uç alanında belirtilen Publicıp adresini kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="6582d-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="6582d-124">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="6582d-124">-EnableFloatingIP</span></span>
<span data-ttu-id="6582d-125">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6582d-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="6582d-126">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="6582d-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="6582d-127">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6582d-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6582d-128">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="6582d-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="6582d-129">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6582d-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="6582d-130">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="6582d-130">-FrontendPort</span></span>
<span data-ttu-id="6582d-131">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6582d-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6582d-132">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="6582d-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6582d-133">Bir yük dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="6582d-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="6582d-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="6582d-134">-LoadDistribution</span></span>
<span data-ttu-id="6582d-135">Bir yük dağılımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6582d-135">Specifies a load distribution.</span></span>
<span data-ttu-id="6582d-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6582d-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6582d-137">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="6582d-137">Default</span></span>
- <span data-ttu-id="6582d-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="6582d-138">SourceIP</span></span>
- <span data-ttu-id="6582d-139">Sourceıpprotocol</span><span class="sxs-lookup"><span data-stu-id="6582d-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="6582d-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="6582d-140">-Name</span></span>
<span data-ttu-id="6582d-141">Bu cmdlet 'in oluşturduğu Yük Dengeleme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6582d-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6582d-142">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="6582d-142">-Probe</span></span>
<span data-ttu-id="6582d-143">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="6582d-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6582d-144">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="6582d-144">-ProbeId</span></span>
<span data-ttu-id="6582d-145">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6582d-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="6582d-146">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="6582d-146">-Protocol</span></span>
<span data-ttu-id="6582d-147">Yük dengeleyici kuralı yapılandırmasıyla eşleşen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6582d-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="6582d-148">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="6582d-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="6582d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6582d-149">CommonParameters</span></span>
<span data-ttu-id="6582d-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6582d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6582d-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6582d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6582d-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6582d-152">INPUTS</span></span>

## <span data-ttu-id="6582d-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6582d-153">OUTPUTS</span></span>

### <span data-ttu-id="6582d-154">Microsoft. Azure. Commands. Network. modeller. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="6582d-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="6582d-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6582d-155">NOTES</span></span>

## <span data-ttu-id="6582d-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6582d-156">RELATED LINKS</span></span>

[<span data-ttu-id="6582d-157">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6582d-157">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6582d-158">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6582d-158">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6582d-159">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6582d-159">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="6582d-160">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6582d-160">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


