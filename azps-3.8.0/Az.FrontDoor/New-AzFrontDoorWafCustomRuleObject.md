---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: d352f70d28b9bfafae46697fb6d69dc50c739b19
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103838"
---
# <span data-ttu-id="02f6c-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="02f6c-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="02f6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="02f6c-103">WAF ilkesi oluşturma için CustomRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="02f6c-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="02f6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02f6c-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02f6c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="02f6c-105">DESCRIPTION</span></span>
<span data-ttu-id="02f6c-106">WAF ilkesi oluşturma için CustomRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="02f6c-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="02f6c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02f6c-107">EXAMPLES</span></span>

### <span data-ttu-id="02f6c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02f6c-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="02f6c-109">CustomRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="02f6c-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="02f6c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02f6c-110">PARAMETERS</span></span>

### <span data-ttu-id="02f6c-111">-Eylem</span><span class="sxs-lookup"><span data-stu-id="02f6c-111">-Action</span></span>
<span data-ttu-id="02f6c-112">Eylem türü.</span><span class="sxs-lookup"><span data-stu-id="02f6c-112">Type of Actions.</span></span>
<span data-ttu-id="02f6c-113">Olası değerler: ' Izin ver ', ' engelle ', ' günlük '</span><span class="sxs-lookup"><span data-stu-id="02f6c-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="02f6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f6c-114">-DefaultProfile</span></span>
<span data-ttu-id="02f6c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02f6c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02f6c-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="02f6c-116">-EnabledState</span></span>
<span data-ttu-id="02f6c-117">Etkin durum.</span><span class="sxs-lookup"><span data-stu-id="02f6c-117">Enabled State.</span></span> <span data-ttu-id="02f6c-118">Olası değerler: ' Enabled ', ' Disabled '.</span><span class="sxs-lookup"><span data-stu-id="02f6c-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f6c-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="02f6c-119">-MatchCondition</span></span>
<span data-ttu-id="02f6c-120">Eşleşme koşulları listesi.</span><span class="sxs-lookup"><span data-stu-id="02f6c-120">List of match conditions.</span></span>

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

### <span data-ttu-id="02f6c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="02f6c-121">-Name</span></span>
<span data-ttu-id="02f6c-122">Kuralın adı</span><span class="sxs-lookup"><span data-stu-id="02f6c-122">Name of the rule</span></span>

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

### <span data-ttu-id="02f6c-123">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="02f6c-123">-Priority</span></span>
<span data-ttu-id="02f6c-124">Kuralın önceliğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="02f6c-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="02f6c-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="02f6c-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="02f6c-126">Hız limiti süresi.</span><span class="sxs-lookup"><span data-stu-id="02f6c-126">Rate limit duration.</span></span> <span data-ttu-id="02f6c-127">Varsayılan-1 dakika</span><span class="sxs-lookup"><span data-stu-id="02f6c-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="02f6c-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="02f6c-128">-RateLimitThreshold</span></span>
<span data-ttu-id="02f6c-129">Hız limiti eşiği</span><span class="sxs-lookup"><span data-stu-id="02f6c-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="02f6c-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="02f6c-130">-RuleType</span></span>
<span data-ttu-id="02f6c-131">Kuralın türü.</span><span class="sxs-lookup"><span data-stu-id="02f6c-131">Type of the rule.</span></span>
<span data-ttu-id="02f6c-132">Olası değerler: ' MatchRule ', ' RateLimitRule '</span><span class="sxs-lookup"><span data-stu-id="02f6c-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="02f6c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f6c-133">CommonParameters</span></span>
<span data-ttu-id="02f6c-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02f6c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f6c-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02f6c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f6c-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02f6c-136">INPUTS</span></span>

### <span data-ttu-id="02f6c-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="02f6c-137">None</span></span>

## <span data-ttu-id="02f6c-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02f6c-138">OUTPUTS</span></span>

### <span data-ttu-id="02f6c-139">Microsoft. Azure. Commands. Frontkapısı. modeller. Psccustomrule</span><span class="sxs-lookup"><span data-stu-id="02f6c-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="02f6c-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02f6c-140">NOTES</span></span>

## <span data-ttu-id="02f6c-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02f6c-141">RELATED LINKS</span></span>

<span data-ttu-id="02f6c-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="02f6c-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span></span>
