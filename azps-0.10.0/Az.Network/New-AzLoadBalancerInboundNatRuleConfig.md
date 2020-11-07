---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 52aad9586840875cf63a27a8f27ff7296d080bd7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935388"
---
# <span data-ttu-id="f384d-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f384d-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="f384d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f384d-102">SYNOPSIS</span></span>
<span data-ttu-id="f384d-103">Bir yük dengeleyici için gelen NAT kural yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f384d-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="f384d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f384d-104">SYNTAX</span></span>

### <span data-ttu-id="f384d-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="f384d-105">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f384d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f384d-106">SetByResource</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f384d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f384d-107">DESCRIPTION</span></span>
<span data-ttu-id="f384d-108">**New-Azloadbalancerınboundnatruleconfig** cmdlet 'i, bir Azure yük dengeleyicisi için bir gelen ağ adresi ÇEVIRI (NAT) kuralı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f384d-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f384d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f384d-109">EXAMPLES</span></span>

### <span data-ttu-id="f384d-110">Örnek 1: yük dengeleyici için gelen NAT kural yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="f384d-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="f384d-111">İlk komut MyResourceGroup adlı kaynak grubunda MyPublicIP adlı genel bir IP adresi oluşturur ve $publicip değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f384d-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="f384d-112">İkinci komut, $publicip genel IP adresini kullanarak FrontendIpConfig01 adlı ön uç IP yapılandırması oluşturur ve $frontend değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f384d-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="f384d-113">Üçüncü komut, $frontend ön uç nesnesini kullanan MyInboundNatRule adlı bir gelen NAT kural yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f384d-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="f384d-114">TCP protokolü belirtilmiştir ve ön uç bağlantı noktası 3389, bu durumda arka uç bağlantı noktasıyla aynıdır.</span><span class="sxs-lookup"><span data-stu-id="f384d-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="f384d-115">*Frontendıkeyapılandırma* , *procotol* , *Frontenvseçport* ve *backendport* parametreleri gelen NAT kural yapılandırması oluşturmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f384d-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="f384d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f384d-116">PARAMETERS</span></span>

### <span data-ttu-id="f384d-117">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="f384d-117">-BackendPort</span></span>
<span data-ttu-id="f384d-118">Bu kural yapılandırmasıyla eşleşen trafik için arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f384d-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="f384d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f384d-119">-DefaultProfile</span></span>
<span data-ttu-id="f384d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f384d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f384d-121">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="f384d-121">-EnableFloatingIP</span></span>
<span data-ttu-id="f384d-122">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f384d-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="f384d-123">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="f384d-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f384d-124">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f384d-124">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f384d-125">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="f384d-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="f384d-126">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f384d-126">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="f384d-127">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="f384d-127">-FrontendPort</span></span>
<span data-ttu-id="f384d-128">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f384d-128">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f384d-129">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="f384d-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f384d-130">Bir yük dengeleyicide konuşmaları durumunu geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="f384d-130">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="f384d-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="f384d-131">-Name</span></span>
<span data-ttu-id="f384d-132">Bu cmdlet 'in oluşturduğu kural yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f384d-132">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f384d-133">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="f384d-133">-Protocol</span></span>
<span data-ttu-id="f384d-134">Protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f384d-134">Specifies a protocol.</span></span>
<span data-ttu-id="f384d-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f384d-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f384d-136">TC</span><span class="sxs-lookup"><span data-stu-id="f384d-136">Tcp</span></span>
- <span data-ttu-id="f384d-137">UDP</span><span class="sxs-lookup"><span data-stu-id="f384d-137">Udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f384d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f384d-138">CommonParameters</span></span>
<span data-ttu-id="f384d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f384d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f384d-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f384d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f384d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f384d-141">INPUTS</span></span>

## <span data-ttu-id="f384d-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f384d-142">OUTPUTS</span></span>

### <span data-ttu-id="f384d-143">Microsoft. Azure. Commands. Network. model. Psınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="f384d-143">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="f384d-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f384d-144">NOTES</span></span>

## <span data-ttu-id="f384d-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f384d-145">RELATED LINKS</span></span>

[<span data-ttu-id="f384d-146">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f384d-146">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f384d-147">Get-Azloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="f384d-147">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f384d-148">Yeni-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="f384d-148">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f384d-149">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="f384d-149">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="f384d-150">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f384d-150">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f384d-151">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f384d-151">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


