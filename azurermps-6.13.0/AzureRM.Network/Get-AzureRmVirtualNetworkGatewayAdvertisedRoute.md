---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: 288a2382470682c8c7b55f7342d5a0f193446019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595068"
---
# <span data-ttu-id="5d9d1-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="5d9d1-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="5d9d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d9d1-102">SYNOPSIS</span></span>
<span data-ttu-id="5d9d1-103">Bir Azure sanal ağ ağ geçidi tarafından tanıtılan yolları listeler</span><span class="sxs-lookup"><span data-stu-id="5d9d1-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d9d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d9d1-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d9d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d9d1-105">DESCRIPTION</span></span>
<span data-ttu-id="5d9d1-106">BGP eşinin IP 'si verildiğinde, belirtilen Azure sanal ağ ağ geçidiyle bu eşe tanıtılan yolları numaralandırır.</span><span class="sxs-lookup"><span data-stu-id="5d9d1-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="5d9d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d9d1-107">EXAMPLES</span></span>

### <span data-ttu-id="5d9d1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5d9d1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="5d9d1-109">Kaynak grubunda gatewayName adlı Azure ağ geçidi için, IP 10.0.0.254 ile BGP eşine tanıtılmakta olan yolların listesini yönlendirir</span><span class="sxs-lookup"><span data-stu-id="5d9d1-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="5d9d1-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5d9d1-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="5d9d1-111">ResourceGroupName kaynak grubunda gatewayName adlı Azure ağ geçidi için, tanıtılmakta olan yolları ağ geçidinin BGP eşleri listesindeki ilk BGP eşine getirir.</span><span class="sxs-lookup"><span data-stu-id="5d9d1-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="5d9d1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d9d1-112">PARAMETERS</span></span>

### <span data-ttu-id="5d9d1-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="5d9d1-113">-AsJob</span></span>
<span data-ttu-id="5d9d1-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5d9d1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d9d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d9d1-115">-DefaultProfile</span></span>
<span data-ttu-id="5d9d1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d9d1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d9d1-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="5d9d1-117">-Peer</span></span>
<span data-ttu-id="5d9d1-118">BGP eşinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="5d9d1-118">BGP peer's IP address.</span></span> <span data-ttu-id="5d9d1-119">Bu, Azure sanal ağının içinden ağ üzerinden erişilebilen adres alanı içinde bir IP olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5d9d1-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="5d9d1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d9d1-120">-ResourceGroupName</span></span>
<span data-ttu-id="5d9d1-121">Sanal ağ geçidi kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5d9d1-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="5d9d1-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5d9d1-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5d9d1-123">Sanal ağ geçidi adı</span><span class="sxs-lookup"><span data-stu-id="5d9d1-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="5d9d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d9d1-124">CommonParameters</span></span>
<span data-ttu-id="5d9d1-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d9d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d9d1-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d9d1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d9d1-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d9d1-127">INPUTS</span></span>

### <span data-ttu-id="5d9d1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5d9d1-128">System.String</span></span>

## <span data-ttu-id="5d9d1-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d9d1-129">OUTPUTS</span></span>

### <span data-ttu-id="5d9d1-130">Microsoft. Azure. Commands. Network. model. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="5d9d1-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="5d9d1-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d9d1-131">NOTES</span></span>
<span data-ttu-id="5d9d1-132">Bu komut yalnızca BGP etkinleştirilmiş bağlantılar içeren Azure sanal ağ geçitleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="5d9d1-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="5d9d1-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d9d1-133">RELATED LINKS</span></span>
