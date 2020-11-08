---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277411"
---
# <span data-ttu-id="e09bd-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="e09bd-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="e09bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e09bd-102">SYNOPSIS</span></span>
<span data-ttu-id="e09bd-103">Kural altyapısı kuralı oluşturmak için PSRulesEngineMatchCondition nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e09bd-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="e09bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e09bd-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e09bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e09bd-105">DESCRIPTION</span></span>
<span data-ttu-id="e09bd-106">Kural altyapısı kuralı oluşturmak için PSRulesEngineMatchCondition nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e09bd-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="e09bd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e09bd-107">EXAMPLES</span></span>

### <span data-ttu-id="e09bd-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e09bd-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="e09bd-109">Yeni bir PSRulesEngineMatchCondition Greate.</span><span class="sxs-lookup"><span data-stu-id="e09bd-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="e09bd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e09bd-110">PARAMETERS</span></span>

### <span data-ttu-id="e09bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e09bd-111">-DefaultProfile</span></span>
<span data-ttu-id="e09bd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e09bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e09bd-113">-Eşleşme değeri</span><span class="sxs-lookup"><span data-stu-id="e09bd-113">-MatchValue</span></span>
<span data-ttu-id="e09bd-114">Eşlenecek değerleri eşleştirin.</span><span class="sxs-lookup"><span data-stu-id="e09bd-114">Match values to match against.</span></span>
<span data-ttu-id="e09bd-115">İşleç, buradaki veya semantiklerle her değere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e09bd-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="e09bd-116">Herhangi birinin verilen işleç ile değişkenle eşleşmesi durumunda, bu eşleşme koşulu eşleşme olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="e09bd-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e09bd-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="e09bd-117">-MatchVariable</span></span>
<span data-ttu-id="e09bd-118">Değişkeni eşle.</span><span class="sxs-lookup"><span data-stu-id="e09bd-118">Match Variable.</span></span>
<span data-ttu-id="e09bd-119">Olası değerler IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span><span class="sxs-lookup"><span data-stu-id="e09bd-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: IsMobile, RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestPath, RequestFilename, RequestFilenameExtension, RequestHeader, RequestBody, RequestScheme

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e09bd-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="e09bd-120">-NegateCondition</span></span>
<span data-ttu-id="e09bd-121">Bunun Negate koşulu olup olmadığını açıklar</span><span class="sxs-lookup"><span data-stu-id="e09bd-121">Describes if this is negate condition or not</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e09bd-122">-İşleç</span><span class="sxs-lookup"><span data-stu-id="e09bd-122">-Operator</span></span>
<span data-ttu-id="e09bd-123">Eşleştirme koşuluna uygulanacak işleç açıklanır.</span><span class="sxs-lookup"><span data-stu-id="e09bd-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="e09bd-124">Olası değerler, IPMatch, GeoMatch, eşittir, Contains, LessThan, GreaterThan, Lessıal, GreaterThanOrEqual, BeginsWith, EndsWith.</span><span class="sxs-lookup"><span data-stu-id="e09bd-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineOperator
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e09bd-125">-Seçici</span><span class="sxs-lookup"><span data-stu-id="e09bd-125">-Selector</span></span>
<span data-ttu-id="e09bd-126">RequestHeader veya RequestBody eşleşmesi için seçicinin adı</span><span class="sxs-lookup"><span data-stu-id="e09bd-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="e09bd-127">-Dönüştürme</span><span class="sxs-lookup"><span data-stu-id="e09bd-127">-Transform</span></span>
<span data-ttu-id="e09bd-128">Eşleştirme öncesinde hangi dönüşümlerin uygulandığını gösteren liste.</span><span class="sxs-lookup"><span data-stu-id="e09bd-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="e09bd-129">Olası tek tek dönüştürme değerleri küçük, büyük, Kırp, Urlçözemiyor, UrlEncode, RemoveNulls.</span><span class="sxs-lookup"><span data-stu-id="e09bd-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSTransform[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e09bd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e09bd-130">CommonParameters</span></span>
<span data-ttu-id="e09bd-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e09bd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e09bd-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e09bd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e09bd-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e09bd-133">INPUTS</span></span>

### <span data-ttu-id="e09bd-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e09bd-134">None</span></span>

## <span data-ttu-id="e09bd-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e09bd-135">OUTPUTS</span></span>

### <span data-ttu-id="e09bd-136">Microsoft. Azure. Commands. Frontkapısı. modeller. PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="e09bd-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="e09bd-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e09bd-137">NOTES</span></span>

## <span data-ttu-id="e09bd-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e09bd-138">RELATED LINKS</span></span>
