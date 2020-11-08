---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: dc3019154d4041396d46f3c9f6dbdbdd3deb22a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937821"
---
# <span data-ttu-id="3e015-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3e015-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="3e015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e015-102">SYNOPSIS</span></span>
<span data-ttu-id="3e015-103">Uygulama ağ geçidi yeniden yazma kuralı kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="3e015-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="3e015-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e015-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e015-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e015-105">DESCRIPTION</span></span>
<span data-ttu-id="3e015-106">Uygulama ağ geçidi yeniden yazma kuralı kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="3e015-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="3e015-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e015-107">EXAMPLES</span></span>

### <span data-ttu-id="3e015-108">Örnek 1: belirli bir yeniden yazma kuralı kümesi alma</span><span class="sxs-lookup"><span data-stu-id="3e015-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="3e015-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3e015-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="3e015-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden RuleSet01 adlı yeniden yazma kuralı kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="3e015-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="3e015-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e015-111">PARAMETERS</span></span>

### <span data-ttu-id="3e015-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e015-112">-ApplicationGateway</span></span>
<span data-ttu-id="3e015-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e015-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e015-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e015-114">-DefaultProfile</span></span>
<span data-ttu-id="3e015-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e015-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e015-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e015-116">-Name</span></span>
<span data-ttu-id="3e015-117">Uygulama ağ geçidi Rewriterset 'in adı</span><span class="sxs-lookup"><span data-stu-id="3e015-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="3e015-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e015-118">CommonParameters</span></span>
<span data-ttu-id="3e015-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e015-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e015-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3e015-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e015-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e015-121">INPUTS</span></span>

### <span data-ttu-id="3e015-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e015-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e015-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e015-123">OUTPUTS</span></span>

### <span data-ttu-id="3e015-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3e015-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="3e015-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e015-125">NOTES</span></span>

## <span data-ttu-id="3e015-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e015-126">RELATED LINKS</span></span>

[<span data-ttu-id="3e015-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3e015-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3e015-128">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3e015-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3e015-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3e015-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3e015-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3e015-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3e015-131">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3e015-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="3e015-132">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3e015-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="3e015-133">Yeni-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e015-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)