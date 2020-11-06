---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightslinktargets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: a1040e5fe810a5dfbbb2e41daf7e8933102e3799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588433"
---
# <span data-ttu-id="f9ea4-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="f9ea4-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="f9ea4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ea4-103">Abonelikle ilişkilendirilmemiş hesapları alır.</span><span class="sxs-lookup"><span data-stu-id="f9ea4-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9ea4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9ea4-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9ea4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9ea4-105">DESCRIPTION</span></span>
<span data-ttu-id="f9ea4-106">**Get-Azurermoperationalınsightslinktargets** cmdlet 'ı bir Azure aboneliğiyle ilişkilendirilmemiş mevcut hesapları listeler.</span><span class="sxs-lookup"><span data-stu-id="f9ea4-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="f9ea4-107">Yeni bir çalışma alanını varolan bir hesaba bağlamak için, yeni bir çalışma alanının müşteri KIMLIĞI özelliğinde bu işlem tarafından döndürülen bir müşteri KIMLIĞI kullanın.</span><span class="sxs-lookup"><span data-stu-id="f9ea4-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="f9ea4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9ea4-108">EXAMPLES</span></span>

### <span data-ttu-id="f9ea4-109">Örnek 1: bağlantısız hesapları alma</span><span class="sxs-lookup"><span data-stu-id="f9ea4-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="f9ea4-110">Bu komut arayan KIMLIĞININ sahibi olduğu bağlantısız hesapları alır.</span><span class="sxs-lookup"><span data-stu-id="f9ea4-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="f9ea4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9ea4-111">PARAMETERS</span></span>

### <span data-ttu-id="f9ea4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ea4-112">-DefaultProfile</span></span>
<span data-ttu-id="f9ea4-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f9ea4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9ea4-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ea4-114">CommonParameters</span></span>
<span data-ttu-id="f9ea4-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9ea4-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ea4-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9ea4-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ea4-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9ea4-117">INPUTS</span></span>

### <span data-ttu-id="f9ea4-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f9ea4-118">None</span></span>

## <span data-ttu-id="f9ea4-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9ea4-119">OUTPUTS</span></span>

### <span data-ttu-id="f9ea4-120">Microsoft. Azure. Commands. Operationalınsights. model. PSAccount</span><span class="sxs-lookup"><span data-stu-id="f9ea4-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="f9ea4-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9ea4-121">NOTES</span></span>

## <span data-ttu-id="f9ea4-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9ea4-122">RELATED LINKS</span></span>

[<span data-ttu-id="f9ea4-123">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="f9ea4-123">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


