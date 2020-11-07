---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937450"
---
# <span data-ttu-id="1068d-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="1068d-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="1068d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1068d-102">SYNOPSIS</span></span> 
<span data-ttu-id="1068d-103">Verilen bağlanılan VPN istemci bağlantılarının belirli bir sanal ağ ağ geçidiyle bağlantısını kesin.</span><span class="sxs-lookup"><span data-stu-id="1068d-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="1068d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1068d-104">SYNTAX</span></span>
### <span data-ttu-id="1068d-105">ByVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1068d-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="1068d-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="1068d-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="1068d-107">Byvpngatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="1068d-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="1068d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1068d-108">DESCRIPTION</span></span>
<span data-ttu-id="1068d-109">**Bağlantı kesilmesi-AzVirtualNetworkGatewayVpnConnection** cmdlet 'i, bağlanılan bağlanılan VPN istemci bağlantısının bağlantısını kesmenizi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="1068d-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="1068d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1068d-110">EXAMPLES</span></span>

### <span data-ttu-id="1068d-111">Örnekteki</span><span class="sxs-lookup"><span data-stu-id="1068d-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="1068d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1068d-112">PARAMETERS</span></span>

### <span data-ttu-id="1068d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1068d-113">-ResourceGroupName</span></span>
<span data-ttu-id="1068d-114">Sanal ağ geçidi kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1068d-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1068d-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1068d-115">-ResourceName</span></span>
<span data-ttu-id="1068d-116">Sanal ağ geçidi adı</span><span class="sxs-lookup"><span data-stu-id="1068d-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1068d-117">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1068d-117">-ResourceId</span></span>
<span data-ttu-id="1068d-118">Sanal ağ geçidi kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="1068d-118">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1068d-119">-Vpnconnectionıd</span><span class="sxs-lookup"><span data-stu-id="1068d-119">-VpnConnectionId</span></span>
<span data-ttu-id="1068d-120">VPN bağlantı kimlikleri</span><span class="sxs-lookup"><span data-stu-id="1068d-120">Vpn Connection Ids</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1068d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1068d-121">-InputObject</span></span>
<span data-ttu-id="1068d-122">Sanal ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="1068d-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1068d-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="1068d-123">-AsJob</span></span>
<span data-ttu-id="1068d-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1068d-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1068d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1068d-125">CommonParameters</span></span>
<span data-ttu-id="1068d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1068d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1068d-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1068d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1068d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1068d-128">INPUTS</span></span>

### <span data-ttu-id="1068d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1068d-129">System.String</span></span>

## <span data-ttu-id="1068d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1068d-130">OUTPUTS</span></span>

### <span data-ttu-id="1068d-131">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1068d-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1068d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1068d-132">NOTES</span></span>

## <span data-ttu-id="1068d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1068d-133">RELATED LINKS</span></span>
