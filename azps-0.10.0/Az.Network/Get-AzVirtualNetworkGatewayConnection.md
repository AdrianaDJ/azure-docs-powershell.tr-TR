---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8658dcf73d6cf1549ac6471e79269883abdf7616
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935469"
---
# <span data-ttu-id="5ea20-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5ea20-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="5ea20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ea20-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea20-103">Sanal ağ geçidi bağlantısını alır</span><span class="sxs-lookup"><span data-stu-id="5ea20-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="5ea20-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ea20-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ea20-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ea20-105">DESCRIPTION</span></span>
<span data-ttu-id="5ea20-106">Sanal ağ geçidi bağlantısı, Azure 'daki sanal ağ geçidine bağlı olan IPSec tüneli (siteden siteye veya VNET arası) temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="5ea20-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="5ea20-107">**Get-AzVirtualNetworkGatewayConnection** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak bağlantınızın nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5ea20-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="5ea20-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ea20-108">EXAMPLES</span></span>

### <span data-ttu-id="5ea20-109">1: sanal ağ geçidi bağlantısı edinin</span><span class="sxs-lookup"><span data-stu-id="5ea20-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="5ea20-110">Sanal Ağ Geçidi bağlantısının "myTunnel" adlı sanal ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="5ea20-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="5ea20-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ea20-111">PARAMETERS</span></span>

### <span data-ttu-id="5ea20-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea20-112">-DefaultProfile</span></span>
<span data-ttu-id="5ea20-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5ea20-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ea20-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="5ea20-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea20-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea20-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="5ea20-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea20-116">CommonParameters</span></span>
<span data-ttu-id="5ea20-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ea20-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea20-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ea20-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea20-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ea20-119">INPUTS</span></span>

## <span data-ttu-id="5ea20-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ea20-120">OUTPUTS</span></span>

### <span data-ttu-id="5ea20-121">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5ea20-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="5ea20-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ea20-122">NOTES</span></span>

## <span data-ttu-id="5ea20-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ea20-123">RELATED LINKS</span></span>

