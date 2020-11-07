---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
ms.openlocfilehash: 70ab8b592c550280f424f9c0a4bfced877942edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762929"
---
# <span data-ttu-id="b4474-101">New-AzureRmFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="b4474-101">New-AzureRmFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="b4474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4474-102">SYNOPSIS</span></span>
<span data-ttu-id="b4474-103">WAF ilkesi oluşturma için MatchCondition nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4474-103">Create MatchCondition Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4474-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4474-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable>
 -OperatorProperty <PSOperatorProperty> -MatchValue <String[]> [-Selector <String>]
 [-NegateCondition <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4474-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4474-105">DESCRIPTION</span></span>
<span data-ttu-id="b4474-106">WAF ilkesi oluşturma için MatchCondition nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4474-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="b4474-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4474-107">EXAMPLES</span></span>

### <span data-ttu-id="b4474-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4474-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "UserAgent" -MatchValue "Windows"


MatchVariable    : RequestHeader
OperatorProperty : Contains
MatchValue       : {Windows}
Selector         : UserAgent
NegateCondition  : False
```

<span data-ttu-id="b4474-109">MatchCondition nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4474-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="b4474-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4474-110">PARAMETERS</span></span>

### <span data-ttu-id="b4474-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4474-111">-DefaultProfile</span></span>
<span data-ttu-id="b4474-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4474-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4474-113">-Eşleşme değeri</span><span class="sxs-lookup"><span data-stu-id="b4474-113">-MatchValue</span></span>
<span data-ttu-id="b4474-114">Değeri Eşleştir.</span><span class="sxs-lookup"><span data-stu-id="b4474-114">Match value.</span></span>

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

### <span data-ttu-id="b4474-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="b4474-115">-MatchVariable</span></span>
<span data-ttu-id="b4474-116">Değişkeni eşle.</span><span class="sxs-lookup"><span data-stu-id="b4474-116">Match Variable.</span></span>
<span data-ttu-id="b4474-117">Olası değerler: ' RemoteAddr ', ' RequestMethod ', ' QueryString ', ' PostArgs ', ' RequestUri ', ' RequestHeader ', ' RequestBody '</span><span class="sxs-lookup"><span data-stu-id="b4474-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

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

### <span data-ttu-id="b4474-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="b4474-118">-NegateCondition</span></span>
<span data-ttu-id="b4474-119">Bunun Negate koşulu mı yoksa varsayılan değerin yanlış mu olduğunu açıklar</span><span class="sxs-lookup"><span data-stu-id="b4474-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="b4474-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="b4474-120">-OperatorProperty</span></span>
<span data-ttu-id="b4474-121">Eşleştirilecek işleç açıklanır.</span><span class="sxs-lookup"><span data-stu-id="b4474-121">Describes operator to be matched.</span></span>
<span data-ttu-id="b4474-122">Olası değerler şunlardır: ' any ', ' IPMatch ', ' GeoMatch ', ' eşittir ', ' Contains ', ' LessThan ', ' GreaterThan ', ' Lessibinal ', ' GreaterThanOrEqual ', ' BeginsWith ', ' EndsWith ' '</span><span class="sxs-lookup"><span data-stu-id="b4474-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

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

### <span data-ttu-id="b4474-123">-Seçici</span><span class="sxs-lookup"><span data-stu-id="b4474-123">-Selector</span></span>
<span data-ttu-id="b4474-124">RequestHeader veya RequestBody eşleşmesi için seçicinin adı</span><span class="sxs-lookup"><span data-stu-id="b4474-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="b4474-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4474-125">CommonParameters</span></span>
<span data-ttu-id="b4474-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4474-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4474-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4474-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4474-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4474-128">INPUTS</span></span>

### <span data-ttu-id="b4474-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b4474-129">None</span></span>

## <span data-ttu-id="b4474-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4474-130">OUTPUTS</span></span>

### <span data-ttu-id="b4474-131">Microsoft. Azure. Commands. Frontkapısı. modeller. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="b4474-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="b4474-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4474-132">NOTES</span></span>

## <span data-ttu-id="b4474-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4474-133">RELATED LINKS</span></span>

[<span data-ttu-id="b4474-134">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="b4474-134">New-AzureRmFrontDoorCustomRuleObject</span></span>](./New-AzureRmFrontDoorCustomRuleObject.md)
