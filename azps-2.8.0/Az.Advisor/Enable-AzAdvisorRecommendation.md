---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 05d74b254645a970389aae859d60583c53c07670
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753693"
---
# <span data-ttu-id="599d1-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="599d1-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="599d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="599d1-102">SYNOPSIS</span></span>
<span data-ttu-id="599d1-103">Azure Advisor tavsiyeleri etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="599d1-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="599d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="599d1-104">SYNTAX</span></span>

### <span data-ttu-id="599d1-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="599d1-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="599d1-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="599d1-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="599d1-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="599d1-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="599d1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="599d1-108">DESCRIPTION</span></span>
<span data-ttu-id="599d1-109">Bu cmdlet önceden gizlenmiş bir öneriyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="599d1-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="599d1-110">Öneri ile ilişkili tüm bastırmaları da kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="599d1-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="599d1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="599d1-111">EXAMPLES</span></span>

### <span data-ttu-id="599d1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="599d1-112">Example 1</span></span>
```powershell
PS C:\> Enable-AzAdvisorRecommendation -ResourceId c3621337-f131-4bf4-92f2-3fb9c8cfa0d8 

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="599d1-113">"Recommendation_id" adlı öneri için tüm bastırmaları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="599d1-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="599d1-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="599d1-114">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" 
| Enable-AzAdvisorRecommendation

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/{recommendation_id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : {recommendation_id}
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="599d1-115">Ardışık düzene geçilen belirli tavsiyeleriyle ilgili tüm bastırmaları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="599d1-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="599d1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="599d1-116">PARAMETERS</span></span>

### <span data-ttu-id="599d1-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="599d1-117">-Confirm</span></span>
<span data-ttu-id="599d1-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="599d1-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599d1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="599d1-119">-DefaultProfile</span></span>
<span data-ttu-id="599d1-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="599d1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="599d1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="599d1-121">-InputObject</span></span>
<span data-ttu-id="599d1-122">Get-AzAdvisorRecommendation çağrısı tarafından döndürülen Psazureadvisorresourcereyorumdationbase PowerShell nesnesi.</span><span class="sxs-lookup"><span data-stu-id="599d1-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

```yaml
Type: PsAzureAdvisorResourceRecommendationBase
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="599d1-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="599d1-123">-RecommendationName</span></span>
<span data-ttu-id="599d1-124">Önerin ResourceName.</span><span class="sxs-lookup"><span data-stu-id="599d1-124">ResourceName of the recommendation.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599d1-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="599d1-125">-ResourceId</span></span>
<span data-ttu-id="599d1-126">Bastırılacak öneri kimliği.</span><span class="sxs-lookup"><span data-stu-id="599d1-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="599d1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="599d1-127">-WhatIf</span></span>
<span data-ttu-id="599d1-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="599d1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="599d1-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="599d1-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599d1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="599d1-130">CommonParameters</span></span>
<span data-ttu-id="599d1-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="599d1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="599d1-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="599d1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="599d1-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="599d1-133">INPUTS</span></span>

### <span data-ttu-id="599d1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="599d1-134">System.String</span></span>

### <span data-ttu-id="599d1-135">Microsoft. Azure. Commands. Advisor. cmdlet. modeller. Psazureadvisorresourcereyorumdationbase</span><span class="sxs-lookup"><span data-stu-id="599d1-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="599d1-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="599d1-136">OUTPUTS</span></span>

### <span data-ttu-id="599d1-137">Microsoft. Azure. Commands. Advisor. cmdlet. modeller. Psazureadvisorresourcereyorumdationbase</span><span class="sxs-lookup"><span data-stu-id="599d1-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="599d1-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="599d1-138">NOTES</span></span>

## <span data-ttu-id="599d1-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="599d1-139">RELATED LINKS</span></span>