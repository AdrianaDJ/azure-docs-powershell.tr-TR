---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: c881232c065f8494b962a0e010865cbefe8bc0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592184"
---
# <span data-ttu-id="3b124-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b124-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="3b124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b124-102">SYNOPSIS</span></span>
<span data-ttu-id="3b124-103">Yerel ağ geçidi alır</span><span class="sxs-lookup"><span data-stu-id="3b124-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b124-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b124-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b124-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b124-105">DESCRIPTION</span></span>
<span data-ttu-id="3b124-106">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="3b124-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="3b124-107">**Get-AzureRmLocalNetworkGateway** cmdlet 'i, şirket içi ağ geçidinizi temsil eden nesneyi ad ve kaynak grubu adına göre döndürür.</span><span class="sxs-lookup"><span data-stu-id="3b124-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="3b124-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b124-108">EXAMPLES</span></span>

### <span data-ttu-id="3b124-109">1: yerel ağ ağ geçidi alın</span><span class="sxs-lookup"><span data-stu-id="3b124-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="3b124-110">Yerel ağ geçidinin "myLocalGW" adlı yerel ağ geçidinin nesnesini, "myRG" kaynak grubunda döndürür</span><span class="sxs-lookup"><span data-stu-id="3b124-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="3b124-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b124-111">PARAMETERS</span></span>

### <span data-ttu-id="3b124-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b124-112">-Name</span></span>
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

### <span data-ttu-id="3b124-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b124-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="3b124-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b124-114">-DefaultProfile</span></span>
<span data-ttu-id="3b124-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b124-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b124-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b124-116">CommonParameters</span></span>
<span data-ttu-id="3b124-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b124-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b124-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b124-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b124-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b124-119">INPUTS</span></span>

## <span data-ttu-id="3b124-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b124-120">OUTPUTS</span></span>

### <span data-ttu-id="3b124-121">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3b124-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="3b124-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b124-122">NOTES</span></span>

## <span data-ttu-id="3b124-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b124-123">RELATED LINKS</span></span>

