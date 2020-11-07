---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: eba8cd39c621cd2e7b959e54cf20a26ec3434af0
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93765207"
---
# <span data-ttu-id="bb10f-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="bb10f-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="bb10f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb10f-102">SYNOPSIS</span></span>
<span data-ttu-id="bb10f-103">Sanal ağ geçidi için IP yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="bb10f-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb10f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb10f-104">SYNTAX</span></span>

### <span data-ttu-id="bb10f-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="bb10f-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb10f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bb10f-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb10f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb10f-107">DESCRIPTION</span></span>
<span data-ttu-id="bb10f-108">**Yeni-AzureRmVirtualNetworkGatewayIpConfig** cmdlet 'ı, alt ağ kimliğine dayanan bir (önceden oluşturulmuş) genel IP adresiyle sanal ağ geçidine atanmış bir yapılandırma oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bb10f-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="bb10f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb10f-109">EXAMPLES</span></span>

### <span data-ttu-id="bb10f-110">1: sanal ağ geçidi için IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="bb10f-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="bb10f-111">Genel IP adresiyle sanal ağ geçidi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="bb10f-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="bb10f-112">Değişken $myGWsubnet, sanal ağ geçidi oluşturmayı düşündüğünüz sanal ağdaki "GatewaySubnet" adresindeki **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet 'i kullanılarak elde edilir.</span><span class="sxs-lookup"><span data-stu-id="bb10f-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="bb10f-113">$MyGWpip değişken, **New-Azurermpublicıpaddress** cmdlet 'i kullanılarak elde edilir.</span><span class="sxs-lookup"><span data-stu-id="bb10f-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="bb10f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb10f-114">PARAMETERS</span></span>

### <span data-ttu-id="bb10f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb10f-115">-DefaultProfile</span></span>
<span data-ttu-id="bb10f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb10f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb10f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb10f-117">-Name</span></span>
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

### <span data-ttu-id="bb10f-118">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="bb10f-118">-PrivateIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb10f-119">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="bb10f-119">-PublicIpAddress</span></span>
```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb10f-120">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="bb10f-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="bb10f-121">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="bb10f-121">-Subnet</span></span>
```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb10f-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bb10f-122">-SubnetId</span></span>
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

### <span data-ttu-id="bb10f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb10f-123">CommonParameters</span></span>
<span data-ttu-id="bb10f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb10f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb10f-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb10f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb10f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb10f-126">INPUTS</span></span>

### <span data-ttu-id="bb10f-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bb10f-127">None</span></span>
<span data-ttu-id="bb10f-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="bb10f-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb10f-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb10f-129">OUTPUTS</span></span>

### <span data-ttu-id="bb10f-130">Microsoft. Azure. Commands. Network. model. Psvirtualnetworkgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="bb10f-130">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="bb10f-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb10f-131">NOTES</span></span>

## <span data-ttu-id="bb10f-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb10f-132">RELATED LINKS</span></span>

