---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104774"
---
# <span data-ttu-id="bd681-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd681-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="bd681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd681-102">SYNOPSIS</span></span>
<span data-ttu-id="bd681-103">Uygulama ağ geçidi için bir istek yönlendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bd681-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="bd681-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd681-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd681-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd681-105">DESCRIPTION</span></span>
<span data-ttu-id="bd681-106">**Yeni-AzApplicationGatewayRewriteRuleSet** cmdlet 'i, bir Azure Application Gateway için yeniden yazma kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bd681-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="bd681-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd681-107">EXAMPLES</span></span>

### <span data-ttu-id="bd681-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bd681-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="bd681-109">Bu komut ruleset1 adlı bir yeniden yazma kuralı kümesi oluşturur ve sonucu $ruleset adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="bd681-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="bd681-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd681-110">PARAMETERS</span></span>

### <span data-ttu-id="bd681-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd681-111">-DefaultProfile</span></span>
<span data-ttu-id="bd681-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd681-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd681-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="bd681-113">-Name</span></span>
<span data-ttu-id="bd681-114">RewriteRuleSet 'in adı</span><span class="sxs-lookup"><span data-stu-id="bd681-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="bd681-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="bd681-115">-RewriteRule</span></span>
<span data-ttu-id="bd681-116">Yeniden yazma kuralları listesi</span><span class="sxs-lookup"><span data-stu-id="bd681-116">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd681-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd681-117">CommonParameters</span></span>
<span data-ttu-id="bd681-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd681-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd681-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd681-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd681-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd681-120">INPUTS</span></span>

### <span data-ttu-id="bd681-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bd681-121">None</span></span>

## <span data-ttu-id="bd681-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd681-122">OUTPUTS</span></span>

### <span data-ttu-id="bd681-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd681-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="bd681-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd681-124">NOTES</span></span>

## <span data-ttu-id="bd681-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd681-125">RELATED LINKS</span></span>

[<span data-ttu-id="bd681-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd681-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd681-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd681-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd681-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd681-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd681-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd681-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd681-130">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="bd681-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="bd681-131">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="bd681-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="bd681-132">Yeni-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd681-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
