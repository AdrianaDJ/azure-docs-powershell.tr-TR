---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: 0708540cbb0ccac2f445fc0692c3c91f9358213c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939708"
---
# <span data-ttu-id="3278a-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3278a-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="3278a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3278a-102">SYNOPSIS</span></span>
<span data-ttu-id="3278a-103">Yük dengeleyicisine bir kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="3278a-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3278a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3278a-104">SYNTAX</span></span>

### <span data-ttu-id="3278a-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="3278a-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3278a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3278a-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3278a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3278a-107">DESCRIPTION</span></span>
<span data-ttu-id="3278a-108">**Add-AzureRmLoadBalancerRuleConfig** cmdlet 'ı bir Azure yük dengeleyicisine bir kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="3278a-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="3278a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3278a-109">EXAMPLES</span></span>

### <span data-ttu-id="3278a-110">Örnek 1: yük dengeleyicisine kural yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="3278a-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="3278a-111">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3278a-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="3278a-112">İkinci $slb komut, (NewRule adlı kural yapılandırmasını ekleyen **-AzureRmLoadBalancerRuleConfig öğesini ekleme**</span><span class="sxs-lookup"><span data-stu-id="3278a-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="3278a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3278a-113">PARAMETERS</span></span>

### <span data-ttu-id="3278a-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3278a-114">-BackendAddressPool</span></span>
<span data-ttu-id="3278a-115">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3278a-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3278a-116">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="3278a-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="3278a-117">Yük dengeleyici kuralı yapılandırmasıyla ilişkilendirilecek bir **Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3278a-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3278a-118">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="3278a-118">-BackendPort</span></span>
<span data-ttu-id="3278a-119">Yük dengeleyici kuralı yapılandırması ile eşleşen trafik için arka uç bağlantı noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="3278a-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3278a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3278a-120">-DefaultProfile</span></span>
<span data-ttu-id="3278a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3278a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3278a-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="3278a-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="3278a-123">Arka uç havuzundaki VM 'Ler için SNAT 'yi, Yük Dengeleme kuralının ön uç alanında belirtilen Publicıp adresini kullanacak şekilde yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="3278a-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="3278a-124">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="3278a-124">-EnableFloatingIP</span></span>
<span data-ttu-id="3278a-125">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3278a-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="3278a-126">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="3278a-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="3278a-127">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3278a-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3278a-128">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="3278a-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="3278a-129">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3278a-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="3278a-130">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="3278a-130">-FrontendPort</span></span>
<span data-ttu-id="3278a-131">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3278a-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3278a-132">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="3278a-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3278a-133">Yükleme dengeleyicide konuşmalar durumunun tutulduğu süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="3278a-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="3278a-134">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3278a-134">-LoadBalancer</span></span>
<span data-ttu-id="3278a-135">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3278a-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="3278a-136">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine bir kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="3278a-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="3278a-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="3278a-137">-LoadDistribution</span></span>
<span data-ttu-id="3278a-138">Bir yük dağılımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3278a-138">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="3278a-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="3278a-139">-Name</span></span>
<span data-ttu-id="3278a-140">Yük dengeleyici kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3278a-140">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3278a-141">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="3278a-141">-Probe</span></span>
<span data-ttu-id="3278a-142">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="3278a-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3278a-143">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="3278a-143">-ProbeId</span></span>
<span data-ttu-id="3278a-144">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3278a-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3278a-145">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="3278a-145">-Protocol</span></span>
<span data-ttu-id="3278a-146">Bir yük dengeleyici kuralıyla eşleşen Protokolü büyütür.</span><span class="sxs-lookup"><span data-stu-id="3278a-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="3278a-147">Bu parametre için kabul edilebilir değerler: TCP veya UDP.</span><span class="sxs-lookup"><span data-stu-id="3278a-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="3278a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3278a-148">CommonParameters</span></span>
<span data-ttu-id="3278a-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3278a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3278a-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3278a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3278a-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3278a-151">INPUTS</span></span>

### <span data-ttu-id="3278a-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3278a-152">PSLoadBalancer</span></span>
<span data-ttu-id="3278a-153">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3278a-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="3278a-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3278a-154">OUTPUTS</span></span>

### <span data-ttu-id="3278a-155">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3278a-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3278a-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3278a-156">NOTES</span></span>

## <span data-ttu-id="3278a-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3278a-157">RELATED LINKS</span></span>

[<span data-ttu-id="3278a-158">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3278a-158">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="3278a-159">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3278a-159">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="3278a-160">Yeni-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3278a-160">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="3278a-161">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3278a-161">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="3278a-162">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3278a-162">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


