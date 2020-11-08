---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096157"
---
# <span data-ttu-id="41f69-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="41f69-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="41f69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41f69-102">SYNOPSIS</span></span>
<span data-ttu-id="41f69-103">Sanal ağ geçidi bağlantısını alır</span><span class="sxs-lookup"><span data-stu-id="41f69-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="41f69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41f69-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41f69-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="41f69-105">DESCRIPTION</span></span>
<span data-ttu-id="41f69-106">Sanal ağ geçidi bağlantısı, Azure 'daki sanal ağ geçidine bağlı olan IPSec tüneli (siteden siteye veya VNET arası) temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="41f69-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="41f69-107">**Get-AzVirtualNetworkGatewayConnection** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak bağlantınızın nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="41f69-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="41f69-108">-Name parametresini belirtmeden **Get-AzVirtualNetworkGatewayConnection** cmdlet 'i verildiyse, çıkış ConnectionStatus ve sharedkey ayrıntılarını göstermez.</span><span class="sxs-lookup"><span data-stu-id="41f69-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="41f69-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41f69-109">EXAMPLES</span></span>

### <span data-ttu-id="41f69-110">1: sanal ağ geçidi bağlantısı edinin</span><span class="sxs-lookup"><span data-stu-id="41f69-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="41f69-111">Sanal Ağ Geçidi bağlantısının "myTunnel" adlı sanal ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="41f69-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="41f69-112">2: filtreleme kullanarak tüm sanal ağ ağ geçidi bağlantılarını alma</span><span class="sxs-lookup"><span data-stu-id="41f69-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="41f69-113">"MyRG" kaynak grubunda "myTunnel" ile başlayan tüm sanal ağ geçidi bağlantılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="41f69-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="41f69-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41f69-114">PARAMETERS</span></span>

### <span data-ttu-id="41f69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f69-115">-DefaultProfile</span></span>
<span data-ttu-id="41f69-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="41f69-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41f69-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="41f69-117">-Name</span></span>
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

### <span data-ttu-id="41f69-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f69-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="41f69-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f69-119">CommonParameters</span></span>
<span data-ttu-id="41f69-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41f69-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f69-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="41f69-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f69-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41f69-122">INPUTS</span></span>

### <span data-ttu-id="41f69-123">System. String</span><span class="sxs-lookup"><span data-stu-id="41f69-123">System.String</span></span>

## <span data-ttu-id="41f69-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41f69-124">OUTPUTS</span></span>

### <span data-ttu-id="41f69-125">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="41f69-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="41f69-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41f69-126">NOTES</span></span>

## <span data-ttu-id="41f69-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41f69-127">RELATED LINKS</span></span>

[<span data-ttu-id="41f69-128">Yeni-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="41f69-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="41f69-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="41f69-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="41f69-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="41f69-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)