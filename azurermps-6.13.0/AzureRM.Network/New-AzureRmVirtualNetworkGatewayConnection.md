---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: a9ad0933ce42dc0d031d9ca44d9b5ff7b84d6b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592290"
---
# <span data-ttu-id="25bf2-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25bf2-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="25bf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25bf2-102">SYNOPSIS</span></span>
<span data-ttu-id="25bf2-103">Sanal ağ geçidi ile şirket içi VPN aygıtı arasında siteden siteye VPN bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="25bf2-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25bf2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25bf2-104">SYNTAX</span></span>

### <span data-ttu-id="25bf2-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="25bf2-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>] [-ExpressRouteGatewayBypass]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bf2-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="25bf2-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>] [-ExpressRouteGatewayBypass]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25bf2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="25bf2-107">DESCRIPTION</span></span>
<span data-ttu-id="25bf2-108">Sanal ağ geçidi ile şirket içi VPN aygıtı arasında siteden siteye VPN bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="25bf2-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="25bf2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25bf2-109">EXAMPLES</span></span>

### <span data-ttu-id="25bf2-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="25bf2-110">Example 1</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="25bf2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25bf2-111">PARAMETERS</span></span>

### <span data-ttu-id="25bf2-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="25bf2-112">-AsJob</span></span>
<span data-ttu-id="25bf2-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="25bf2-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25bf2-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="25bf2-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="25bf2-115">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="25bf2-115">-ConnectionType</span></span>

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

### <span data-ttu-id="25bf2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bf2-116">-DefaultProfile</span></span>
<span data-ttu-id="25bf2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25bf2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25bf2-118">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="25bf2-118">-EnableBgp</span></span>

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

### <span data-ttu-id="25bf2-119">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="25bf2-119">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input:  True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25bf2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="25bf2-120">-Force</span></span>

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

### <span data-ttu-id="25bf2-121">-Ipsecpolicies</span><span class="sxs-lookup"><span data-stu-id="25bf2-121">-IpsecPolicies</span></span>
<span data-ttu-id="25bf2-122">IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="25bf2-122">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25bf2-123">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="25bf2-123">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="25bf2-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="25bf2-124">-Location</span></span>

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

### <span data-ttu-id="25bf2-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="25bf2-125">-Name</span></span>

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

### <span data-ttu-id="25bf2-126">-Peer</span><span class="sxs-lookup"><span data-stu-id="25bf2-126">-Peer</span></span>

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

### <span data-ttu-id="25bf2-127">-PeerID</span><span class="sxs-lookup"><span data-stu-id="25bf2-127">-PeerId</span></span>

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

### <span data-ttu-id="25bf2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25bf2-128">-ResourceGroupName</span></span>

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

### <span data-ttu-id="25bf2-129">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="25bf2-129">-RoutingWeight</span></span>

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

### <span data-ttu-id="25bf2-130">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="25bf2-130">-SharedKey</span></span>

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

### <span data-ttu-id="25bf2-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="25bf2-131">-Tag</span></span>
<span data-ttu-id="25bf2-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="25bf2-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="25bf2-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="25bf2-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="25bf2-134">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="25bf2-134">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="25bf2-135">S2S bağlantısı için ilkeye dayalı trafik seçicileri kullanma</span><span class="sxs-lookup"><span data-stu-id="25bf2-135">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="25bf2-136">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="25bf2-136">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="25bf2-137">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="25bf2-137">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="25bf2-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="25bf2-138">-Confirm</span></span>
<span data-ttu-id="25bf2-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="25bf2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25bf2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25bf2-140">-WhatIf</span></span>
<span data-ttu-id="25bf2-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="25bf2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25bf2-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="25bf2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25bf2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bf2-143">CommonParameters</span></span>
<span data-ttu-id="25bf2-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25bf2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bf2-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25bf2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bf2-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25bf2-146">INPUTS</span></span>

### <span data-ttu-id="25bf2-147">System. String</span><span class="sxs-lookup"><span data-stu-id="25bf2-147">System.String</span></span>

### <span data-ttu-id="25bf2-148">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25bf2-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="25bf2-149">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25bf2-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="25bf2-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="25bf2-150">System.Int32</span></span>

### <span data-ttu-id="25bf2-151">Microsoft. Azure. Commands. Network. model. pspe,</span><span class="sxs-lookup"><span data-stu-id="25bf2-151">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="25bf2-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25bf2-152">System.Boolean</span></span>

### <span data-ttu-id="25bf2-153">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="25bf2-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="25bf2-154">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSIpsecPolicy, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="25bf2-154">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="25bf2-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25bf2-155">OUTPUTS</span></span>

### <span data-ttu-id="25bf2-156">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25bf2-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="25bf2-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25bf2-157">NOTES</span></span>

## <span data-ttu-id="25bf2-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25bf2-158">RELATED LINKS</span></span>

[<span data-ttu-id="25bf2-159">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25bf2-159">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="25bf2-160">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25bf2-160">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="25bf2-161">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25bf2-161">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
