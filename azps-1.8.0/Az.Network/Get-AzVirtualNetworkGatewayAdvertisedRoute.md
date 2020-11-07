---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: f7ac40d088cca1b88a5a4a5413fe048faac99d1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760483"
---
# <span data-ttu-id="a1b37-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="a1b37-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="a1b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1b37-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b37-103">Bir Azure sanal ağ ağ geçidi tarafından tanıtılan yolları listeler</span><span class="sxs-lookup"><span data-stu-id="a1b37-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="a1b37-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1b37-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1b37-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1b37-105">DESCRIPTION</span></span>
<span data-ttu-id="a1b37-106">BGP eşinin IP 'si verildiğinde, belirtilen Azure sanal ağ ağ geçidiyle bu eşe tanıtılan yolları numaralandırır.</span><span class="sxs-lookup"><span data-stu-id="a1b37-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="a1b37-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1b37-107">EXAMPLES</span></span>

### <span data-ttu-id="a1b37-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a1b37-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="a1b37-109">Kaynak grubunda gatewayName adlı Azure ağ geçidi için, IP 10.0.0.254 ile BGP eşine tanıtılmakta olan yolların listesini yönlendirir</span><span class="sxs-lookup"><span data-stu-id="a1b37-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="a1b37-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a1b37-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="a1b37-111">ResourceGroupName kaynak grubunda gatewayName adlı Azure ağ geçidi için, tanıtılmakta olan yolları ağ geçidinin BGP eşleri listesindeki ilk BGP eşine getirir.</span><span class="sxs-lookup"><span data-stu-id="a1b37-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="a1b37-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1b37-112">PARAMETERS</span></span>

### <span data-ttu-id="a1b37-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a1b37-113">-AsJob</span></span>
<span data-ttu-id="a1b37-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a1b37-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1b37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b37-115">-DefaultProfile</span></span>
<span data-ttu-id="a1b37-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1b37-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1b37-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="a1b37-117">-Peer</span></span>
<span data-ttu-id="a1b37-118">BGP eşinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="a1b37-118">BGP peer's IP address.</span></span> <span data-ttu-id="a1b37-119">Bu, Azure sanal ağının içinden ağ üzerinden erişilebilen adres alanı içinde bir IP olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a1b37-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="a1b37-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b37-120">-ResourceGroupName</span></span>
<span data-ttu-id="a1b37-121">Sanal ağ geçidi kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a1b37-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="a1b37-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a1b37-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a1b37-123">Sanal ağ geçidi adı</span><span class="sxs-lookup"><span data-stu-id="a1b37-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="a1b37-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b37-124">CommonParameters</span></span>
<span data-ttu-id="a1b37-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1b37-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b37-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a1b37-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b37-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1b37-127">INPUTS</span></span>

### <span data-ttu-id="a1b37-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a1b37-128">System.String</span></span>

## <span data-ttu-id="a1b37-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1b37-129">OUTPUTS</span></span>

### <span data-ttu-id="a1b37-130">Microsoft. Azure. Commands. Network. model. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="a1b37-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="a1b37-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1b37-131">NOTES</span></span>
<span data-ttu-id="a1b37-132">Bu komut yalnızca BGP etkinleştirilmiş bağlantılar içeren Azure sanal ağ geçitleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="a1b37-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="a1b37-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1b37-133">RELATED LINKS</span></span>
