---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: 06e161ef2e1a2b6470144453bd9fe77ade13f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751241"
---
# <span data-ttu-id="1ce45-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="1ce45-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="1ce45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ce45-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce45-103">Azure Danışmanı önerisini devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="1ce45-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="1ce45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ce45-104">SYNTAX</span></span>

### <span data-ttu-id="1ce45-105">Idparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1ce45-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ce45-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ce45-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ce45-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="1ce45-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ce45-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ce45-108">DESCRIPTION</span></span>
<span data-ttu-id="1ce45-109">Öneri için bir gizleme oluşturur; Bu, belirli bir önerisinin belirli bir süre veya sonsuz ertelenmesi sağlanır.</span><span class="sxs-lookup"><span data-stu-id="1ce45-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="1ce45-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ce45-110">EXAMPLES</span></span>

### <span data-ttu-id="1ce45-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1ce45-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="1ce45-112">Varsayılan-SuppressionName ve varsayılan günler-1 olarak verilen öneri adı için bir gizleme oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1ce45-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="1ce45-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1ce45-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="1ce45-114">Verilen öneri kimliği için bir gizleme oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1ce45-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="1ce45-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1ce45-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzAdvisorRecommendation -ResourceId "/subscriptions/user_subscription/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" | Disable-A
zAdvisorRecommendation

SuppressionId : daf24e78-af2d-e8d3-9c50-fa970edc2937
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="1ce45-116">Gizleme oluşturma, Get-AzAdvisorRecommendation 'den devre dışı bırak-Azdanışmanlar ve öneri.</span><span class="sxs-lookup"><span data-stu-id="1ce45-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="1ce45-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ce45-117">PARAMETERS</span></span>

### <span data-ttu-id="1ce45-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="1ce45-118">-Confirm</span></span>
<span data-ttu-id="1ce45-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1ce45-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ce45-120">-Gün</span><span class="sxs-lookup"><span data-stu-id="1ce45-120">-Days</span></span>
<span data-ttu-id="1ce45-121">İzinli günler.</span><span class="sxs-lookup"><span data-stu-id="1ce45-121">Days to disable.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce45-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce45-122">-DefaultProfile</span></span>
<span data-ttu-id="1ce45-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ce45-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ce45-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ce45-124">-InputObject</span></span>
<span data-ttu-id="1ce45-125">Get-AzAdvisorRecommendation çağrısı tarafından döndürülen Psazureadvisorresourcereyorumdationbase PowerShell nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1ce45-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="1ce45-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="1ce45-126">-RecommendationName</span></span>
<span data-ttu-id="1ce45-127">Önerin ResourceName</span><span class="sxs-lookup"><span data-stu-id="1ce45-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="1ce45-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1ce45-128">-ResourceId</span></span>
<span data-ttu-id="1ce45-129">Bastırılacak öneri kimliği.</span><span class="sxs-lookup"><span data-stu-id="1ce45-129">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce45-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ce45-130">-WhatIf</span></span>
<span data-ttu-id="1ce45-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ce45-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ce45-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1ce45-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ce45-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce45-133">CommonParameters</span></span>
<span data-ttu-id="1ce45-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ce45-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1ce45-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ce45-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce45-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ce45-136">INPUTS</span></span>

### <span data-ttu-id="1ce45-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1ce45-137">System.String</span></span>

### <span data-ttu-id="1ce45-138">Microsoft. Azure. Commands. Advisor. cmdlet. modeller. Psazureadvisorresourcereyorumdationbase</span><span class="sxs-lookup"><span data-stu-id="1ce45-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="1ce45-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ce45-139">OUTPUTS</span></span>

### <span data-ttu-id="1ce45-140">Microsoft. Azure. Commands. Advisor. cmdlet. modeller. PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="1ce45-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="1ce45-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ce45-141">NOTES</span></span>

## <span data-ttu-id="1ce45-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ce45-142">RELATED LINKS</span></span>
