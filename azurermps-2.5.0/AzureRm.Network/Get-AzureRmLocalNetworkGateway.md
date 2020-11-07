---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1a2a8aa8405be5dfc5275a07d253f06f1134e3e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939529"
---
# <span data-ttu-id="1396d-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1396d-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="1396d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1396d-102">SYNOPSIS</span></span>
<span data-ttu-id="1396d-103">Yerel ağ geçidi alır</span><span class="sxs-lookup"><span data-stu-id="1396d-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1396d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1396d-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1396d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1396d-105">DESCRIPTION</span></span>
<span data-ttu-id="1396d-106">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="1396d-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="1396d-107">**Get-AzureRmLocalNetworkGateway** cmdlet 'i, şirket içi ağ geçidinizi temsil eden nesneyi ad ve kaynak grubu adına göre döndürür.</span><span class="sxs-lookup"><span data-stu-id="1396d-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="1396d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1396d-108">EXAMPLES</span></span>

### <span data-ttu-id="1396d-109">1: yerel ağ ağ geçidi alın</span><span class="sxs-lookup"><span data-stu-id="1396d-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="1396d-110">Yerel ağ geçidinin "myLocalGW" adlı yerel ağ geçidinin nesnesini, "myRG" kaynak grubunda döndürür</span><span class="sxs-lookup"><span data-stu-id="1396d-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="1396d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1396d-111">PARAMETERS</span></span>

### <span data-ttu-id="1396d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1396d-112">-DefaultProfile</span></span>
<span data-ttu-id="1396d-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1396d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1396d-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="1396d-114">-Name</span></span>
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

### <span data-ttu-id="1396d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1396d-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="1396d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1396d-116">CommonParameters</span></span>
<span data-ttu-id="1396d-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1396d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1396d-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1396d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1396d-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1396d-119">INPUTS</span></span>

## <span data-ttu-id="1396d-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1396d-120">OUTPUTS</span></span>

### <span data-ttu-id="1396d-121">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1396d-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="1396d-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1396d-122">NOTES</span></span>

## <span data-ttu-id="1396d-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1396d-123">RELATED LINKS</span></span>

