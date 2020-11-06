---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: c5db5d27edb537602638ff5654a6da3ac35813ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592328"
---
# <span data-ttu-id="c5d93-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c5d93-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="c5d93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5d93-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d93-103">CDN uç noktasının uygunluk durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c5d93-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5d93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5d93-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5d93-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5d93-105">DESCRIPTION</span></span>
<span data-ttu-id="c5d93-106">**Get-Azurermcdnendpointnameuygunluk** cmdlet 'ı Azure Içerik teslim ağı (CDN) uç noktasının uygunluk durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c5d93-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="c5d93-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5d93-107">EXAMPLES</span></span>

## <span data-ttu-id="c5d93-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5d93-108">PARAMETERS</span></span>

### <span data-ttu-id="c5d93-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d93-109">-DefaultProfile</span></span>
<span data-ttu-id="c5d93-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c5d93-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5d93-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c5d93-111">-EndpointName</span></span>
<span data-ttu-id="c5d93-112">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5d93-112">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d93-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d93-113">CommonParameters</span></span>
<span data-ttu-id="c5d93-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5d93-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d93-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5d93-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d93-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5d93-116">INPUTS</span></span>

### <span data-ttu-id="c5d93-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c5d93-117">None</span></span>

## <span data-ttu-id="c5d93-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5d93-118">OUTPUTS</span></span>

### <span data-ttu-id="c5d93-119">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="c5d93-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="c5d93-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5d93-120">NOTES</span></span>

## <span data-ttu-id="c5d93-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5d93-121">RELATED LINKS</span></span>
