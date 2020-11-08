---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277404"
---
# <span data-ttu-id="3dc2f-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="3dc2f-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="3dc2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dc2f-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc2f-103">WAF yönetilen kural kümeleri, gruplar veya kurallar için yönetilen kural dışlama nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3dc2f-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="3dc2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3dc2f-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dc2f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3dc2f-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc2f-106">WAF yönetilen kural kümeleri, gruplar veya kurallar için yönetilen kural dışlama nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3dc2f-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="3dc2f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3dc2f-107">EXAMPLES</span></span>

### <span data-ttu-id="3dc2f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3dc2f-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="3dc2f-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3dc2f-109">PARAMETERS</span></span>

### <span data-ttu-id="3dc2f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc2f-110">-DefaultProfile</span></span>
<span data-ttu-id="3dc2f-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3dc2f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dc2f-112">-İşleç</span><span class="sxs-lookup"><span data-stu-id="3dc2f-112">-Operator</span></span>
<span data-ttu-id="3dc2f-113">Seçiciyi eşleştirirken kullanılacak işleç, EqualsAny anlamına gelir (belirtilen türdeki tüm değişkenler eşleşmelidir)</span><span class="sxs-lookup"><span data-stu-id="3dc2f-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="3dc2f-114">-Seçici</span><span class="sxs-lookup"><span data-stu-id="3dc2f-114">-Selector</span></span>
<span data-ttu-id="3dc2f-115">İşleci kullanarak eşleşmesi için seçici deseni (işleç hiçbir Equaldeğilse)</span><span class="sxs-lookup"><span data-stu-id="3dc2f-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="3dc2f-116">Değişkenli</span><span class="sxs-lookup"><span data-stu-id="3dc2f-116">-Variable</span></span>
<span data-ttu-id="3dc2f-117">Değişkeni eşle.</span><span class="sxs-lookup"><span data-stu-id="3dc2f-117">Match variable.</span></span> <span data-ttu-id="3dc2f-118">Olası değerler, Istekadı, Requestargenames, QueryStringArgNames, RequestBodyPostArgNames değerleridir.</span><span class="sxs-lookup"><span data-stu-id="3dc2f-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="3dc2f-119">Örneğin, QueryStringArgNames adları, verilen operatörün seçiciyle eşleşen GET parametrelerinin dışlamasıdır.</span><span class="sxs-lookup"><span data-stu-id="3dc2f-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="3dc2f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc2f-120">CommonParameters</span></span>
<span data-ttu-id="3dc2f-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3dc2f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc2f-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3dc2f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc2f-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3dc2f-123">INPUTS</span></span>

### <span data-ttu-id="3dc2f-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3dc2f-124">None</span></span>

## <span data-ttu-id="3dc2f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3dc2f-125">OUTPUTS</span></span>

### <span data-ttu-id="3dc2f-126">Microsoft. Azure. Commands. Frontkapısı. modeller. Psmanagedruledışlaması</span><span class="sxs-lookup"><span data-stu-id="3dc2f-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="3dc2f-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3dc2f-127">NOTES</span></span>

## <span data-ttu-id="3dc2f-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3dc2f-128">RELATED LINKS</span></span>

<span data-ttu-id="3dc2f-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="3dc2f-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
