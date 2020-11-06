---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/confirm-azurermcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
ms.openlocfilehash: d6cf25c352c89592112aaa0a60cf7ba14ff7acf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591397"
---
# <span data-ttu-id="d3b21-101">Confirm-AzureRmCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="d3b21-101">Confirm-AzureRmCdnEndpointProbeURL</span></span>

## <span data-ttu-id="d3b21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3b21-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b21-103">Araştırma URL 'sini doğrular.</span><span class="sxs-lookup"><span data-stu-id="d3b21-103">Validates a probe URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3b21-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3b21-104">SYNTAX</span></span>

```
Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3b21-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3b21-105">DESCRIPTION</span></span>
<span data-ttu-id="d3b21-106">**Confirm-AzureRmCdnEndpointProbeURL** cmdlet 'i, sağlanan araştırma URL 'sinin dinamik site ivmesi için kullanılabileceğini doğrular.</span><span class="sxs-lookup"><span data-stu-id="d3b21-106">The **Confirm-AzureRmCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="d3b21-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3b21-107">EXAMPLES</span></span>

### <span data-ttu-id="d3b21-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d3b21-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="d3b21-109">Araştırma URL 'sini doğrular " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="d3b21-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="d3b21-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3b21-110">PARAMETERS</span></span>

### <span data-ttu-id="d3b21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b21-111">-DefaultProfile</span></span>
<span data-ttu-id="d3b21-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3b21-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3b21-113">-ProbeUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="d3b21-113">-ProbeUrl</span></span>
<span data-ttu-id="d3b21-114">Doğrulanacak araştırma URL adı.</span><span class="sxs-lookup"><span data-stu-id="d3b21-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="d3b21-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b21-115">CommonParameters</span></span>
<span data-ttu-id="d3b21-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3b21-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b21-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3b21-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b21-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3b21-118">INPUTS</span></span>

### <span data-ttu-id="d3b21-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d3b21-119">None</span></span>

## <span data-ttu-id="d3b21-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3b21-120">OUTPUTS</span></span>

### <span data-ttu-id="d3b21-121">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="d3b21-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="d3b21-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3b21-122">NOTES</span></span>

## <span data-ttu-id="d3b21-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3b21-123">RELATED LINKS</span></span>
