---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 84be6aa60ede19e88b98ca9517fa3cbce3872c8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931919"
---
# <span data-ttu-id="76b7e-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="76b7e-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="76b7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="76b7e-103">Uygulama ağ geçidi için yeniden yazma kuralı eylem kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76b7e-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="76b7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76b7e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76b7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76b7e-105">DESCRIPTION</span></span>
<span data-ttu-id="76b7e-106">**Yeni-AzApplicationGatewayRewriteRuleActionSet** cmdlet 'ı bir Azure uygulama ağ geçidi için yeniden yazma kuralı eylem kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76b7e-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="76b7e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76b7e-107">EXAMPLES</span></span>

### <span data-ttu-id="76b7e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76b7e-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="76b7e-109">Bu komut yeniden yazma kuralı eylem kümesi oluşturur ve sonucu $action adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="76b7e-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="76b7e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76b7e-110">PARAMETERS</span></span>

### <span data-ttu-id="76b7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b7e-111">-DefaultProfile</span></span>
<span data-ttu-id="76b7e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76b7e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76b7e-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="76b7e-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="76b7e-114">İstek üst bilgi yapılandırmalarının listesi</span><span class="sxs-lookup"><span data-stu-id="76b7e-114">List of request header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b7e-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="76b7e-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="76b7e-116">Yanıt üst bilgi yapılandırmalarının listesi</span><span class="sxs-lookup"><span data-stu-id="76b7e-116">List of response header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b7e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b7e-117">CommonParameters</span></span>
<span data-ttu-id="76b7e-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76b7e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b7e-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76b7e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b7e-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76b7e-120">INPUTS</span></span>

### <span data-ttu-id="76b7e-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="76b7e-121">None</span></span>

## <span data-ttu-id="76b7e-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76b7e-122">OUTPUTS</span></span>

### <span data-ttu-id="76b7e-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="76b7e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="76b7e-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76b7e-124">NOTES</span></span>

## <span data-ttu-id="76b7e-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76b7e-125">RELATED LINKS</span></span>

[<span data-ttu-id="76b7e-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76b7e-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="76b7e-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76b7e-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="76b7e-128">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76b7e-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="76b7e-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76b7e-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="76b7e-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76b7e-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="76b7e-131">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="76b7e-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="76b7e-132">Yeni-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="76b7e-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
