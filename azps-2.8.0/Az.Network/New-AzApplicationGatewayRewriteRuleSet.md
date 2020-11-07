---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 1ed5c90d4c53769d53cd645b2e5bced7bdec4ce8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931911"
---
# <span data-ttu-id="d8826-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8826-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="d8826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8826-102">SYNOPSIS</span></span>
<span data-ttu-id="d8826-103">Uygulama ağ geçidi için bir istek yönlendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8826-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="d8826-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8826-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8826-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8826-105">DESCRIPTION</span></span>
<span data-ttu-id="d8826-106">**Yeni-AzApplicationGatewayRewriteRuleSet** cmdlet 'i, bir Azure Application Gateway için yeniden yazma kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8826-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="d8826-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8826-107">EXAMPLES</span></span>

### <span data-ttu-id="d8826-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d8826-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="d8826-109">Bu komut ruleset1 adlı bir yeniden yazma kuralı kümesi oluşturur ve sonucu $ruleset adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="d8826-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="d8826-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8826-110">PARAMETERS</span></span>

### <span data-ttu-id="d8826-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8826-111">-DefaultProfile</span></span>
<span data-ttu-id="d8826-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8826-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8826-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8826-113">-Name</span></span>
<span data-ttu-id="d8826-114">RewriteRuleSet 'in adı</span><span class="sxs-lookup"><span data-stu-id="d8826-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="d8826-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="d8826-115">-RewriteRule</span></span>
<span data-ttu-id="d8826-116">Yeniden yazma kuralları listesi</span><span class="sxs-lookup"><span data-stu-id="d8826-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="d8826-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8826-117">CommonParameters</span></span>
<span data-ttu-id="d8826-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8826-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8826-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8826-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8826-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8826-120">INPUTS</span></span>

### <span data-ttu-id="d8826-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d8826-121">None</span></span>

## <span data-ttu-id="d8826-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8826-122">OUTPUTS</span></span>

### <span data-ttu-id="d8826-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8826-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="d8826-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8826-124">NOTES</span></span>

## <span data-ttu-id="d8826-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8826-125">RELATED LINKS</span></span>

[<span data-ttu-id="d8826-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8826-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d8826-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8826-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d8826-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8826-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d8826-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8826-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d8826-130">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d8826-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d8826-131">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d8826-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="d8826-132">Yeni-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8826-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)