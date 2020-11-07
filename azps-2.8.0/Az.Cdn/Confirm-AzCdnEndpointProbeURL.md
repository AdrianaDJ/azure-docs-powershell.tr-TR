---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: 517fb30fd95bfc435fcc847a7f9f0765befc21c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753099"
---
# <span data-ttu-id="9bb12-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="9bb12-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="9bb12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bb12-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb12-103">Araştırma URL 'sini doğrular.</span><span class="sxs-lookup"><span data-stu-id="9bb12-103">Validates a probe URL.</span></span>

## <span data-ttu-id="9bb12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bb12-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bb12-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bb12-105">DESCRIPTION</span></span>
<span data-ttu-id="9bb12-106">**Confirm-AzCdnEndpointProbeURL** cmdlet 'i, sağlanan araştırma URL 'sinin dinamik site ivmesi için kullanılabileceğini doğrular.</span><span class="sxs-lookup"><span data-stu-id="9bb12-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="9bb12-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bb12-107">EXAMPLES</span></span>

### <span data-ttu-id="9bb12-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9bb12-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="9bb12-109">Araştırma URL 'sini doğrular " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="9bb12-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="9bb12-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bb12-110">PARAMETERS</span></span>

### <span data-ttu-id="9bb12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb12-111">-DefaultProfile</span></span>
<span data-ttu-id="9bb12-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9bb12-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bb12-113">-ProbeUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="9bb12-113">-ProbeUrl</span></span>
<span data-ttu-id="9bb12-114">Doğrulanacak araştırma URL adı.</span><span class="sxs-lookup"><span data-stu-id="9bb12-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="9bb12-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb12-115">CommonParameters</span></span>
<span data-ttu-id="9bb12-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bb12-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb12-117">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9bb12-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb12-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bb12-118">INPUTS</span></span>

### <span data-ttu-id="9bb12-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9bb12-119">None</span></span>

## <span data-ttu-id="9bb12-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bb12-120">OUTPUTS</span></span>

### <span data-ttu-id="9bb12-121">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="9bb12-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="9bb12-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bb12-122">NOTES</span></span>

## <span data-ttu-id="9bb12-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bb12-123">RELATED LINKS</span></span>
