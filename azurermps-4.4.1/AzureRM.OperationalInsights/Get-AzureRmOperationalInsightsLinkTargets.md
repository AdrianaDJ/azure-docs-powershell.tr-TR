---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: 3f0418a06b11af933cfc7ad09a2c0fc492db4f24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593048"
---
# <span data-ttu-id="2627a-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="2627a-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="2627a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2627a-102">SYNOPSIS</span></span>
<span data-ttu-id="2627a-103">Abonelikle ilişkilendirilmemiş hesapları alır.</span><span class="sxs-lookup"><span data-stu-id="2627a-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2627a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2627a-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2627a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2627a-105">DESCRIPTION</span></span>
<span data-ttu-id="2627a-106">**Get-Azurermoperationalınsightslinktargets** cmdlet 'ı bir Azure aboneliğiyle ilişkilendirilmemiş mevcut hesapları listeler.</span><span class="sxs-lookup"><span data-stu-id="2627a-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="2627a-107">Yeni bir çalışma alanını varolan bir hesaba bağlamak için, yeni bir çalışma alanının müşteri KIMLIĞI özelliğinde bu işlem tarafından döndürülen bir müşteri KIMLIĞI kullanın.</span><span class="sxs-lookup"><span data-stu-id="2627a-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="2627a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2627a-108">EXAMPLES</span></span>

### <span data-ttu-id="2627a-109">Örnek 1: bağlantısız hesapları alma</span><span class="sxs-lookup"><span data-stu-id="2627a-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="2627a-110">Bu komut arayan KIMLIĞININ sahibi olduğu bağlantısız hesapları alır.</span><span class="sxs-lookup"><span data-stu-id="2627a-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="2627a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2627a-111">PARAMETERS</span></span>

### <span data-ttu-id="2627a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2627a-112">-DefaultProfile</span></span>
<span data-ttu-id="2627a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2627a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2627a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2627a-114">CommonParameters</span></span>
<span data-ttu-id="2627a-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2627a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2627a-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2627a-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2627a-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2627a-117">INPUTS</span></span>

## <span data-ttu-id="2627a-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2627a-118">OUTPUTS</span></span>

### <span data-ttu-id="2627a-119">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Operationalınsights. model. PSAccount]</span><span class="sxs-lookup"><span data-stu-id="2627a-119">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount]</span></span>

## <span data-ttu-id="2627a-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2627a-120">NOTES</span></span>

## <span data-ttu-id="2627a-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2627a-121">RELATED LINKS</span></span>

[<span data-ttu-id="2627a-122">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="2627a-122">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


