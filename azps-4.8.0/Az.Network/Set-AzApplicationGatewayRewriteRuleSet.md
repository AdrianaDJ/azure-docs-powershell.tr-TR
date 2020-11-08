---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 45d7fdf6a276e98ce0aca2c2a0db6989e062e42c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108844"
---
# <span data-ttu-id="0fe75-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0fe75-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="0fe75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fe75-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe75-103">Uygulama ağ geçidi için ayarlanmış yeniden yazma kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0fe75-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="0fe75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0fe75-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fe75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0fe75-105">DESCRIPTION</span></span>
<span data-ttu-id="0fe75-106">**Set-AzApplicationGatewayRewriteRuleSet** cmdlet 'i, istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0fe75-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="0fe75-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0fe75-107">EXAMPLES</span></span>

### <span data-ttu-id="0fe75-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0fe75-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="0fe75-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0fe75-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0fe75-110">İkinci komut, uygulama ağ geçidi 'nin yeniden yazma kuralını, $rule değişkeninde belirtilen yeniden yazma kurallarını kullanacak şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0fe75-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="0fe75-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0fe75-111">PARAMETERS</span></span>

### <span data-ttu-id="0fe75-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fe75-112">-ApplicationGateway</span></span>
<span data-ttu-id="0fe75-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fe75-113">The applicationGateway</span></span>

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

### <span data-ttu-id="0fe75-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe75-114">-DefaultProfile</span></span>
<span data-ttu-id="0fe75-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0fe75-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe75-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0fe75-116">-Name</span></span>
<span data-ttu-id="0fe75-117">RewriteRuleSet 'in adı</span><span class="sxs-lookup"><span data-stu-id="0fe75-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="0fe75-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="0fe75-118">-RewriteRule</span></span>
<span data-ttu-id="0fe75-119">Yeniden yazma kuralları listesi</span><span class="sxs-lookup"><span data-stu-id="0fe75-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="0fe75-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe75-120">CommonParameters</span></span>
<span data-ttu-id="0fe75-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0fe75-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe75-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fe75-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe75-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0fe75-123">INPUTS</span></span>

### <span data-ttu-id="0fe75-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fe75-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0fe75-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0fe75-125">OUTPUTS</span></span>

### <span data-ttu-id="0fe75-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fe75-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0fe75-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0fe75-127">NOTES</span></span>

## <span data-ttu-id="0fe75-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0fe75-128">RELATED LINKS</span></span>

[<span data-ttu-id="0fe75-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0fe75-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0fe75-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0fe75-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0fe75-131">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0fe75-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0fe75-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0fe75-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0fe75-133">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0fe75-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="0fe75-134">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0fe75-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="0fe75-135">Yeni-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fe75-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
