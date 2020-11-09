---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325816"
---
# <span data-ttu-id="18382-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18382-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="18382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18382-102">SYNOPSIS</span></span>
<span data-ttu-id="18382-103">Uygulama ağ geçidinden yeniden yazma kural kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18382-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="18382-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18382-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18382-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18382-105">DESCRIPTION</span></span>
<span data-ttu-id="18382-106">**Remove-AzApplicationGatewayRewriteRuleSet** cmdlet 'ı, Azure uygulama ağ geçidinden yeniden yazma kuralı kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18382-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="18382-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18382-107">EXAMPLES</span></span>

### <span data-ttu-id="18382-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="18382-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="18382-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="18382-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="18382-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden RuleSet02 adlı yeniden yazma kuralı kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18382-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="18382-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18382-111">PARAMETERS</span></span>

### <span data-ttu-id="18382-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18382-112">-ApplicationGateway</span></span>
<span data-ttu-id="18382-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18382-113">The applicationGateway</span></span>

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

### <span data-ttu-id="18382-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18382-114">-DefaultProfile</span></span>
<span data-ttu-id="18382-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18382-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18382-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="18382-116">-Name</span></span>
<span data-ttu-id="18382-117">Uygulama ağ geçidi Rewriterset 'in adı</span><span class="sxs-lookup"><span data-stu-id="18382-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="18382-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18382-118">CommonParameters</span></span>
<span data-ttu-id="18382-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18382-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18382-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18382-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18382-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18382-121">INPUTS</span></span>

### <span data-ttu-id="18382-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18382-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="18382-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18382-123">OUTPUTS</span></span>

### <span data-ttu-id="18382-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18382-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="18382-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18382-125">NOTES</span></span>

## <span data-ttu-id="18382-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18382-126">RELATED LINKS</span></span>

[<span data-ttu-id="18382-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18382-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="18382-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18382-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="18382-129">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18382-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="18382-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="18382-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="18382-131">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="18382-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="18382-132">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="18382-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="18382-133">Yeni-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="18382-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
