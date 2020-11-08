---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 79517dc748a0599fca588e18d18a9d1e41f5e7fa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098754"
---
# <span data-ttu-id="c1c77-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="c1c77-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="c1c77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1c77-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c77-103">Konum için kullanılabilir uç nokta hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="c1c77-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="c1c77-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1c77-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1c77-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1c77-105">DESCRIPTION</span></span>
<span data-ttu-id="c1c77-106">Get-AzVirtualNetworkAvailableEndpointService belirtilen konumda kullanılabilen uç nokta hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="c1c77-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="c1c77-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1c77-107">EXAMPLES</span></span>

### <span data-ttu-id="c1c77-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c1c77-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="c1c77-109">Westus bölgesinde kullanılabilir uç nokta hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c1c77-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="c1c77-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1c77-110">PARAMETERS</span></span>

### <span data-ttu-id="c1c77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c77-111">-DefaultProfile</span></span>
<span data-ttu-id="c1c77-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1c77-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1c77-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="c1c77-113">-Location</span></span>
<span data-ttu-id="c1c77-114">Bitiş noktası hizmetlerinin alınacağı konum.</span><span class="sxs-lookup"><span data-stu-id="c1c77-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="c1c77-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c77-115">CommonParameters</span></span>
<span data-ttu-id="c1c77-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1c77-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c77-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c1c77-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c77-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1c77-118">INPUTS</span></span>

### <span data-ttu-id="c1c77-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c1c77-119">System.String</span></span>

## <span data-ttu-id="c1c77-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1c77-120">OUTPUTS</span></span>

### <span data-ttu-id="c1c77-121">Microsoft. Azure. Commands. Network. modeller. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="c1c77-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="c1c77-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1c77-122">NOTES</span></span>

## <span data-ttu-id="c1c77-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1c77-123">RELATED LINKS</span></span>
