---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b00c3950140c0ebf158170a8ddd2396e62c2b2c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763146"
---
# <span data-ttu-id="2fca4-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="2fca4-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="2fca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fca4-102">SYNOPSIS</span></span>
<span data-ttu-id="2fca4-103">Sanal ağ geçidi için IP yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="2fca4-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fca4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2fca4-104">SYNTAX</span></span>

### <span data-ttu-id="2fca4-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="2fca4-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fca4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2fca4-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fca4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2fca4-107">DESCRIPTION</span></span>
<span data-ttu-id="2fca4-108">**Yeni-AzureRmVirtualNetworkGatewayIpConfig** cmdlet 'ı, alt ağ kimliğine dayanan bir (önceden oluşturulmuş) genel IP adresiyle sanal ağ geçidine atanmış bir yapılandırma oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fca4-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="2fca4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2fca4-109">EXAMPLES</span></span>

### <span data-ttu-id="2fca4-110">1: sanal ağ geçidi için IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="2fca4-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="2fca4-111">Genel IP adresiyle sanal ağ geçidi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="2fca4-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="2fca4-112">Değişken $myGWsubnet, sanal ağ geçidi oluşturmayı düşündüğünüz sanal ağdaki "GatewaySubnet" adresindeki **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet 'i kullanılarak elde edilir.</span><span class="sxs-lookup"><span data-stu-id="2fca4-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="2fca4-113">$MyGWpip değişken, **New-Azurermpublicıpaddress** cmdlet 'i kullanılarak elde edilir.</span><span class="sxs-lookup"><span data-stu-id="2fca4-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="2fca4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2fca4-114">PARAMETERS</span></span>

### <span data-ttu-id="2fca4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fca4-115">-DefaultProfile</span></span>
<span data-ttu-id="2fca4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2fca4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fca4-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2fca4-117">-Name</span></span>
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

### <span data-ttu-id="2fca4-118">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="2fca4-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="2fca4-119">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="2fca4-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="2fca4-120">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="2fca4-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="2fca4-121">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="2fca4-121">-Subnet</span></span>
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

### <span data-ttu-id="2fca4-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2fca4-122">-SubnetId</span></span>
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

### <span data-ttu-id="2fca4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fca4-123">CommonParameters</span></span>
<span data-ttu-id="2fca4-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2fca4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fca4-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fca4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fca4-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2fca4-126">INPUTS</span></span>

### <span data-ttu-id="2fca4-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2fca4-127">None</span></span>

## <span data-ttu-id="2fca4-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2fca4-128">OUTPUTS</span></span>

### <span data-ttu-id="2fca4-129">Microsoft. Azure. Commands. Network. model. Psvirtualnetworkgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2fca4-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="2fca4-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2fca4-130">NOTES</span></span>

## <span data-ttu-id="2fca4-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2fca4-131">RELATED LINKS</span></span>
