---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
ms.openlocfilehash: ed33d1a683e10e0e39d0b722dec92b7f7ba11254
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939109"
---
# <span data-ttu-id="1fb0b-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="1fb0b-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="1fb0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fb0b-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb0b-103">Konum için kullanılabilir uç nokta hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="1fb0b-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fb0b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1fb0b-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fb0b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1fb0b-105">DESCRIPTION</span></span>
<span data-ttu-id="1fb0b-106">Get-AzureRmVirtualNetworkAvailableEndpointService belirtilen konumda kullanılabilen uç nokta hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="1fb0b-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="1fb0b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1fb0b-107">EXAMPLES</span></span>

### <span data-ttu-id="1fb0b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1fb0b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="1fb0b-109">Westus bölgesinde kullanılabilir uç nokta hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="1fb0b-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="1fb0b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1fb0b-110">PARAMETERS</span></span>

### <span data-ttu-id="1fb0b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb0b-111">-DefaultProfile</span></span>
<span data-ttu-id="1fb0b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1fb0b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fb0b-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="1fb0b-113">-Location</span></span>
<span data-ttu-id="1fb0b-114">Bitiş noktası hizmetlerinin alınacağı konum.</span><span class="sxs-lookup"><span data-stu-id="1fb0b-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="1fb0b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb0b-115">CommonParameters</span></span>
<span data-ttu-id="1fb0b-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1fb0b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb0b-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb0b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb0b-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1fb0b-118">INPUTS</span></span>

### <span data-ttu-id="1fb0b-119">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb0b-119">System.String</span></span>

## <span data-ttu-id="1fb0b-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1fb0b-120">OUTPUTS</span></span>

### <span data-ttu-id="1fb0b-121">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSEndpointServiceResult, Microsoft. Azure. Commands. Network, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1fb0b-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1fb0b-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1fb0b-122">NOTES</span></span>

## <span data-ttu-id="1fb0b-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1fb0b-123">RELATED LINKS</span></span>
