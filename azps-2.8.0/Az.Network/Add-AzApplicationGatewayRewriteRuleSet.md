---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 4b2b8f2694377845af92db5809230a423f83d594
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932111"
---
# <span data-ttu-id="98172-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98172-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="98172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98172-102">SYNOPSIS</span></span>
<span data-ttu-id="98172-103">Uygulama ağ geçidine yeniden yazma kuralı kümesi ekler.</span><span class="sxs-lookup"><span data-stu-id="98172-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="98172-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98172-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98172-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98172-105">DESCRIPTION</span></span>
<span data-ttu-id="98172-106">**Add-AzApplicationGatewayRewriteRuleSet** cmdlet 'i, uygulama ağ geçidine yeniden yazma kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="98172-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="98172-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98172-107">EXAMPLES</span></span>

### <span data-ttu-id="98172-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="98172-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="98172-109">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="98172-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="98172-110">İkinci komut, yeniden yazma kuralı 'nı uygulama ağ geçidine ekler.</span><span class="sxs-lookup"><span data-stu-id="98172-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="98172-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98172-111">PARAMETERS</span></span>

### <span data-ttu-id="98172-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98172-112">-ApplicationGateway</span></span>
<span data-ttu-id="98172-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98172-113">The applicationGateway</span></span>

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

### <span data-ttu-id="98172-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98172-114">-DefaultProfile</span></span>
<span data-ttu-id="98172-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98172-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98172-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="98172-116">-Name</span></span>
<span data-ttu-id="98172-117">RewriteRuleSet 'in adı</span><span class="sxs-lookup"><span data-stu-id="98172-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="98172-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="98172-118">-RewriteRule</span></span>
<span data-ttu-id="98172-119">Yeniden yazma kuralları listesi</span><span class="sxs-lookup"><span data-stu-id="98172-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="98172-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98172-120">CommonParameters</span></span>
<span data-ttu-id="98172-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98172-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98172-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98172-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98172-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98172-123">INPUTS</span></span>

### <span data-ttu-id="98172-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98172-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="98172-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98172-125">OUTPUTS</span></span>

### <span data-ttu-id="98172-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98172-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="98172-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98172-127">NOTES</span></span>

## <span data-ttu-id="98172-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98172-128">RELATED LINKS</span></span>

[<span data-ttu-id="98172-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98172-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98172-130">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98172-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98172-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98172-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98172-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98172-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="98172-133">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="98172-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="98172-134">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="98172-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="98172-135">Yeni-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="98172-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
