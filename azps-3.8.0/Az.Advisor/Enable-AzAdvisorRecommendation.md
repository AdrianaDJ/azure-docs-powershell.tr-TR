---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097466"
---
# <span data-ttu-id="a6dc8-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="a6dc8-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="a6dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="a6dc8-103">Azure Advisor tavsiyeleri etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="a6dc8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6dc8-104">SYNTAX</span></span>

### <span data-ttu-id="a6dc8-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a6dc8-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6dc8-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="a6dc8-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6dc8-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="a6dc8-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6dc8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6dc8-108">DESCRIPTION</span></span>
<span data-ttu-id="a6dc8-109">Bu cmdlet önceden gizlenmiş bir öneriyi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="a6dc8-110">Öneri ile ilişkili tüm bastırmaları da kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="a6dc8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6dc8-111">EXAMPLES</span></span>

### <span data-ttu-id="a6dc8-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a6dc8-112">Example 1</span></span>
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

<span data-ttu-id="a6dc8-113">"Recommendation_id" adlı öneri için tüm bastırmaları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="a6dc8-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a6dc8-114">Example 2</span></span>
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

<span data-ttu-id="a6dc8-115">Ardışık düzene geçilen belirli tavsiyeleriyle ilgili tüm bastırmaları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="a6dc8-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6dc8-116">PARAMETERS</span></span>

### <span data-ttu-id="a6dc8-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6dc8-117">-Confirm</span></span>
<span data-ttu-id="a6dc8-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6dc8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6dc8-119">-DefaultProfile</span></span>
<span data-ttu-id="a6dc8-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6dc8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6dc8-121">-InputObject</span></span>
<span data-ttu-id="a6dc8-122">Get-AzAdvisorRecommendation çağrısı tarafından döndürülen Psazureadvisorresourcereyorumdationbase PowerShell nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="a6dc8-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="a6dc8-123">-RecommendationName</span></span>
<span data-ttu-id="a6dc8-124">Önerin ResourceName.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-124">ResourceName of the recommendation.</span></span>

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

### <span data-ttu-id="a6dc8-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a6dc8-125">-ResourceId</span></span>
<span data-ttu-id="a6dc8-126">Bastırılacak öneri kimliği.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="a6dc8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6dc8-127">-WhatIf</span></span>
<span data-ttu-id="a6dc8-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6dc8-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6dc8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6dc8-130">CommonParameters</span></span>
<span data-ttu-id="a6dc8-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6dc8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a6dc8-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6dc8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6dc8-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6dc8-133">INPUTS</span></span>

### <span data-ttu-id="a6dc8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a6dc8-134">System.String</span></span>

### <span data-ttu-id="a6dc8-135">Microsoft. Azure. Commands. Advisor. cmdlet. modeller. Psazureadvisorresourcereyorumdationbase</span><span class="sxs-lookup"><span data-stu-id="a6dc8-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="a6dc8-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6dc8-136">OUTPUTS</span></span>

### <span data-ttu-id="a6dc8-137">Microsoft. Azure. Commands. Advisor. cmdlet. modeller. Psazureadvisorresourcereyorumdationbase</span><span class="sxs-lookup"><span data-stu-id="a6dc8-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="a6dc8-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6dc8-138">NOTES</span></span>

## <span data-ttu-id="a6dc8-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6dc8-139">RELATED LINKS</span></span>
