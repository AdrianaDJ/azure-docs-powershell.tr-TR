---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinktarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
ms.openlocfilehash: beb4fad10424a94b2623070508ac827ea7b15306
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938612"
---
# <span data-ttu-id="1e54c-101">Get-AzOperationalInsightsLinkTarget</span><span class="sxs-lookup"><span data-stu-id="1e54c-101">Get-AzOperationalInsightsLinkTarget</span></span>

## <span data-ttu-id="1e54c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e54c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e54c-103">Abonelikle ilişkilendirilmemiş hesapları alır.</span><span class="sxs-lookup"><span data-stu-id="1e54c-103">Gets accounts that are not associated with a subscription.</span></span>

## <span data-ttu-id="1e54c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e54c-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkTarget [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e54c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e54c-105">DESCRIPTION</span></span>
<span data-ttu-id="1e54c-106">**Get-Azişlemkimliği** , bir Azure aboneliğiyle ilişkilendirilmemiş mevcut hesapları listeler.</span><span class="sxs-lookup"><span data-stu-id="1e54c-106">The **Get-AzOperationalInsightsLinkTarget** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="1e54c-107">Yeni bir çalışma alanını varolan bir hesaba bağlamak için, yeni bir çalışma alanının müşteri KIMLIĞI özelliğinde bu işlem tarafından döndürülen bir müşteri KIMLIĞI kullanın.</span><span class="sxs-lookup"><span data-stu-id="1e54c-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="1e54c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e54c-108">EXAMPLES</span></span>

### <span data-ttu-id="1e54c-109">Örnek 1: bağlantısız hesapları alma</span><span class="sxs-lookup"><span data-stu-id="1e54c-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzOperationalInsightsLinkTarget
```

<span data-ttu-id="1e54c-110">Bu komut arayan KIMLIĞININ sahibi olduğu bağlantısız hesapları alır.</span><span class="sxs-lookup"><span data-stu-id="1e54c-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="1e54c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e54c-111">PARAMETERS</span></span>

### <span data-ttu-id="1e54c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e54c-112">-DefaultProfile</span></span>
<span data-ttu-id="1e54c-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1e54c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e54c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e54c-114">CommonParameters</span></span>
<span data-ttu-id="1e54c-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e54c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e54c-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e54c-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e54c-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e54c-117">INPUTS</span></span>

### <span data-ttu-id="1e54c-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1e54c-118">None</span></span>

## <span data-ttu-id="1e54c-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e54c-119">OUTPUTS</span></span>

### <span data-ttu-id="1e54c-120">Microsoft. Azure. Commands. Operationalınsights. model. PSAccount</span><span class="sxs-lookup"><span data-stu-id="1e54c-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="1e54c-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e54c-121">NOTES</span></span>

## <span data-ttu-id="1e54c-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e54c-122">RELATED LINKS</span></span>

[<span data-ttu-id="1e54c-123">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="1e54c-123">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


