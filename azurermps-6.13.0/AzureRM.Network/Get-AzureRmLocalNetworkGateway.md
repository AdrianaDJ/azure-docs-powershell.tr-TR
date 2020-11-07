---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 522516df5d4500f55a17e769140149f021501210
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765097"
---
# <span data-ttu-id="7aa49-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7aa49-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="7aa49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7aa49-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa49-103">Yerel ağ geçidi alır</span><span class="sxs-lookup"><span data-stu-id="7aa49-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7aa49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7aa49-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7aa49-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7aa49-105">DESCRIPTION</span></span>
<span data-ttu-id="7aa49-106">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="7aa49-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="7aa49-107">**Get-AzureRmLocalNetworkGateway** cmdlet 'i, şirket içi ağ geçidinizi temsil eden nesneyi ad ve kaynak grubu adına göre döndürür.</span><span class="sxs-lookup"><span data-stu-id="7aa49-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="7aa49-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7aa49-108">EXAMPLES</span></span>

### <span data-ttu-id="7aa49-109">1: yerel ağ ağ geçidi alın</span><span class="sxs-lookup"><span data-stu-id="7aa49-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="7aa49-110">Yerel ağ geçidinin "myLocalGW" adlı yerel ağ geçidinin nesnesini, "myRG" kaynak grubunda döndürür</span><span class="sxs-lookup"><span data-stu-id="7aa49-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="7aa49-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7aa49-111">PARAMETERS</span></span>

### <span data-ttu-id="7aa49-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa49-112">-DefaultProfile</span></span>
<span data-ttu-id="7aa49-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7aa49-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aa49-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="7aa49-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa49-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aa49-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="7aa49-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa49-116">CommonParameters</span></span>
<span data-ttu-id="7aa49-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7aa49-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa49-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aa49-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa49-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7aa49-119">INPUTS</span></span>

### <span data-ttu-id="7aa49-120">System. String</span><span class="sxs-lookup"><span data-stu-id="7aa49-120">System.String</span></span>

## <span data-ttu-id="7aa49-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7aa49-121">OUTPUTS</span></span>

### <span data-ttu-id="7aa49-122">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7aa49-122">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="7aa49-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7aa49-123">NOTES</span></span>

## <span data-ttu-id="7aa49-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7aa49-124">RELATED LINKS</span></span>
