---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 3587005559849072d973242eb6af221c0b8b0557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917944"
---
# <span data-ttu-id="fe7bb-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe7bb-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="fe7bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="fe7bb-103">Uygulama ağ geçidi için ayarlanmış yeniden yazma kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fe7bb-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="fe7bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe7bb-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe7bb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe7bb-105">DESCRIPTION</span></span>
<span data-ttu-id="fe7bb-106">**Set-AzApplicationGatewayRewriteRuleSet** cmdlet 'i, istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fe7bb-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="fe7bb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe7bb-107">EXAMPLES</span></span>

### <span data-ttu-id="fe7bb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fe7bb-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="fe7bb-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fe7bb-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fe7bb-110">İkinci komut, uygulama ağ geçidi 'nin yeniden yazma kuralını, $rule değişkeninde belirtilen yeniden yazma kurallarını kullanacak şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fe7bb-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="fe7bb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe7bb-111">PARAMETERS</span></span>

### <span data-ttu-id="fe7bb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe7bb-112">-ApplicationGateway</span></span>
<span data-ttu-id="fe7bb-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe7bb-113">The applicationGateway</span></span>

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

### <span data-ttu-id="fe7bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe7bb-114">-DefaultProfile</span></span>
<span data-ttu-id="fe7bb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fe7bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe7bb-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="fe7bb-116">-Name</span></span>
<span data-ttu-id="fe7bb-117">RewriteRuleSet 'in adı</span><span class="sxs-lookup"><span data-stu-id="fe7bb-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="fe7bb-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="fe7bb-118">-RewriteRule</span></span>
<span data-ttu-id="fe7bb-119">Yeniden yazma kuralları listesi</span><span class="sxs-lookup"><span data-stu-id="fe7bb-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="fe7bb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe7bb-120">CommonParameters</span></span>
<span data-ttu-id="fe7bb-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe7bb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe7bb-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe7bb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe7bb-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe7bb-123">INPUTS</span></span>

### <span data-ttu-id="fe7bb-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe7bb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe7bb-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe7bb-125">OUTPUTS</span></span>

### <span data-ttu-id="fe7bb-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe7bb-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe7bb-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe7bb-127">NOTES</span></span>

## <span data-ttu-id="fe7bb-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe7bb-128">RELATED LINKS</span></span>

[<span data-ttu-id="fe7bb-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe7bb-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fe7bb-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe7bb-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fe7bb-131">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe7bb-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fe7bb-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe7bb-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="fe7bb-133">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="fe7bb-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="fe7bb-134">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="fe7bb-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="fe7bb-135">Yeni-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe7bb-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
