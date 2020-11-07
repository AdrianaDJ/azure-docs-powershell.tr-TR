---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: a9b8cd9f13de8c1c4e3a7f20a0ffe410211f8973
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762762"
---
# <span data-ttu-id="d74a8-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="d74a8-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="d74a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d74a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d74a8-103">Bir Azure sanal ağ ağ geçidi tarafından tanıtılan yolları listeler</span><span class="sxs-lookup"><span data-stu-id="d74a8-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d74a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d74a8-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d74a8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d74a8-105">DESCRIPTION</span></span>
<span data-ttu-id="d74a8-106">BGP eşinin IP 'si verildiğinde, belirtilen Azure sanal ağ ağ geçidiyle bu eşe tanıtılan yolları numaralandırır.</span><span class="sxs-lookup"><span data-stu-id="d74a8-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="d74a8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d74a8-107">EXAMPLES</span></span>

### <span data-ttu-id="d74a8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d74a8-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="d74a8-109">Kaynak grubunda gatewayName adlı Azure ağ geçidi için, IP 10.0.0.254 ile BGP eşine tanıtılmakta olan yolların listesini yönlendirir</span><span class="sxs-lookup"><span data-stu-id="d74a8-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="d74a8-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d74a8-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="d74a8-111">ResourceGroupName kaynak grubunda gatewayName adlı Azure ağ geçidi için, tanıtılmakta olan yolları ağ geçidinin BGP eşleri listesindeki ilk BGP eşine getirir.</span><span class="sxs-lookup"><span data-stu-id="d74a8-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="d74a8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d74a8-112">PARAMETERS</span></span>

### <span data-ttu-id="d74a8-113">-Peer</span><span class="sxs-lookup"><span data-stu-id="d74a8-113">-Peer</span></span>
<span data-ttu-id="d74a8-114">BGP eşinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="d74a8-114">BGP peer's IP address.</span></span> <span data-ttu-id="d74a8-115">Bu, Azure sanal ağının içinden ağ üzerinden erişilebilen adres alanı içinde bir IP olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d74a8-115">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="d74a8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d74a8-116">-ResourceGroupName</span></span>
<span data-ttu-id="d74a8-117">Sanal ağ geçidi kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d74a8-117">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="d74a8-118">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="d74a8-118">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="d74a8-119">Sanal ağ geçidi adı</span><span class="sxs-lookup"><span data-stu-id="d74a8-119">Virtual network gateway name</span></span>

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

### <span data-ttu-id="d74a8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74a8-120">-DefaultProfile</span></span>
<span data-ttu-id="d74a8-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d74a8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d74a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74a8-122">CommonParameters</span></span>
<span data-ttu-id="d74a8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d74a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74a8-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d74a8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74a8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d74a8-125">INPUTS</span></span>

### <span data-ttu-id="d74a8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d74a8-126">System.String</span></span>

## <span data-ttu-id="d74a8-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d74a8-127">OUTPUTS</span></span>

### <span data-ttu-id="d74a8-128">Microsoft. Azure. Commands. Network. model. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="d74a8-128">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="d74a8-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d74a8-129">NOTES</span></span>
<span data-ttu-id="d74a8-130">Bu komut yalnızca BGP etkinleştirilmiş bağlantılar içeren Azure sanal ağ geçitleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="d74a8-130">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="d74a8-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d74a8-131">RELATED LINKS</span></span>

