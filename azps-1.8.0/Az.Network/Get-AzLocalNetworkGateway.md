---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 04cec0db46eef985819ea44355b9bbedf792dbf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760544"
---
# <span data-ttu-id="9d4d3-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9d4d3-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="9d4d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="9d4d3-103">Yerel ağ geçidi alır</span><span class="sxs-lookup"><span data-stu-id="9d4d3-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="9d4d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d4d3-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d4d3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d4d3-105">DESCRIPTION</span></span>
<span data-ttu-id="9d4d3-106">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="9d4d3-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="9d4d3-107">**Get-AzLocalNetworkGateway** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak şirket içi ağ geçidinizi temsil eden nesneyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="9d4d3-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="9d4d3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d4d3-108">EXAMPLES</span></span>

### <span data-ttu-id="9d4d3-109">1: yerel ağ ağ geçidi alın</span><span class="sxs-lookup"><span data-stu-id="9d4d3-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="9d4d3-110">Yerel ağ geçidinin "myLocalGW1" adıyla "myRG" adlı yerel ağ geçidinin nesnesini döndürür</span><span class="sxs-lookup"><span data-stu-id="9d4d3-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="9d4d3-111">2: filtreleme kullanarak yerel ağ geçitleri alma</span><span class="sxs-lookup"><span data-stu-id="9d4d3-111">2: Get Local Network Gateways using filtering</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="9d4d3-112">"MyRG" kaynak grubunda "myLocalGW" ile başlayan yerel ağ ağ geçidinin nesnesini döndürür</span><span class="sxs-lookup"><span data-stu-id="9d4d3-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="9d4d3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d4d3-113">PARAMETERS</span></span>

### <span data-ttu-id="9d4d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d4d3-114">-DefaultProfile</span></span>
<span data-ttu-id="9d4d3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9d4d3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d4d3-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="9d4d3-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9d4d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d4d3-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9d4d3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d4d3-118">CommonParameters</span></span>
<span data-ttu-id="9d4d3-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d4d3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d4d3-120">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9d4d3-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d4d3-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d4d3-121">INPUTS</span></span>

### <span data-ttu-id="9d4d3-122">System. String</span><span class="sxs-lookup"><span data-stu-id="9d4d3-122">System.String</span></span>

## <span data-ttu-id="9d4d3-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d4d3-123">OUTPUTS</span></span>

### <span data-ttu-id="9d4d3-124">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9d4d3-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="9d4d3-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d4d3-125">NOTES</span></span>

## <span data-ttu-id="9d4d3-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d4d3-126">RELATED LINKS</span></span>

[<span data-ttu-id="9d4d3-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9d4d3-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="9d4d3-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9d4d3-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="9d4d3-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9d4d3-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
