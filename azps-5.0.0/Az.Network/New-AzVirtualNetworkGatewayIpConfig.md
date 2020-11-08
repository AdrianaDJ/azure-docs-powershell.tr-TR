---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278114"
---
# <span data-ttu-id="7722b-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7722b-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="7722b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7722b-102">SYNOPSIS</span></span>
<span data-ttu-id="7722b-103">Sanal ağ geçidi için IP yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="7722b-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="7722b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7722b-104">SYNTAX</span></span>

### <span data-ttu-id="7722b-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="7722b-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7722b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7722b-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7722b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7722b-107">DESCRIPTION</span></span>
<span data-ttu-id="7722b-108">**New-AzVirtualNetworkGatewayIpConfig** cmdlet 'ı, alt ağ kimliğine dayanan bir (önceden oluşturulmuş) genel IP adresiyle sanal ağ geçidine atanmış bir yapılandırma oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7722b-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="7722b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7722b-109">EXAMPLES</span></span>

### <span data-ttu-id="7722b-110">1: sanal ağ geçidi için IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="7722b-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="7722b-111">Genel IP adresiyle sanal ağ geçidi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="7722b-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="7722b-112">Değişken $myGWsubnet, sanal ağ geçidi oluşturmayı düşündüğünüz sanal ağdaki "GatewaySubnet" adresindeki **Get-AzVirtualNetworkSubnetConfig** cmdlet 'i kullanılarak elde edilir.</span><span class="sxs-lookup"><span data-stu-id="7722b-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="7722b-113">$MyGWpip değişken, **New-Azpublicıpaddress** cmdlet 'i kullanılarak elde edilir.</span><span class="sxs-lookup"><span data-stu-id="7722b-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="7722b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7722b-114">PARAMETERS</span></span>

### <span data-ttu-id="7722b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7722b-115">-DefaultProfile</span></span>
<span data-ttu-id="7722b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7722b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7722b-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="7722b-117">-Name</span></span>
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

### <span data-ttu-id="7722b-118">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="7722b-118">-PrivateIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7722b-119">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7722b-119">-PublicIpAddress</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7722b-120">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="7722b-120">-PublicIpAddressId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7722b-121">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="7722b-121">-Subnet</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7722b-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7722b-122">-SubnetId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7722b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7722b-123">CommonParameters</span></span>
<span data-ttu-id="7722b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7722b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7722b-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7722b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7722b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7722b-126">INPUTS</span></span>

### <span data-ttu-id="7722b-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7722b-127">None</span></span>

## <span data-ttu-id="7722b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7722b-128">OUTPUTS</span></span>

### <span data-ttu-id="7722b-129">Microsoft. Azure. Commands. Network. model. Psvirtualnetworkgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="7722b-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="7722b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7722b-130">NOTES</span></span>

## <span data-ttu-id="7722b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7722b-131">RELATED LINKS</span></span>

[<span data-ttu-id="7722b-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7722b-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="7722b-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7722b-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
