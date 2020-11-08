---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/send-feedback
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
ms.openlocfilehash: 1405886572efabf1ffc91f071f262ca98515d141
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097475"
---
# <span data-ttu-id="dd0de-101">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="dd0de-101">Send-Feedback</span></span>

## <span data-ttu-id="dd0de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd0de-102">SYNOPSIS</span></span>
<span data-ttu-id="dd0de-103">Bir dizi Kılavuzlu istem aracılığıyla Azure PowerShell ekibine görüşler gönderir.</span><span class="sxs-lookup"><span data-stu-id="dd0de-103">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

## <span data-ttu-id="dd0de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd0de-104">SYNTAX</span></span>

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd0de-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd0de-105">DESCRIPTION</span></span>
<span data-ttu-id="dd0de-106">Send-Feedback cmdlet 'i Azure PowerShell ekibine görüşlerinizi gönderir.</span><span class="sxs-lookup"><span data-stu-id="dd0de-106">The Send-Feedback cmdlet sends feedback to the Azure PowerShell team.</span></span>

## <span data-ttu-id="dd0de-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd0de-107">EXAMPLES</span></span>

### <span data-ttu-id="dd0de-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="dd0de-108">Example 1:</span></span>
```
PS C:\> Send-Feedback

With zero (0) being the least and ten (10) being the most, how likely are you to recommend Azure PowerShell to a friend or colleague?

10

What does Azure PowerShell do well?

Response.

Upon what could Azure PowerShell improve?

Response.

Please enter your email if you are interested in providing follow up information:

your@email.com
```

## <span data-ttu-id="dd0de-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd0de-109">PARAMETERS</span></span>

### <span data-ttu-id="dd0de-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd0de-110">-DefaultProfile</span></span>
<span data-ttu-id="dd0de-111">Azure ile iletişim için kullanılan kimlik bilgileri, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd0de-111">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd0de-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd0de-112">CommonParameters</span></span>
<span data-ttu-id="dd0de-113">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd0de-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd0de-114">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd0de-114">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd0de-115">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd0de-115">INPUTS</span></span>

### <span data-ttu-id="dd0de-116">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dd0de-116">None</span></span>

## <span data-ttu-id="dd0de-117">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd0de-117">OUTPUTS</span></span>

### <span data-ttu-id="dd0de-118">System. void</span><span class="sxs-lookup"><span data-stu-id="dd0de-118">System.Void</span></span>

## <span data-ttu-id="dd0de-119">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd0de-119">NOTES</span></span>

## <span data-ttu-id="dd0de-120">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd0de-120">RELATED LINKS</span></span>