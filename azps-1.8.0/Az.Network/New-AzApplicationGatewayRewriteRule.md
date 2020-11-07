---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 9fdbf6f7cd88774c2d14d079201993f6a324ace5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760390"
---
# <span data-ttu-id="3ce86-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3ce86-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="3ce86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ce86-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce86-103">Uygulama ağ geçidi için yeniden yazma kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ce86-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="3ce86-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ce86-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ce86-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ce86-105">DESCRIPTION</span></span>
<span data-ttu-id="3ce86-106">**Yeni-AzApplicationGatewayRewriteRule** cmdlet 'ı bir Azure Application Gateway için yeniden yazma kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ce86-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="3ce86-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ce86-107">EXAMPLES</span></span>

### <span data-ttu-id="3ce86-108">Örnek 1: uygulama ağ geçidi için yeniden yazma kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="3ce86-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="3ce86-109">Bu komut rule1 adlı bir yeniden yazma kuralı oluşturur ve sonucu $rule adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3ce86-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="3ce86-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ce86-110">PARAMETERS</span></span>

### <span data-ttu-id="3ce86-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="3ce86-111">-ActionSet</span></span>
<span data-ttu-id="3ce86-112">Yeniden yazma kuralının ActionSet</span><span class="sxs-lookup"><span data-stu-id="3ce86-112">ActionSet of the rewrite rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce86-113">-Koşul</span><span class="sxs-lookup"><span data-stu-id="3ce86-113">-Condition</span></span>
<span data-ttu-id="3ce86-114">Yeniden yazma kuralının yürütüleceği koşul</span><span class="sxs-lookup"><span data-stu-id="3ce86-114">Condition for the rewrite rule to execute</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce86-115">-DefaultProfile</span></span>
<span data-ttu-id="3ce86-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ce86-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ce86-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ce86-117">-Name</span></span>
<span data-ttu-id="3ce86-118">Yeniden yazan kuralı</span><span class="sxs-lookup"><span data-stu-id="3ce86-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="3ce86-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="3ce86-119">-RuleSequence</span></span>
<span data-ttu-id="3ce86-120">Yeniden yazma kuralı kümesindeki bu yeniden yazma kuralının kural sıralaması</span><span class="sxs-lookup"><span data-stu-id="3ce86-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="3ce86-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce86-121">CommonParameters</span></span>
<span data-ttu-id="3ce86-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ce86-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce86-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce86-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce86-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ce86-124">INPUTS</span></span>

### <span data-ttu-id="3ce86-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3ce86-125">None</span></span>

## <span data-ttu-id="3ce86-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ce86-126">OUTPUTS</span></span>

### <span data-ttu-id="3ce86-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3ce86-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="3ce86-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ce86-128">NOTES</span></span>

## <span data-ttu-id="3ce86-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ce86-129">RELATED LINKS</span></span>

[<span data-ttu-id="3ce86-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ce86-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3ce86-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ce86-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3ce86-132">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ce86-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3ce86-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ce86-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3ce86-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ce86-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3ce86-135">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3ce86-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="3ce86-136">Yeni-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ce86-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
