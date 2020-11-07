---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f13591a92b52e00ed94e93fec480d810037f061d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760388"
---
# <span data-ttu-id="daf9a-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="daf9a-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="daf9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daf9a-102">SYNOPSIS</span></span>
<span data-ttu-id="daf9a-103">Uygulama ağ geçidi için bir yeniden yazma kuralı eylem kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="daf9a-103">Creates a rewrite rule actionset for an application gateway.</span></span>

## <span data-ttu-id="daf9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="daf9a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daf9a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="daf9a-105">DESCRIPTION</span></span>
<span data-ttu-id="daf9a-106">**New-AzApplicationGatewayRewriteRuleActionSet** cmdlet 'ı bir Azure uygulama ağ geçidi için bir yeniden yazma kuralı actionset.</span><span class="sxs-lookup"><span data-stu-id="daf9a-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule actionset for an Azure application gateway.</span></span>

## <span data-ttu-id="daf9a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="daf9a-107">EXAMPLES</span></span>

### <span data-ttu-id="daf9a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="daf9a-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="daf9a-109">Bu komut bir yeniden yazma kuralı eylem kümesi oluşturur ve sonucu $action adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="daf9a-109">This command creates a rewrite rule actionset and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="daf9a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="daf9a-110">PARAMETERS</span></span>

### <span data-ttu-id="daf9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf9a-111">-DefaultProfile</span></span>
<span data-ttu-id="daf9a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="daf9a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daf9a-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="daf9a-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="daf9a-114">İstek üst bilgi yapılandırmalarının listesi</span><span class="sxs-lookup"><span data-stu-id="daf9a-114">List of request header configurations</span></span>

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

### <span data-ttu-id="daf9a-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="daf9a-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="daf9a-116">Yanıt üst bilgi yapılandırmalarının listesi</span><span class="sxs-lookup"><span data-stu-id="daf9a-116">List of response header configurations</span></span>

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

### <span data-ttu-id="daf9a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf9a-117">CommonParameters</span></span>
<span data-ttu-id="daf9a-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="daf9a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf9a-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf9a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf9a-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="daf9a-120">INPUTS</span></span>

### <span data-ttu-id="daf9a-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="daf9a-121">None</span></span>

## <span data-ttu-id="daf9a-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="daf9a-122">OUTPUTS</span></span>

### <span data-ttu-id="daf9a-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="daf9a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="daf9a-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="daf9a-124">NOTES</span></span>

## <span data-ttu-id="daf9a-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="daf9a-125">RELATED LINKS</span></span>

[<span data-ttu-id="daf9a-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daf9a-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="daf9a-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daf9a-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="daf9a-128">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daf9a-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="daf9a-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daf9a-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="daf9a-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daf9a-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="daf9a-131">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="daf9a-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="daf9a-132">Yeni-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="daf9a-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
