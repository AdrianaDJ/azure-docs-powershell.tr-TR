---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 894fc2b3f3e722c7924e05e6c700ae03f741562f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751237"
---
# <span data-ttu-id="3b968-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="3b968-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="3b968-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b968-102">SYNOPSIS</span></span>
<span data-ttu-id="3b968-103">Azure Danışmanı önerilerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="3b968-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="3b968-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b968-104">SYNTAX</span></span>

### <span data-ttu-id="3b968-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3b968-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b968-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="3b968-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b968-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b968-107">DESCRIPTION</span></span>
<span data-ttu-id="3b968-108">Azure Danışmanı önerileri listesini alır.</span><span class="sxs-lookup"><span data-stu-id="3b968-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="3b968-109">Kategoriye, kaynak koduna, ada göre filtrelenebilir.</span><span class="sxs-lookup"><span data-stu-id="3b968-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="3b968-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b968-110">EXAMPLES</span></span>

### <span data-ttu-id="3b968-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3b968-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="3b968-112">Tüm önerilerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="3b968-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="3b968-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3b968-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -Category Performance
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="3b968-114">Kategori performansına göre filtrelenmiş tüm önerilerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="3b968-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="3b968-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b968-115">PARAMETERS</span></span>

### <span data-ttu-id="3b968-116">-Kategori</span><span class="sxs-lookup"><span data-stu-id="3b968-116">-Category</span></span>
<span data-ttu-id="3b968-117">Öneri kategorisi</span><span class="sxs-lookup"><span data-stu-id="3b968-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b968-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b968-118">-DefaultProfile</span></span>
<span data-ttu-id="3b968-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b968-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b968-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b968-120">-ResourceGroupName</span></span>
<span data-ttu-id="3b968-121">Öneri kaynak adı</span><span class="sxs-lookup"><span data-stu-id="3b968-121">ResourceGroup name of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b968-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3b968-122">-ResourceId</span></span>
<span data-ttu-id="3b968-123">Öneri için RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3b968-123">ResourceId of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b968-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b968-124">CommonParameters</span></span>
<span data-ttu-id="3b968-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b968-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3b968-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b968-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b968-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b968-127">INPUTS</span></span>

### <span data-ttu-id="3b968-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3b968-128">System.String</span></span>

## <span data-ttu-id="3b968-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b968-129">OUTPUTS</span></span>

### <span data-ttu-id="3b968-130">Microsoft. Azure. Commands. Advisor. cmdlet. modeller. Psazureadvisorresourcereyorumdationbase</span><span class="sxs-lookup"><span data-stu-id="3b968-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="3b968-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b968-131">NOTES</span></span>

## <span data-ttu-id="3b968-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b968-132">RELATED LINKS</span></span>
