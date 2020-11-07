---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6f724cb7208afb1a5f9474048b5e2dc46c17f5af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932368"
---
# <span data-ttu-id="e39a1-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e39a1-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="e39a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e39a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e39a1-103">Bir yük dengeleyici için gelen NAT kural yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e39a1-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="e39a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e39a1-104">SYNTAX</span></span>

### <span data-ttu-id="e39a1-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e39a1-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e39a1-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="e39a1-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e39a1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e39a1-107">DESCRIPTION</span></span>
<span data-ttu-id="e39a1-108">**New-Azloadbalancerınboundnatruleconfig** cmdlet 'i, bir Azure yük dengeleyicisi için bir gelen ağ adresi ÇEVIRI (NAT) kuralı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e39a1-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e39a1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e39a1-109">EXAMPLES</span></span>

### <span data-ttu-id="e39a1-110">Örnek 1: yük dengeleyici için gelen NAT kural yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="e39a1-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="e39a1-111">İlk komut MyResourceGroup adlı kaynak grubunda MyPublicIP adlı genel bir IP adresi oluşturur ve $publicip değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e39a1-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="e39a1-112">İkinci komut, $publicip genel IP adresini kullanarak FrontendIpConfig01 adlı ön uç IP yapılandırması oluşturur ve $frontend değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e39a1-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="e39a1-113">Üçüncü komut, $frontend ön uç nesnesini kullanan MyInboundNatRule adlı bir gelen NAT kural yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e39a1-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="e39a1-114">TCP protokolü belirtilmiştir ve ön uç bağlantı noktası 3389, bu durumda arka uç bağlantı noktasıyla aynıdır.</span><span class="sxs-lookup"><span data-stu-id="e39a1-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="e39a1-115">Bir gelen NAT kural yapılandırması oluşturmak için *Frontendıyapılandırma* , *protokol* , *Frontenvseçport* ve *backendport* parametrelerinin tümü gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e39a1-115">The *FrontendIpConfiguration* , *Protocol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="e39a1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e39a1-116">PARAMETERS</span></span>

### <span data-ttu-id="e39a1-117">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="e39a1-117">-BackendPort</span></span>
<span data-ttu-id="e39a1-118">Bu kural yapılandırmasıyla eşleşen trafik için arka uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e39a1-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="e39a1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e39a1-119">-DefaultProfile</span></span>
<span data-ttu-id="e39a1-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e39a1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e39a1-121">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="e39a1-121">-EnableFloatingIP</span></span>
<span data-ttu-id="e39a1-122">Bu cmdlet 'in bir kural yapılandırması için kayan IP adresi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e39a1-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="e39a1-123">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="e39a1-123">-EnableTcpReset</span></span>
<span data-ttu-id="e39a1-124">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="e39a1-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="e39a1-125">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e39a1-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="e39a1-126">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="e39a1-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e39a1-127">Yük dengeleyici kuralı yapılandırması ile ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e39a1-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e39a1-128">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="e39a1-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="e39a1-129">Ön uç IP adresi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e39a1-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="e39a1-130">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="e39a1-130">-FrontendPort</span></span>
<span data-ttu-id="e39a1-131">Yük dengeleyici kuralı yapılandırmasıyla eşleşen ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e39a1-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="e39a1-132">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="e39a1-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e39a1-133">Bir yük dengeleyicide konuşmaları durumunu geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="e39a1-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="e39a1-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="e39a1-134">-Name</span></span>
<span data-ttu-id="e39a1-135">Bu cmdlet 'in oluşturduğu kural yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e39a1-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e39a1-136">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="e39a1-136">-Protocol</span></span>
<span data-ttu-id="e39a1-137">Protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e39a1-137">Specifies a protocol.</span></span>
<span data-ttu-id="e39a1-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e39a1-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e39a1-139">TC</span><span class="sxs-lookup"><span data-stu-id="e39a1-139">Tcp</span></span>
- <span data-ttu-id="e39a1-140">UDP</span><span class="sxs-lookup"><span data-stu-id="e39a1-140">Udp</span></span>

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

### <span data-ttu-id="e39a1-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="e39a1-141">-Confirm</span></span>
<span data-ttu-id="e39a1-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e39a1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e39a1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e39a1-143">-WhatIf</span></span>
<span data-ttu-id="e39a1-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e39a1-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e39a1-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e39a1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e39a1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e39a1-146">CommonParameters</span></span>
<span data-ttu-id="e39a1-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e39a1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e39a1-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e39a1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e39a1-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e39a1-149">INPUTS</span></span>

### <span data-ttu-id="e39a1-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e39a1-150">System.String</span></span>

### <span data-ttu-id="e39a1-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e39a1-151">System.Int32</span></span>

### <span data-ttu-id="e39a1-152">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="e39a1-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="e39a1-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e39a1-153">OUTPUTS</span></span>

### <span data-ttu-id="e39a1-154">Microsoft. Azure. Commands. Network. model. Psınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="e39a1-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="e39a1-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e39a1-155">NOTES</span></span>

## <span data-ttu-id="e39a1-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e39a1-156">RELATED LINKS</span></span>

[<span data-ttu-id="e39a1-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e39a1-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e39a1-158">Get-Azloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="e39a1-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e39a1-159">Yeni-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="e39a1-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e39a1-160">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="e39a1-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="e39a1-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e39a1-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e39a1-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e39a1-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


