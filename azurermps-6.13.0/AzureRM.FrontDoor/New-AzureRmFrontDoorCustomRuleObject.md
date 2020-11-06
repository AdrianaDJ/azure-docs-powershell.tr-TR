---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
ms.openlocfilehash: a5a1494bd217147a4e6f4c94a85140313429898f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572761"
---
# <span data-ttu-id="bb817-101">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="bb817-101">New-AzureRmFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="bb817-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb817-102">SYNOPSIS</span></span>
<span data-ttu-id="bb817-103">WAF ilkesi oluşturma için CustomRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bb817-103">Create CustomRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb817-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb817-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb817-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb817-105">DESCRIPTION</span></span>
<span data-ttu-id="bb817-106">WAF ilkesi oluşturma için CustomRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bb817-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="bb817-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb817-107">EXAMPLES</span></span>

### <span data-ttu-id="bb817-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bb817-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

RuleType                   : MatchRule
Action                     : Block
MatchConditions            : {Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition}
Priority                   : 2
RateLimitDurationInMinutes : 1
RateLimitThreshold         :
Name                       : Rule1
Etag                       :
Transforms                 :
```

<span data-ttu-id="bb817-109">CustomRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bb817-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="bb817-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb817-110">PARAMETERS</span></span>

### <span data-ttu-id="bb817-111">-Eylem</span><span class="sxs-lookup"><span data-stu-id="bb817-111">-Action</span></span>
<span data-ttu-id="bb817-112">Eylem türü.</span><span class="sxs-lookup"><span data-stu-id="bb817-112">Type of Actions.</span></span>
<span data-ttu-id="bb817-113">Olası değerler: ' Izin ver ', ' engelle ', ' günlük '</span><span class="sxs-lookup"><span data-stu-id="bb817-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb817-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb817-114">-DefaultProfile</span></span>
<span data-ttu-id="bb817-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb817-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb817-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="bb817-116">-MatchCondition</span></span>
<span data-ttu-id="bb817-117">Eşleşme koşulları listesi.</span><span class="sxs-lookup"><span data-stu-id="bb817-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb817-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb817-118">-Name</span></span>
<span data-ttu-id="bb817-119">Kuralın adı</span><span class="sxs-lookup"><span data-stu-id="bb817-119">Name of the rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb817-120">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="bb817-120">-Priority</span></span>
<span data-ttu-id="bb817-121">Kuralın önceliğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="bb817-121">Describes priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb817-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="bb817-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="bb817-123">Hız limiti süresi.</span><span class="sxs-lookup"><span data-stu-id="bb817-123">Rate limit duration.</span></span> <span data-ttu-id="bb817-124">Varsayılan-1 dakika</span><span class="sxs-lookup"><span data-stu-id="bb817-124">Default - 1 minute</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb817-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="bb817-125">-RateLimitThreshold</span></span>
<span data-ttu-id="bb817-126">Derecelendirme hızı</span><span class="sxs-lookup"><span data-stu-id="bb817-126">Rate limit thresold</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb817-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="bb817-127">-RuleType</span></span>
<span data-ttu-id="bb817-128">Kuralın türü.</span><span class="sxs-lookup"><span data-stu-id="bb817-128">Type of the rule.</span></span>
<span data-ttu-id="bb817-129">Olası değerler: ' MatchRule ', ' RateLimitRule '</span><span class="sxs-lookup"><span data-stu-id="bb817-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRuleType
Parameter Sets: (All)
Aliases:
Accepted values: RateLimitRule, MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb817-130">-Dönüştürme</span><span class="sxs-lookup"><span data-stu-id="bb817-130">-Transform</span></span>
<span data-ttu-id="bb817-131">Dönüşümlerin listesi</span><span class="sxs-lookup"><span data-stu-id="bb817-131">List of transforms</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb817-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb817-132">CommonParameters</span></span>
<span data-ttu-id="bb817-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb817-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb817-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb817-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb817-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb817-135">INPUTS</span></span>

### <span data-ttu-id="bb817-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bb817-136">None</span></span>

## <span data-ttu-id="bb817-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb817-137">OUTPUTS</span></span>

### <span data-ttu-id="bb817-138">Microsoft. Azure. Commands. Frontkapısı. modeller. Psccustomrule</span><span class="sxs-lookup"><span data-stu-id="bb817-138">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="bb817-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb817-139">NOTES</span></span>

## <span data-ttu-id="bb817-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb817-140">RELATED LINKS</span></span>

<span data-ttu-id="bb817-141">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="bb817-141">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span></span>
