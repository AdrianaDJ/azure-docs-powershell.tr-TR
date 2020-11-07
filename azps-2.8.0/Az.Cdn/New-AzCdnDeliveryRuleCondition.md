---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 830b561a3d46e23f083d77dcac627b28f7dbb94e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753060"
---
# <span data-ttu-id="b7310-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="b7310-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="b7310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7310-102">SYNOPSIS</span></span>
<span data-ttu-id="b7310-103">Teslim kuralı koşulu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b7310-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="b7310-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7310-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> -MatchValue <String[]>
 [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7310-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7310-105">DESCRIPTION</span></span>
<span data-ttu-id="b7310-106">**New-AzCdnDeliveryRule** CMDLET 'i CDN uç noktası oluşturma için bir teslim kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b7310-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="b7310-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7310-107">EXAMPLES</span></span>

### <span data-ttu-id="b7310-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b7310-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="b7310-109">Basit bir koşul oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b7310-109">Create a simple condition.</span></span>

## <span data-ttu-id="b7310-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7310-110">PARAMETERS</span></span>

### <span data-ttu-id="b7310-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7310-111">-DefaultProfile</span></span>
<span data-ttu-id="b7310-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7310-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7310-113">-Eşleşme değeri</span><span class="sxs-lookup"><span data-stu-id="b7310-113">-MatchValue</span></span>
<span data-ttu-id="b7310-114">Olası eşleşme değerleri listesi.</span><span class="sxs-lookup"><span data-stu-id="b7310-114">List of possible match values.</span></span>

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

### <span data-ttu-id="b7310-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="b7310-115">-MatchVariable</span></span>
<span data-ttu-id="b7310-116">Koşulun değişkenini eşleştirin.</span><span class="sxs-lookup"><span data-stu-id="b7310-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="b7310-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="b7310-117">-NegateCondition</span></span>
<span data-ttu-id="b7310-118">Bu koşulun sonucunun ne olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7310-118">Describes if the result of this condition should be negated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7310-119">-İşleç</span><span class="sxs-lookup"><span data-stu-id="b7310-119">-Operator</span></span>
<span data-ttu-id="b7310-120">Eşleştirilecek işletmeni açıklar</span><span class="sxs-lookup"><span data-stu-id="b7310-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="b7310-121">-Dönüştürme</span><span class="sxs-lookup"><span data-stu-id="b7310-121">-Transform</span></span>
<span data-ttu-id="b7310-122">Eşleştirme öncesinde uygulanacak dönüştürme.</span><span class="sxs-lookup"><span data-stu-id="b7310-122">Transform to apply before matching.</span></span>
<span data-ttu-id="b7310-123">Olası değerler küçük ve büyük harf</span><span class="sxs-lookup"><span data-stu-id="b7310-123">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="b7310-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7310-124">CommonParameters</span></span>
<span data-ttu-id="b7310-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7310-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7310-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b7310-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7310-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7310-127">INPUTS</span></span>

### <span data-ttu-id="b7310-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b7310-128">None</span></span>

## <span data-ttu-id="b7310-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7310-129">OUTPUTS</span></span>

### <span data-ttu-id="b7310-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="b7310-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="b7310-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7310-131">NOTES</span></span>

## <span data-ttu-id="b7310-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7310-132">RELATED LINKS</span></span>
