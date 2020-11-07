---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 19f8215f8feaa1765da871f0fa38cc0120d842ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916751"
---
# <span data-ttu-id="0c8ff-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="0c8ff-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="0c8ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c8ff-102">SYNOPSIS</span></span>
<span data-ttu-id="0c8ff-103">WAF ilkesi oluşturma için CustomRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c8ff-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="0c8ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c8ff-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c8ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c8ff-105">DESCRIPTION</span></span>
<span data-ttu-id="0c8ff-106">WAF ilkesi oluşturma için CustomRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c8ff-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="0c8ff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c8ff-107">EXAMPLES</span></span>

### <span data-ttu-id="0c8ff-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c8ff-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="0c8ff-109">CustomRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c8ff-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="0c8ff-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c8ff-110">PARAMETERS</span></span>

### <span data-ttu-id="0c8ff-111">-Eylem</span><span class="sxs-lookup"><span data-stu-id="0c8ff-111">-Action</span></span>
<span data-ttu-id="0c8ff-112">Eylem türü.</span><span class="sxs-lookup"><span data-stu-id="0c8ff-112">Type of Actions.</span></span>
<span data-ttu-id="0c8ff-113">Olası değerler: ' Izin ver ', ' engelle ', ' günlük '</span><span class="sxs-lookup"><span data-stu-id="0c8ff-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c8ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c8ff-114">-DefaultProfile</span></span>
<span data-ttu-id="0c8ff-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c8ff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c8ff-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="0c8ff-116">-MatchCondition</span></span>
<span data-ttu-id="0c8ff-117">Eşleşme koşulları listesi.</span><span class="sxs-lookup"><span data-stu-id="0c8ff-117">List of match conditions.</span></span>

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

### <span data-ttu-id="0c8ff-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c8ff-118">-Name</span></span>
<span data-ttu-id="0c8ff-119">Kuralın adı</span><span class="sxs-lookup"><span data-stu-id="0c8ff-119">Name of the rule</span></span>

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

### <span data-ttu-id="0c8ff-120">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="0c8ff-120">-Priority</span></span>
<span data-ttu-id="0c8ff-121">Kuralın önceliğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="0c8ff-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="0c8ff-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="0c8ff-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="0c8ff-123">Hız limiti süresi.</span><span class="sxs-lookup"><span data-stu-id="0c8ff-123">Rate limit duration.</span></span> <span data-ttu-id="0c8ff-124">Varsayılan-1 dakika</span><span class="sxs-lookup"><span data-stu-id="0c8ff-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="0c8ff-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="0c8ff-125">-RateLimitThreshold</span></span>
<span data-ttu-id="0c8ff-126">Derecelendirme hızı</span><span class="sxs-lookup"><span data-stu-id="0c8ff-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="0c8ff-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="0c8ff-127">-RuleType</span></span>
<span data-ttu-id="0c8ff-128">Kuralın türü.</span><span class="sxs-lookup"><span data-stu-id="0c8ff-128">Type of the rule.</span></span>
<span data-ttu-id="0c8ff-129">Olası değerler: ' MatchRule ', ' RateLimitRule '</span><span class="sxs-lookup"><span data-stu-id="0c8ff-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="0c8ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c8ff-130">CommonParameters</span></span>
<span data-ttu-id="0c8ff-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c8ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c8ff-132">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0c8ff-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c8ff-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c8ff-133">INPUTS</span></span>

### <span data-ttu-id="0c8ff-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0c8ff-134">None</span></span>

## <span data-ttu-id="0c8ff-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c8ff-135">OUTPUTS</span></span>

### <span data-ttu-id="0c8ff-136">Microsoft. Azure. Commands. Frontkapısı. modeller. Psccustomrule</span><span class="sxs-lookup"><span data-stu-id="0c8ff-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="0c8ff-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c8ff-137">NOTES</span></span>

## <span data-ttu-id="0c8ff-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c8ff-138">RELATED LINKS</span></span>

<span data-ttu-id="0c8ff-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="0c8ff-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span></span>
