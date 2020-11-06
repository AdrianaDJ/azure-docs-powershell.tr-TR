---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightslinktargets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: 64e74b2c9d4aa5f22d48bb6cb80c5a1952424c38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588851"
---
# <span data-ttu-id="aae05-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="aae05-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="aae05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aae05-102">SYNOPSIS</span></span>
<span data-ttu-id="aae05-103">Abonelikle ilişkilendirilmemiş hesapları alır.</span><span class="sxs-lookup"><span data-stu-id="aae05-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aae05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aae05-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aae05-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aae05-105">DESCRIPTION</span></span>
<span data-ttu-id="aae05-106">**Get-Azurermoperationalınsightslinktargets** cmdlet 'ı bir Azure aboneliğiyle ilişkilendirilmemiş mevcut hesapları listeler.</span><span class="sxs-lookup"><span data-stu-id="aae05-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="aae05-107">Yeni bir çalışma alanını varolan bir hesaba bağlamak için, yeni bir çalışma alanının müşteri KIMLIĞI özelliğinde bu işlem tarafından döndürülen bir müşteri KIMLIĞI kullanın.</span><span class="sxs-lookup"><span data-stu-id="aae05-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="aae05-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aae05-108">EXAMPLES</span></span>

### <span data-ttu-id="aae05-109">Örnek 1: bağlantısız hesapları alma</span><span class="sxs-lookup"><span data-stu-id="aae05-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="aae05-110">Bu komut arayan KIMLIĞININ sahibi olduğu bağlantısız hesapları alır.</span><span class="sxs-lookup"><span data-stu-id="aae05-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="aae05-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aae05-111">PARAMETERS</span></span>

### <span data-ttu-id="aae05-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae05-112">-DefaultProfile</span></span>
<span data-ttu-id="aae05-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="aae05-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aae05-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae05-114">CommonParameters</span></span>
<span data-ttu-id="aae05-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aae05-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae05-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae05-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae05-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aae05-117">INPUTS</span></span>

### <span data-ttu-id="aae05-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="aae05-118">None</span></span>
<span data-ttu-id="aae05-119">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="aae05-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aae05-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aae05-120">OUTPUTS</span></span>

### <span data-ttu-id="aae05-121">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Operationalınsights. model. PSAccount]</span><span class="sxs-lookup"><span data-stu-id="aae05-121">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount]</span></span>

## <span data-ttu-id="aae05-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aae05-122">NOTES</span></span>

## <span data-ttu-id="aae05-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aae05-123">RELATED LINKS</span></span>

[<span data-ttu-id="aae05-124">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="aae05-124">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


