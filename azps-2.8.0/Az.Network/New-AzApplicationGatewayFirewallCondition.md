---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: aec627fdc8889d6bcfc4fb8e7762eb3be7bf0432
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918367"
---
# <span data-ttu-id="f46f8-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="f46f8-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="f46f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f46f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f46f8-103">Özel kural için eşleştirme koşulu oluşturur</span><span class="sxs-lookup"><span data-stu-id="f46f8-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="f46f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f46f8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f46f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f46f8-105">DESCRIPTION</span></span>
<span data-ttu-id="f46f8-106">**Yeni-AzApplicationGatewayFirewallCondition** , güvenlik duvarı özel kuralı için eşleştirme koşulunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f46f8-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="f46f8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f46f8-107">EXAMPLES</span></span>

### <span data-ttu-id="f46f8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f46f8-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallConditon -MatchVariables $variable -Operator Contains -NegationConditon false -Transforms Lowercase, Trim -MatchValues abc, cde
```

<span data-ttu-id="f46f8-109">Komut, $variable tanımlanan Match değişkenini kullanarak yeni bir Match koşulu oluşturur, işleç Içerir ve Olumsuzlaştırma koşulu yanlış, aktarım</span><span class="sxs-lookup"><span data-stu-id="f46f8-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="f46f8-110">Yeni eşleşme koşulu $condition kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="f46f8-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="f46f8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f46f8-111">PARAMETERS</span></span>

### <span data-ttu-id="f46f8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46f8-112">-DefaultProfile</span></span>
<span data-ttu-id="f46f8-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f46f8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f46f8-114">-Eşleşme değeri</span><span class="sxs-lookup"><span data-stu-id="f46f8-114">-MatchValue</span></span>
<span data-ttu-id="f46f8-115">Değeri Eşleştir.</span><span class="sxs-lookup"><span data-stu-id="f46f8-115">Match value.</span></span>

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

### <span data-ttu-id="f46f8-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="f46f8-116">-MatchVariable</span></span>
<span data-ttu-id="f46f8-117">Eşleşme değişkenleri listesi.</span><span class="sxs-lookup"><span data-stu-id="f46f8-117">List of match variables.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46f8-118">-Yoksayıdurumu</span><span class="sxs-lookup"><span data-stu-id="f46f8-118">-NegationCondition</span></span>
<span data-ttu-id="f46f8-119">Bunun Negate koşulu olup olmadığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="f46f8-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="f46f8-120">-İşleç</span><span class="sxs-lookup"><span data-stu-id="f46f8-120">-Operator</span></span>
<span data-ttu-id="f46f8-121">Eşleştirilecek işleç açıklanır.</span><span class="sxs-lookup"><span data-stu-id="f46f8-121">Describes operator to be matched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith, Regex

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46f8-122">-Dönüştürme</span><span class="sxs-lookup"><span data-stu-id="f46f8-122">-Transform</span></span>
<span data-ttu-id="f46f8-123">Dönüşüm listesi.</span><span class="sxs-lookup"><span data-stu-id="f46f8-123">List of transforms.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Trim, UrlDecode, UrlEncode, RemoveNulls, HtmlEntityDecode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46f8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46f8-124">CommonParameters</span></span>
<span data-ttu-id="f46f8-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f46f8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46f8-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f46f8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46f8-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f46f8-127">INPUTS</span></span>

### <span data-ttu-id="f46f8-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f46f8-128">None</span></span>

## <span data-ttu-id="f46f8-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f46f8-129">OUTPUTS</span></span>

### <span data-ttu-id="f46f8-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="f46f8-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="f46f8-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f46f8-131">NOTES</span></span>

## <span data-ttu-id="f46f8-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f46f8-132">RELATED LINKS</span></span>
