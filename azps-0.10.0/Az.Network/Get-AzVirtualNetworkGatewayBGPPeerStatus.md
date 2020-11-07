---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: f92b211befbf019f46869f733fa012e74e72c327
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935480"
---
# <span data-ttu-id="38123-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="38123-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="38123-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38123-102">SYNOPSIS</span></span>
<span data-ttu-id="38123-103">Azure sanal ağı ağ geçidinin BGP eşlerini listeler</span><span class="sxs-lookup"><span data-stu-id="38123-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="38123-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38123-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38123-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="38123-105">DESCRIPTION</span></span>
<span data-ttu-id="38123-106">Bu komut, BGP eşlerine bir Azure sanal ağı ağ geçidi eş olacak şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="38123-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="38123-107">Her eşin durumu da verilir.</span><span class="sxs-lookup"><span data-stu-id="38123-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="38123-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38123-108">EXAMPLES</span></span>

### <span data-ttu-id="38123-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="38123-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="38123-110">Kaynak grubu resourceGroup 'da gatewayName adlı Azure sanal ağ geçidi için BGP eşlerini getirir.</span><span class="sxs-lookup"><span data-stu-id="38123-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>

<span data-ttu-id="38123-111">Bu örnek çıktıda, 10.0.0.254 IP 'si olan bağlı bir BGP eşi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="38123-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="38123-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38123-112">PARAMETERS</span></span>

### <span data-ttu-id="38123-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="38123-113">-AsJob</span></span>
<span data-ttu-id="38123-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="38123-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38123-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38123-115">-DefaultProfile</span></span>
<span data-ttu-id="38123-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38123-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38123-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="38123-117">-Peer</span></span>
<span data-ttu-id="38123-118">Durumu alacak olan eşin IP 'si</span><span class="sxs-lookup"><span data-stu-id="38123-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="38123-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38123-119">-ResourceGroupName</span></span>
<span data-ttu-id="38123-120">Sanal ağ geçidi kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="38123-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="38123-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="38123-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="38123-122">Sanal ağ geçidi adı</span><span class="sxs-lookup"><span data-stu-id="38123-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="38123-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38123-123">CommonParameters</span></span>
<span data-ttu-id="38123-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38123-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38123-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38123-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38123-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38123-126">INPUTS</span></span>

### <span data-ttu-id="38123-127">System. String</span><span class="sxs-lookup"><span data-stu-id="38123-127">System.String</span></span>

## <span data-ttu-id="38123-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38123-128">OUTPUTS</span></span>

### <span data-ttu-id="38123-129">Microsoft. Azure. Commands. Network. model. PSBGPPeerStatus []</span><span class="sxs-lookup"><span data-stu-id="38123-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus[]</span></span>

## <span data-ttu-id="38123-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38123-130">NOTES</span></span>

## <span data-ttu-id="38123-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38123-131">RELATED LINKS</span></span>

