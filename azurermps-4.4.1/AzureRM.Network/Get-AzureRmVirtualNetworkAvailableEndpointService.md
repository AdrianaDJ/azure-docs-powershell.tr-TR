---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 15f1c71e313cfd684c384446f0ffd2913c69143c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591099"
---
# <span data-ttu-id="c1ff3-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="c1ff3-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="c1ff3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ff3-103">Konum için kullanılabilir uç nokta hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="c1ff3-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1ff3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1ff3-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1ff3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1ff3-105">DESCRIPTION</span></span>
<span data-ttu-id="c1ff3-106">Get-AzureRmVirtualNetworkAvailableEndpointService belirtilen konumda kullanılabilen uç nokta hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="c1ff3-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="c1ff3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1ff3-107">EXAMPLES</span></span>

### <span data-ttu-id="c1ff3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c1ff3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="c1ff3-109">Westus bölgesinde kullanılabilir uç nokta hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c1ff3-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="c1ff3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1ff3-110">PARAMETERS</span></span>

### <span data-ttu-id="c1ff3-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="c1ff3-111">-Location</span></span>
<span data-ttu-id="c1ff3-112">Bitiş noktası hizmetlerinin alınacağı konum.</span><span class="sxs-lookup"><span data-stu-id="c1ff3-112">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="c1ff3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ff3-113">-DefaultProfile</span></span>
<span data-ttu-id="c1ff3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1ff3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1ff3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ff3-115">CommonParameters</span></span>
<span data-ttu-id="c1ff3-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1ff3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ff3-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1ff3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ff3-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1ff3-118">INPUTS</span></span>

### <span data-ttu-id="c1ff3-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c1ff3-119">System.String</span></span>

## <span data-ttu-id="c1ff3-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1ff3-120">OUTPUTS</span></span>

### <span data-ttu-id="c1ff3-121">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSEndpointServiceResult, Microsoft. Azure. Commands. Network, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c1ff3-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c1ff3-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1ff3-122">NOTES</span></span>

## <span data-ttu-id="c1ff3-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1ff3-123">RELATED LINKS</span></span>

