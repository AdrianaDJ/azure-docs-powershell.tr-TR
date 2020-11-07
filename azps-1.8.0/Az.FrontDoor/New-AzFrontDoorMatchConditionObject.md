---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
ms.openlocfilehash: ed711160bf761fe7b28f02a94d1ab4ffa6fdb59f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916716"
---
# <span data-ttu-id="9b120-101">New-AzFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="9b120-101">New-AzFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="9b120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b120-102">SYNOPSIS</span></span>
<span data-ttu-id="9b120-103">WAF ilkesi oluşturma için MatchCondition nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b120-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="9b120-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b120-104">SYNTAX</span></span>

```
New-AzFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable> -OperatorProperty <PSOperatorProperty>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b120-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b120-105">DESCRIPTION</span></span>
<span data-ttu-id="9b120-106">WAF ilkesi oluşturma için MatchCondition nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b120-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="9b120-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b120-107">EXAMPLES</span></span>

### <span data-ttu-id="9b120-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9b120-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition
------------- ---------------- ---------- --------   ---------------
RequestHeader         Contains {Windows}  User-Agent           False
```

<span data-ttu-id="9b120-109">MatchCondition nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b120-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="9b120-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b120-110">PARAMETERS</span></span>

### <span data-ttu-id="9b120-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b120-111">-DefaultProfile</span></span>
<span data-ttu-id="9b120-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b120-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b120-113">-Eşleşme değeri</span><span class="sxs-lookup"><span data-stu-id="9b120-113">-MatchValue</span></span>
<span data-ttu-id="9b120-114">Değeri Eşleştir.</span><span class="sxs-lookup"><span data-stu-id="9b120-114">Match value.</span></span>

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

### <span data-ttu-id="9b120-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="9b120-115">-MatchVariable</span></span>
<span data-ttu-id="9b120-116">Değişkeni eşle.</span><span class="sxs-lookup"><span data-stu-id="9b120-116">Match Variable.</span></span>
<span data-ttu-id="9b120-117">Olası değerler: ' RemoteAddr ', ' RequestMethod ', ' QueryString ', ' PostArgs ', ' RequestUri ', ' RequestHeader ', ' RequestBody '</span><span class="sxs-lookup"><span data-stu-id="9b120-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeader, RequestBody

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b120-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="9b120-118">-NegateCondition</span></span>
<span data-ttu-id="9b120-119">Bunun Negate koşulu mı yoksa varsayılan değerin yanlış mu olduğunu açıklar</span><span class="sxs-lookup"><span data-stu-id="9b120-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="9b120-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="9b120-120">-OperatorProperty</span></span>
<span data-ttu-id="9b120-121">Eşleştirilecek işleç açıklanır.</span><span class="sxs-lookup"><span data-stu-id="9b120-121">Describes operator to be matched.</span></span>
<span data-ttu-id="9b120-122">Olası değerler şunlardır: ' any ', ' IPMatch ', ' GeoMatch ', ' eşittir ', ' Contains ', ' LessThan ', ' GreaterThan ', ' Lessibinal ', ' GreaterThanOrEqual ', ' BeginsWith ', ' EndsWith ' '</span><span class="sxs-lookup"><span data-stu-id="9b120-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSOperatorProperty
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b120-123">-Seçici</span><span class="sxs-lookup"><span data-stu-id="9b120-123">-Selector</span></span>
<span data-ttu-id="9b120-124">RequestHeader veya RequestBody eşleşmesi için seçicinin adı</span><span class="sxs-lookup"><span data-stu-id="9b120-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="9b120-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b120-125">CommonParameters</span></span>
<span data-ttu-id="9b120-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b120-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b120-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9b120-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b120-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b120-128">INPUTS</span></span>

### <span data-ttu-id="9b120-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9b120-129">None</span></span>

## <span data-ttu-id="9b120-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b120-130">OUTPUTS</span></span>

### <span data-ttu-id="9b120-131">Microsoft. Azure. Commands. Frontkapısı. modeller. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="9b120-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="9b120-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b120-132">NOTES</span></span>

## <span data-ttu-id="9b120-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b120-133">RELATED LINKS</span></span>

[<span data-ttu-id="9b120-134">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="9b120-134">New-AzFrontDoorCustomRuleObject</span></span>](./New-AzFrontDoorCustomRuleObject.md)
