---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324691"
---
# <span data-ttu-id="be002-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="be002-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="be002-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be002-102">SYNOPSIS</span></span>
<span data-ttu-id="be002-103">Uygulama ağ geçidi için yeniden yazma kuralı eylem kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be002-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="be002-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be002-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be002-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="be002-105">DESCRIPTION</span></span>
<span data-ttu-id="be002-106">**Yeni-AzApplicationGatewayRewriteRuleActionSet** cmdlet 'ı bir Azure uygulama ağ geçidi için yeniden yazma kuralı eylem kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be002-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="be002-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be002-107">EXAMPLES</span></span>

### <span data-ttu-id="be002-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="be002-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="be002-109">Bu komut yeniden yazma kuralı eylem kümesi oluşturur ve sonucu $action adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="be002-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="be002-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be002-110">PARAMETERS</span></span>

### <span data-ttu-id="be002-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be002-111">-DefaultProfile</span></span>
<span data-ttu-id="be002-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be002-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be002-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="be002-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="be002-114">İstek üst bilgi yapılandırmalarının listesi</span><span class="sxs-lookup"><span data-stu-id="be002-114">List of request header configurations</span></span>

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

### <span data-ttu-id="be002-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="be002-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="be002-116">Yanıt üst bilgi yapılandırmalarının listesi</span><span class="sxs-lookup"><span data-stu-id="be002-116">List of response header configurations</span></span>

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

### <span data-ttu-id="be002-117">-Urlyapılandırma</span><span class="sxs-lookup"><span data-stu-id="be002-117">-UrlConfiguration</span></span>
<span data-ttu-id="be002-118">Eylem kümesi için URL yapılandırması</span><span class="sxs-lookup"><span data-stu-id="be002-118">Url Configuration for action set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be002-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be002-119">CommonParameters</span></span>
<span data-ttu-id="be002-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be002-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be002-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be002-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be002-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be002-122">INPUTS</span></span>

### <span data-ttu-id="be002-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="be002-123">None</span></span>

## <span data-ttu-id="be002-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be002-124">OUTPUTS</span></span>

### <span data-ttu-id="be002-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="be002-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="be002-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be002-126">NOTES</span></span>

## <span data-ttu-id="be002-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be002-127">RELATED LINKS</span></span>

[<span data-ttu-id="be002-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="be002-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="be002-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="be002-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="be002-130">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="be002-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="be002-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="be002-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="be002-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="be002-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="be002-133">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="be002-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="be002-134">Yeni-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="be002-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="be002-135">Yeni-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="be002-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)