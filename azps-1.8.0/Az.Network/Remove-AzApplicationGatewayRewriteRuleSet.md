---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 7d7403fff78d04153f1c088cbdf41f61677e2e7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760200"
---
# <span data-ttu-id="2849b-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2849b-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="2849b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2849b-102">SYNOPSIS</span></span>
<span data-ttu-id="2849b-103">Uygulama ağ geçidinden yeniden yazma kural kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2849b-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="2849b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2849b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2849b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2849b-105">DESCRIPTION</span></span>
<span data-ttu-id="2849b-106">**Remove-AzApplicationGatewayRewriteRuleSet** cmdlet 'ı, Azure uygulama ağ geçidinden yeniden yazma kuralı kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2849b-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="2849b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2849b-107">EXAMPLES</span></span>

### <span data-ttu-id="2849b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2849b-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="2849b-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2849b-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2849b-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden RuleSet02 adlı yeniden yazma kuralı kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2849b-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2849b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2849b-111">PARAMETERS</span></span>

### <span data-ttu-id="2849b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2849b-112">-ApplicationGateway</span></span>
<span data-ttu-id="2849b-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2849b-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2849b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2849b-114">-DefaultProfile</span></span>
<span data-ttu-id="2849b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2849b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2849b-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="2849b-116">-Name</span></span>
<span data-ttu-id="2849b-117">Uygulama ağ geçidi Rewriterset 'in adı</span><span class="sxs-lookup"><span data-stu-id="2849b-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2849b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2849b-118">CommonParameters</span></span>
<span data-ttu-id="2849b-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2849b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2849b-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2849b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2849b-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2849b-121">INPUTS</span></span>

### <span data-ttu-id="2849b-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2849b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2849b-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2849b-123">OUTPUTS</span></span>

### <span data-ttu-id="2849b-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2849b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2849b-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2849b-125">NOTES</span></span>

## <span data-ttu-id="2849b-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2849b-126">RELATED LINKS</span></span>

[<span data-ttu-id="2849b-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2849b-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2849b-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2849b-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2849b-129">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2849b-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2849b-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2849b-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2849b-131">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2849b-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="2849b-132">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2849b-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="2849b-133">Yeni-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2849b-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
