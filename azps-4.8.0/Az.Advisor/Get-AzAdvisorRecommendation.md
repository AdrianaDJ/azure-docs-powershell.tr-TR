---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 631e471af79ab5ac567afeafa8103e22ae885ed7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108035"
---
# <span data-ttu-id="55f18-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="55f18-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="55f18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55f18-102">SYNOPSIS</span></span>
<span data-ttu-id="55f18-103">Azure Danışmanı önerilerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="55f18-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="55f18-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55f18-104">SYNTAX</span></span>

### <span data-ttu-id="55f18-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55f18-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55f18-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="55f18-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55f18-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="55f18-107">DESCRIPTION</span></span>
<span data-ttu-id="55f18-108">Azure Danışmanı önerileri listesini alır.</span><span class="sxs-lookup"><span data-stu-id="55f18-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="55f18-109">Kategoriye, kaynak koduna, ada göre filtrelenebilir.</span><span class="sxs-lookup"><span data-stu-id="55f18-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="55f18-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55f18-110">EXAMPLES</span></span>

### <span data-ttu-id="55f18-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="55f18-111">Example 1</span></span>
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
<span data-ttu-id="55f18-112">Tüm önerilerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="55f18-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="55f18-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="55f18-113">Example 2</span></span>
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
<span data-ttu-id="55f18-114">Kategori performansına göre filtrelenmiş tüm önerilerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="55f18-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="55f18-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55f18-115">PARAMETERS</span></span>

### <span data-ttu-id="55f18-116">-Kategori</span><span class="sxs-lookup"><span data-stu-id="55f18-116">-Category</span></span>
<span data-ttu-id="55f18-117">Öneri kategorisi</span><span class="sxs-lookup"><span data-stu-id="55f18-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security, OperationalExcellence

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f18-118">-DefaultProfile</span></span>
<span data-ttu-id="55f18-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55f18-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55f18-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f18-120">-ResourceGroupName</span></span>
<span data-ttu-id="55f18-121">Öneri kaynak adı</span><span class="sxs-lookup"><span data-stu-id="55f18-121">ResourceGroup name of the recommendation</span></span>

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

### <span data-ttu-id="55f18-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="55f18-122">-ResourceId</span></span>
<span data-ttu-id="55f18-123">Öneri için RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="55f18-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="55f18-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f18-124">CommonParameters</span></span>
<span data-ttu-id="55f18-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55f18-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="55f18-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55f18-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f18-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55f18-127">INPUTS</span></span>

### <span data-ttu-id="55f18-128">System. String</span><span class="sxs-lookup"><span data-stu-id="55f18-128">System.String</span></span>

## <span data-ttu-id="55f18-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55f18-129">OUTPUTS</span></span>

### <span data-ttu-id="55f18-130">Microsoft. Azure. Commands. Advisor. cmdlet. modeller. Psazureadvisorresourcereyorumdationbase</span><span class="sxs-lookup"><span data-stu-id="55f18-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="55f18-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55f18-131">NOTES</span></span>

## <span data-ttu-id="55f18-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55f18-132">RELATED LINKS</span></span>
