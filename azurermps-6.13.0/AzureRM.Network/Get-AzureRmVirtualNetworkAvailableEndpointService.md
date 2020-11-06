---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 7499c96ec887673faaf93cf2901e4705b63604b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595072"
---
# <span data-ttu-id="f5edb-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="f5edb-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="f5edb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5edb-102">SYNOPSIS</span></span>
<span data-ttu-id="f5edb-103">Konum için kullanılabilir uç nokta hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="f5edb-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5edb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5edb-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5edb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5edb-105">DESCRIPTION</span></span>
<span data-ttu-id="f5edb-106">Get-AzureRmVirtualNetworkAvailableEndpointService belirtilen konumda kullanılabilen uç nokta hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="f5edb-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="f5edb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5edb-107">EXAMPLES</span></span>

### <span data-ttu-id="f5edb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f5edb-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="f5edb-109">Westus bölgesinde kullanılabilir uç nokta hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f5edb-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="f5edb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5edb-110">PARAMETERS</span></span>

### <span data-ttu-id="f5edb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5edb-111">-DefaultProfile</span></span>
<span data-ttu-id="f5edb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5edb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5edb-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="f5edb-113">-Location</span></span>
<span data-ttu-id="f5edb-114">Bitiş noktası hizmetlerinin alınacağı konum.</span><span class="sxs-lookup"><span data-stu-id="f5edb-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="f5edb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5edb-115">CommonParameters</span></span>
<span data-ttu-id="f5edb-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5edb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5edb-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5edb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5edb-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5edb-118">INPUTS</span></span>

### <span data-ttu-id="f5edb-119">System. String</span><span class="sxs-lookup"><span data-stu-id="f5edb-119">System.String</span></span>

## <span data-ttu-id="f5edb-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5edb-120">OUTPUTS</span></span>

### <span data-ttu-id="f5edb-121">Microsoft. Azure. Commands. Network. modeller. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="f5edb-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="f5edb-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5edb-122">NOTES</span></span>

## <span data-ttu-id="f5edb-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5edb-123">RELATED LINKS</span></span>
