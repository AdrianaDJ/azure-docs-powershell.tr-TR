---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 416bc8910e651ca86ef064fda7bd934d67ed8056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931967"
---
# <span data-ttu-id="4c8c0-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="4c8c0-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="4c8c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c8c0-102">SYNOPSIS</span></span>
<span data-ttu-id="4c8c0-103">Azure sanal ağı ağ geçidinin BGP eşlerini listeler</span><span class="sxs-lookup"><span data-stu-id="4c8c0-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="4c8c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c8c0-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c8c0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c8c0-105">DESCRIPTION</span></span>
<span data-ttu-id="4c8c0-106">Bu komut, BGP eşlerine bir Azure sanal ağı ağ geçidi eş olacak şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="4c8c0-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="4c8c0-107">Her eşin durumu da verilir.</span><span class="sxs-lookup"><span data-stu-id="4c8c0-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="4c8c0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c8c0-108">EXAMPLES</span></span>

### <span data-ttu-id="4c8c0-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4c8c0-109">Example 1</span></span>
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

<span data-ttu-id="4c8c0-110">Kaynak grubu resourceGroup 'da gatewayName adlı Azure sanal ağ geçidi için BGP eşlerini getirir.</span><span class="sxs-lookup"><span data-stu-id="4c8c0-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="4c8c0-111">Bu örnek çıktıda, 10.0.0.254 IP 'si olan bağlı bir BGP eşi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4c8c0-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="4c8c0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c8c0-112">PARAMETERS</span></span>

### <span data-ttu-id="4c8c0-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="4c8c0-113">-AsJob</span></span>
<span data-ttu-id="4c8c0-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4c8c0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c8c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c8c0-115">-DefaultProfile</span></span>
<span data-ttu-id="4c8c0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c8c0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c8c0-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="4c8c0-117">-Peer</span></span>
<span data-ttu-id="4c8c0-118">Durumu alacak olan eşin IP 'si</span><span class="sxs-lookup"><span data-stu-id="4c8c0-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="4c8c0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c8c0-119">-ResourceGroupName</span></span>
<span data-ttu-id="4c8c0-120">Sanal ağ geçidi kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4c8c0-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="4c8c0-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="4c8c0-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="4c8c0-122">Sanal ağ geçidi adı</span><span class="sxs-lookup"><span data-stu-id="4c8c0-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="4c8c0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c8c0-123">CommonParameters</span></span>
<span data-ttu-id="4c8c0-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c8c0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c8c0-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4c8c0-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c8c0-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c8c0-126">INPUTS</span></span>

### <span data-ttu-id="4c8c0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4c8c0-127">System.String</span></span>

## <span data-ttu-id="4c8c0-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c8c0-128">OUTPUTS</span></span>

### <span data-ttu-id="4c8c0-129">Microsoft. Azure. Commands. Network. model. PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="4c8c0-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="4c8c0-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c8c0-130">NOTES</span></span>

## <span data-ttu-id="4c8c0-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c8c0-131">RELATED LINKS</span></span>