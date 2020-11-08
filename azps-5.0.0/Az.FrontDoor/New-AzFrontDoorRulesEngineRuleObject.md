---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277410"
---
# <span data-ttu-id="2492d-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="2492d-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="2492d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2492d-102">SYNOPSIS</span></span>
<span data-ttu-id="2492d-103">Kural altyapısı oluşturmak için PSRulesEngineRule nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2492d-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="2492d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2492d-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2492d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2492d-105">DESCRIPTION</span></span>
<span data-ttu-id="2492d-106">Kural altyapısı oluşturmak için PSRulesEngineRule nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2492d-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="2492d-107">"-Action" parametresine geçilecek PSRulesEngineAction nesnesi oluşturmak için "New-AzFrontDoorRulesEngineActionObject" cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2492d-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="2492d-108">"-MatchCondition" parametresine geçilecek PSRulesEngineMatchCondition nesnesi oluşturmak için "New-AzFrontDoorRulesEngineMatchConditionObject" cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2492d-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="2492d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2492d-109">EXAMPLES</span></span>

### <span data-ttu-id="2492d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2492d-110">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority 0 -Action $rulesEngineAction -MatchProcessingBehavior Stop -MatchCondition $rulesEngineMatchCondition

Name                    : rules1
Priority                : 0
MatchProcessingBehavior : Stop
MatchCondition          : {Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition}
Action                  : Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction


PS C:\> $rulesEngineRule1.Action

RequestHeaderActions           ResponseHeaderActions RouteConfigurationOverride
--------------------           --------------------- --------------------------
{headeraction1, headeraction2} {}                    Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineRule1.MatchCondition[0]

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transforms               : {Lowercase, Uppercase}
```

<span data-ttu-id="2492d-111">Yeni PSRulesEngineRule nesnesi oluşturun ve alt alanların nasıl görüntüleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2492d-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="2492d-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2492d-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="2492d-113">Geçersiz öncelik değeri geçirilirken çıkış bekliyor.</span><span class="sxs-lookup"><span data-stu-id="2492d-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="2492d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2492d-114">PARAMETERS</span></span>

### <span data-ttu-id="2492d-115">-Eylem</span><span class="sxs-lookup"><span data-stu-id="2492d-115">-Action</span></span>
<span data-ttu-id="2492d-116">Tüm eşleşme koşulları sağlanıyorsa istek ve yanıtta gerçekleştirilecek eylemler.</span><span class="sxs-lookup"><span data-stu-id="2492d-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2492d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2492d-117">-DefaultProfile</span></span>
<span data-ttu-id="2492d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2492d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2492d-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="2492d-119">-MatchCondition</span></span>
<span data-ttu-id="2492d-120">Bu kuralın eylemlerinin çalışması için uyması gereken eşleşme koşullarının listesi.</span><span class="sxs-lookup"><span data-stu-id="2492d-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="2492d-121">Hiçbir eşleşme koşulu olmaması, eylemlerin her zaman çalışacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2492d-121">Having no match conditions means the actions will always run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2492d-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="2492d-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="2492d-123">Bu kural bir eşleşmedir, kural altyapısı kalan kuralları çalıştırmaya devam eder veya durur.</span><span class="sxs-lookup"><span data-stu-id="2492d-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="2492d-124">Olası değerler devam eder ve durdurulur.</span><span class="sxs-lookup"><span data-stu-id="2492d-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="2492d-125">Yoksa, varsayılan olarak devam eder.</span><span class="sxs-lookup"><span data-stu-id="2492d-125">If not present, defaults to Continue.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchProcessingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: Continue, Stop

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2492d-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="2492d-126">-Name</span></span>
<span data-ttu-id="2492d-127">Bu belirli kurala başvuruda bulunacak ad.</span><span class="sxs-lookup"><span data-stu-id="2492d-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="2492d-128">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="2492d-128">-Priority</span></span>
<span data-ttu-id="2492d-129">Bu kurala atanmış bir öncelik.</span><span class="sxs-lookup"><span data-stu-id="2492d-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="2492d-130">Negatif olamaz.</span><span class="sxs-lookup"><span data-stu-id="2492d-130">Cannot be negative.</span></span>

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

### <span data-ttu-id="2492d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2492d-131">CommonParameters</span></span>
<span data-ttu-id="2492d-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2492d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2492d-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2492d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2492d-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2492d-134">INPUTS</span></span>

### <span data-ttu-id="2492d-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2492d-135">None</span></span>

## <span data-ttu-id="2492d-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2492d-136">OUTPUTS</span></span>

### <span data-ttu-id="2492d-137">Microsoft. Azure. Commands. Frontkapısı. modeller. PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="2492d-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="2492d-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2492d-138">NOTES</span></span>

## <span data-ttu-id="2492d-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2492d-139">RELATED LINKS</span></span>
