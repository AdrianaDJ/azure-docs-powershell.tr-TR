---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: 0340cbf8c71b0ab117f1ff967ec7c3bb3e32b8f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275451"
---
# <span data-ttu-id="e5be3-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="e5be3-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="e5be3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5be3-102">SYNOPSIS</span></span>
<span data-ttu-id="e5be3-103">WAF ilkesi oluşturma için MatchCondition nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5be3-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="e5be3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5be3-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5be3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5be3-105">DESCRIPTION</span></span>
<span data-ttu-id="e5be3-106">WAF ilkesi oluşturma için MatchCondition nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5be3-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="e5be3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5be3-107">EXAMPLES</span></span>

### <span data-ttu-id="e5be3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e5be3-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="e5be3-109">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e5be3-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="e5be3-110">MatchCondition nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5be3-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="e5be3-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5be3-111">PARAMETERS</span></span>

### <span data-ttu-id="e5be3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5be3-112">-DefaultProfile</span></span>
<span data-ttu-id="e5be3-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5be3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5be3-114">-Eşleşme değeri</span><span class="sxs-lookup"><span data-stu-id="e5be3-114">-MatchValue</span></span>
<span data-ttu-id="e5be3-115">Değeri Eşleştir.</span><span class="sxs-lookup"><span data-stu-id="e5be3-115">Match value.</span></span>

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

### <span data-ttu-id="e5be3-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="e5be3-116">-MatchVariable</span></span>
<span data-ttu-id="e5be3-117">Değişkeni eşle.</span><span class="sxs-lookup"><span data-stu-id="e5be3-117">Match Variable.</span></span>
<span data-ttu-id="e5be3-118">Olası değerler: ' RemoteAddr ', ' RequestMethod ', ' QueryString ', ' PostArgs ', ' RequestUri ', ' RequestHeader ', ' RequestBody ', ' Socketadresi '</span><span class="sxs-lookup"><span data-stu-id="e5be3-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="e5be3-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="e5be3-119">-NegateCondition</span></span>
<span data-ttu-id="e5be3-120">Bunun Negate koşulu mı yoksa varsayılan değerin yanlış mu olduğunu açıklar</span><span class="sxs-lookup"><span data-stu-id="e5be3-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="e5be3-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="e5be3-121">-OperatorProperty</span></span>
<span data-ttu-id="e5be3-122">Eşleştirilecek işleç açıklanır.</span><span class="sxs-lookup"><span data-stu-id="e5be3-122">Describes operator to be matched.</span></span>
<span data-ttu-id="e5be3-123">Olası değerler şunlardır: ' any ', ' IPMatch ', ' GeoMatch ', ' eşittir ', ' Contains ', ' LessThan ', ' GreaterThan ', ' Lessibinal ', ' GreaterThanOrEqual ', ' BeginsWith ', ' EndsWith ', ' RegEx '</span><span class="sxs-lookup"><span data-stu-id="e5be3-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="e5be3-124">-Seçici</span><span class="sxs-lookup"><span data-stu-id="e5be3-124">-Selector</span></span>
<span data-ttu-id="e5be3-125">RequestHeader veya RequestBody eşleşmesi için seçicinin adı</span><span class="sxs-lookup"><span data-stu-id="e5be3-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="e5be3-126">-Dönüştürme</span><span class="sxs-lookup"><span data-stu-id="e5be3-126">-Transform</span></span>
<span data-ttu-id="e5be3-127">Uygulanacak dönüşümler.</span><span class="sxs-lookup"><span data-stu-id="e5be3-127">Transforms to apply.</span></span> <span data-ttu-id="e5be3-128">Olası değerler: ' küçük harfli ', ' büyük harfli ', ' Kırp ', ' Urlkodu ', ' UrlEncode ', ' RemoveNulls '.</span><span class="sxs-lookup"><span data-stu-id="e5be3-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="e5be3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5be3-129">CommonParameters</span></span>
<span data-ttu-id="e5be3-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5be3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5be3-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e5be3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5be3-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5be3-132">INPUTS</span></span>

### <span data-ttu-id="e5be3-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e5be3-133">None</span></span>

## <span data-ttu-id="e5be3-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5be3-134">OUTPUTS</span></span>

### <span data-ttu-id="e5be3-135">Microsoft. Azure. Commands. Frontkapısı. modeller. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="e5be3-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="e5be3-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5be3-136">NOTES</span></span>

## <span data-ttu-id="e5be3-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5be3-137">RELATED LINKS</span></span>

[<span data-ttu-id="e5be3-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="e5be3-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
