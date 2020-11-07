---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: 0b4bdbcdb4a753943278b759d584bb034a717b62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940054"
---
# <span data-ttu-id="512e6-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="512e6-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="512e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="512e6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="512e6-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="512e6-103">SYNTAX</span></span>

### <span data-ttu-id="512e6-104">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="512e6-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="512e6-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="512e6-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="512e6-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="512e6-106">DESCRIPTION</span></span>

## <span data-ttu-id="512e6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="512e6-107">EXAMPLES</span></span>

### <span data-ttu-id="512e6-108">2</span><span class="sxs-lookup"><span data-stu-id="512e6-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="512e6-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="512e6-109">PARAMETERS</span></span>

### <span data-ttu-id="512e6-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="512e6-110">-AsJob</span></span>
<span data-ttu-id="512e6-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="512e6-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="512e6-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="512e6-112">-AuthorizationKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="512e6-113">-ConnectionType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512e6-114">-DefaultProfile</span></span>
<span data-ttu-id="512e6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="512e6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="512e6-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="512e6-116">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="512e6-117">-Force</span></span>
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

### <span data-ttu-id="512e6-118">-Ipsecpolicies</span><span class="sxs-lookup"><span data-stu-id="512e6-118">-IpsecPolicies</span></span>
<span data-ttu-id="512e6-119">IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="512e6-119">A list of IPSec policies.</span></span>
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

### <span data-ttu-id="512e6-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="512e6-120">-LocalNetworkGateway2</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="512e6-121">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="512e6-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-123">-Peer</span><span class="sxs-lookup"><span data-stu-id="512e6-123">-Peer</span></span>
```yaml
Type: PSPeering
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-124">-PeerID</span><span class="sxs-lookup"><span data-stu-id="512e6-124">-PeerId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="512e6-125">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="512e6-126">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="512e6-127">-SharedKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="512e6-128">-Tag</span></span>
<span data-ttu-id="512e6-129">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="512e6-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="512e6-130">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="512e6-130">For example:</span></span>

<span data-ttu-id="512e6-131">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="512e6-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="512e6-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="512e6-133">S2S bağlantısı için ilkeye dayalı trafik seçicileri kullanma</span><span class="sxs-lookup"><span data-stu-id="512e6-133">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="512e6-134">-VirtualNetworkGateway1</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="512e6-135">-VirtualNetworkGateway2</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="512e6-136">-Confirm</span></span>
<span data-ttu-id="512e6-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="512e6-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="512e6-138">-WhatIf</span></span>
<span data-ttu-id="512e6-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="512e6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="512e6-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="512e6-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512e6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512e6-141">CommonParameters</span></span>
<span data-ttu-id="512e6-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="512e6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512e6-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="512e6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512e6-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="512e6-144">INPUTS</span></span>

## <span data-ttu-id="512e6-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="512e6-145">OUTPUTS</span></span>

### <span data-ttu-id="512e6-146">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="512e6-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="512e6-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="512e6-147">NOTES</span></span>

## <span data-ttu-id="512e6-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="512e6-148">RELATED LINKS</span></span>

[<span data-ttu-id="512e6-149">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="512e6-149">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="512e6-150">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="512e6-150">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="512e6-151">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="512e6-151">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
