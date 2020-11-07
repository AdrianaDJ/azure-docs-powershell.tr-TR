---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8f6b095a502c235927a48f2043a9140483cedc3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760260"
---
# <span data-ttu-id="7a7ee-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7a7ee-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7a7ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7ee-103">Sanal ağ geçidi ile şirket içi VPN aygıtı arasında siteden siteye VPN bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="7a7ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a7ee-104">SYNTAX</span></span>

### <span data-ttu-id="7a7ee-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7a7ee-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a7ee-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="7a7ee-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a7ee-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a7ee-107">DESCRIPTION</span></span>
<span data-ttu-id="7a7ee-108">Sanal ağ geçidi ile şirket içi VPN aygıtı arasında siteden siteye VPN bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="7a7ee-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a7ee-109">EXAMPLES</span></span>

### <span data-ttu-id="7a7ee-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7a7ee-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="7a7ee-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a7ee-111">PARAMETERS</span></span>

### <span data-ttu-id="7a7ee-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="7a7ee-112">-AsJob</span></span>
<span data-ttu-id="7a7ee-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7a7ee-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a7ee-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="7a7ee-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="7a7ee-115">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="7a7ee-115">-ConnectionType</span></span>

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

### <span data-ttu-id="7a7ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7ee-116">-DefaultProfile</span></span>
<span data-ttu-id="7a7ee-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a7ee-118">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7a7ee-118">-EnableBgp</span></span>

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

### <span data-ttu-id="7a7ee-119">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="7a7ee-119">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="7a7ee-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7a7ee-120">-Force</span></span>

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

### <span data-ttu-id="7a7ee-121">-Ipsecpolicies</span><span class="sxs-lookup"><span data-stu-id="7a7ee-121">-IpsecPolicies</span></span>
<span data-ttu-id="7a7ee-122">IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-122">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="7a7ee-123">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="7a7ee-123">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="7a7ee-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="7a7ee-124">-Location</span></span>

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

### <span data-ttu-id="7a7ee-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="7a7ee-125">-Name</span></span>

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

### <span data-ttu-id="7a7ee-126">-Peer</span><span class="sxs-lookup"><span data-stu-id="7a7ee-126">-Peer</span></span>

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

### <span data-ttu-id="7a7ee-127">-PeerID</span><span class="sxs-lookup"><span data-stu-id="7a7ee-127">-PeerId</span></span>

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

### <span data-ttu-id="7a7ee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a7ee-128">-ResourceGroupName</span></span>

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

### <span data-ttu-id="7a7ee-129">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="7a7ee-129">-RoutingWeight</span></span>

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

### <span data-ttu-id="7a7ee-130">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7a7ee-130">-SharedKey</span></span>

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

### <span data-ttu-id="7a7ee-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7a7ee-131">-Tag</span></span>
<span data-ttu-id="7a7ee-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7a7ee-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="7a7ee-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7a7ee-134">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="7a7ee-134">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="7a7ee-135">S2S bağlantısı için ilkeye dayalı trafik seçicileri kullanma</span><span class="sxs-lookup"><span data-stu-id="7a7ee-135">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="7a7ee-136">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="7a7ee-136">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="7a7ee-137">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="7a7ee-137">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="7a7ee-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="7a7ee-138">-Confirm</span></span>
<span data-ttu-id="7a7ee-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a7ee-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a7ee-140">-WhatIf</span></span>
<span data-ttu-id="7a7ee-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a7ee-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a7ee-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7ee-143">CommonParameters</span></span>
<span data-ttu-id="7a7ee-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7ee-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a7ee-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7ee-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a7ee-146">INPUTS</span></span>

### <span data-ttu-id="7a7ee-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7a7ee-147">System.String</span></span>

### <span data-ttu-id="7a7ee-148">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a7ee-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="7a7ee-149">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a7ee-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="7a7ee-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7a7ee-150">System.Int32</span></span>

### <span data-ttu-id="7a7ee-151">Microsoft. Azure. Commands. Network. model. pspe,</span><span class="sxs-lookup"><span data-stu-id="7a7ee-151">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="7a7ee-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7a7ee-152">System.Boolean</span></span>

### <span data-ttu-id="7a7ee-153">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7a7ee-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7a7ee-154">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="7a7ee-154">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="7a7ee-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a7ee-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a7ee-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a7ee-156">OUTPUTS</span></span>

### <span data-ttu-id="7a7ee-157">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7a7ee-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7a7ee-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a7ee-158">NOTES</span></span>

## <span data-ttu-id="7a7ee-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a7ee-159">RELATED LINKS</span></span>

[<span data-ttu-id="7a7ee-160">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7a7ee-160">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7a7ee-161">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7a7ee-161">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7a7ee-162">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7a7ee-162">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
