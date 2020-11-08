---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f6dc25bc1000466d853715f62e38237ddfc76aa2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098710"
---
# <span data-ttu-id="f459b-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f459b-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f459b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f459b-102">SYNOPSIS</span></span>
<span data-ttu-id="f459b-103">Sanal ağ geçidi ile şirket içi VPN aygıtı arasında siteden siteye VPN bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f459b-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="f459b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f459b-104">SYNTAX</span></span>

### <span data-ttu-id="f459b-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f459b-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f459b-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="f459b-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f459b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f459b-107">DESCRIPTION</span></span>
<span data-ttu-id="f459b-108">Sanal ağ geçidi ile şirket içi VPN aygıtı arasında siteden siteye VPN bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f459b-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="f459b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f459b-109">EXAMPLES</span></span>

### <span data-ttu-id="f459b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f459b-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="f459b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f459b-111">PARAMETERS</span></span>

### <span data-ttu-id="f459b-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="f459b-112">-AsJob</span></span>
<span data-ttu-id="f459b-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f459b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f459b-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="f459b-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="f459b-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="f459b-115">-ConnectionProtocol</span></span>
<span data-ttu-id="f459b-116">Ağ Geçidi bağlantı protokolü: IKEv1/Ikev2</span><span class="sxs-lookup"><span data-stu-id="f459b-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="f459b-117">-ConnectionType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f459b-118">-DefaultProfile</span></span>
<span data-ttu-id="f459b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f459b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f459b-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f459b-120">-EnableBgp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="f459b-121">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f459b-122">-Force</span></span>

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

### <span data-ttu-id="f459b-123">-Ipsecpolicies</span><span class="sxs-lookup"><span data-stu-id="f459b-123">-IpsecPolicies</span></span>
<span data-ttu-id="f459b-124">IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="f459b-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="f459b-125">-LocalNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="f459b-126">-Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="f459b-127">-Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-128">-Peer</span><span class="sxs-lookup"><span data-stu-id="f459b-128">-Peer</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-129">-PeerID</span><span class="sxs-lookup"><span data-stu-id="f459b-129">-PeerId</span></span>

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

### <span data-ttu-id="f459b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f459b-130">-ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="f459b-131">-RoutingWeight</span></span>

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

### <span data-ttu-id="f459b-132">-Vseçpdtimeoutınseconds</span><span class="sxs-lookup"><span data-stu-id="f459b-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="f459b-133">Bağlantının saniye cinsinden ölü algılama zaman aşımı süresi</span><span class="sxs-lookup"><span data-stu-id="f459b-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="f459b-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="f459b-134">-SharedKey</span></span>

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

### <span data-ttu-id="f459b-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f459b-135">-Tag</span></span>
<span data-ttu-id="f459b-136">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="f459b-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f459b-137">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="f459b-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-138">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f459b-138">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="f459b-139">Trafik seçici ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="f459b-139">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-140">-Uselocalazureıpaddress</span><span class="sxs-lookup"><span data-stu-id="f459b-140">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="f459b-141">Bu S2S VPN tüneli için Privateıp kullanılıp kullanılmayacağını</span><span class="sxs-lookup"><span data-stu-id="f459b-141">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-142">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="f459b-142">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="f459b-143">S2S bağlantısı için ilkeye dayalı trafik seçicileri kullanma</span><span class="sxs-lookup"><span data-stu-id="f459b-143">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-144">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="f459b-144">-VirtualNetworkGateway1</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-145">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="f459b-145">-VirtualNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="f459b-146">-Confirm</span></span>
<span data-ttu-id="f459b-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f459b-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f459b-148">-WhatIf</span></span>
<span data-ttu-id="f459b-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f459b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f459b-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f459b-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f459b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f459b-151">CommonParameters</span></span>
<span data-ttu-id="f459b-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f459b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f459b-153">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f459b-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f459b-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f459b-154">INPUTS</span></span>

### <span data-ttu-id="f459b-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f459b-155">System.String</span></span>

### <span data-ttu-id="f459b-156">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f459b-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="f459b-157">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f459b-157">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="f459b-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f459b-158">System.Int32</span></span>

### <span data-ttu-id="f459b-159">Microsoft. Azure. Commands. Network. model. pspe,</span><span class="sxs-lookup"><span data-stu-id="f459b-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="f459b-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f459b-160">System.Boolean</span></span>

### <span data-ttu-id="f459b-161">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f459b-161">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f459b-162">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="f459b-162">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="f459b-163">Microsoft. Azure. Commands. Network. modeller. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="f459b-163">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="f459b-164">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f459b-164">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f459b-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f459b-165">OUTPUTS</span></span>

### <span data-ttu-id="f459b-166">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f459b-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f459b-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f459b-167">NOTES</span></span>

## <span data-ttu-id="f459b-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f459b-168">RELATED LINKS</span></span>

[<span data-ttu-id="f459b-169">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f459b-169">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f459b-170">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f459b-170">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f459b-171">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f459b-171">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)