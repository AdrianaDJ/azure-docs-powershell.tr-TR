---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 2de970201456f941d8b35d40c569c41e114468c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760485"
---
# <span data-ttu-id="3e435-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="3e435-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="3e435-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e435-102">SYNOPSIS</span></span>
<span data-ttu-id="3e435-103">Konum için kullanılabilir uç nokta hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="3e435-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="3e435-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e435-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e435-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e435-105">DESCRIPTION</span></span>
<span data-ttu-id="3e435-106">Get-AzVirtualNetworkAvailableEndpointService belirtilen konumda kullanılabilen uç nokta hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="3e435-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="3e435-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e435-107">EXAMPLES</span></span>

### <span data-ttu-id="3e435-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3e435-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="3e435-109">Westus bölgesinde kullanılabilir uç nokta hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3e435-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="3e435-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e435-110">PARAMETERS</span></span>

### <span data-ttu-id="3e435-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e435-111">-DefaultProfile</span></span>
<span data-ttu-id="3e435-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e435-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e435-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="3e435-113">-Location</span></span>
<span data-ttu-id="3e435-114">Bitiş noktası hizmetlerinin alınacağı konum.</span><span class="sxs-lookup"><span data-stu-id="3e435-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="3e435-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e435-115">CommonParameters</span></span>
<span data-ttu-id="3e435-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e435-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e435-117">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3e435-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e435-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e435-118">INPUTS</span></span>

### <span data-ttu-id="3e435-119">System. String</span><span class="sxs-lookup"><span data-stu-id="3e435-119">System.String</span></span>

## <span data-ttu-id="3e435-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e435-120">OUTPUTS</span></span>

### <span data-ttu-id="3e435-121">Microsoft. Azure. Commands. Network. modeller. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="3e435-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="3e435-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e435-122">NOTES</span></span>

## <span data-ttu-id="3e435-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e435-123">RELATED LINKS</span></span>
