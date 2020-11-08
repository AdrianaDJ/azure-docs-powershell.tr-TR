---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096454"
---
# <span data-ttu-id="06914-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="06914-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="06914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06914-102">SYNOPSIS</span></span>
<span data-ttu-id="06914-103">CDN uç noktasının uygunluk durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="06914-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="06914-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06914-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06914-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06914-105">DESCRIPTION</span></span>
<span data-ttu-id="06914-106">**Get-Azcdnendpointnameuygunluk** cmdlet 'ı Azure Içerik teslim ağı (CDN) uç noktasının uygunluk durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="06914-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="06914-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06914-107">EXAMPLES</span></span>

## <span data-ttu-id="06914-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06914-108">PARAMETERS</span></span>

### <span data-ttu-id="06914-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06914-109">-DefaultProfile</span></span>
<span data-ttu-id="06914-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="06914-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06914-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="06914-111">-EndpointName</span></span>
<span data-ttu-id="06914-112">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06914-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="06914-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06914-113">CommonParameters</span></span>
<span data-ttu-id="06914-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06914-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06914-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="06914-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06914-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06914-116">INPUTS</span></span>

### <span data-ttu-id="06914-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="06914-117">None</span></span>

## <span data-ttu-id="06914-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06914-118">OUTPUTS</span></span>

### <span data-ttu-id="06914-119">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="06914-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="06914-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06914-120">NOTES</span></span>

## <span data-ttu-id="06914-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06914-121">RELATED LINKS</span></span>
