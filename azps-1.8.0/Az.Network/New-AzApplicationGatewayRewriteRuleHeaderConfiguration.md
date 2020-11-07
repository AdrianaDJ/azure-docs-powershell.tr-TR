---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ad14e461647fce3ec9471106b8bb69d4002eb590
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760384"
---
# <span data-ttu-id="70c6e-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="70c6e-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="70c6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="70c6e-103">Uygulama ağ geçidi için yeniden yazma kuralı üstbilgisi yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70c6e-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="70c6e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70c6e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70c6e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70c6e-105">DESCRIPTION</span></span>
<span data-ttu-id="70c6e-106">**AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet 'ı bir Azure uygulama ağ geçidi için bir yeniden yazma kuralı eylem kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70c6e-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule actionset for an Azure application gateway.</span></span>

## <span data-ttu-id="70c6e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70c6e-107">EXAMPLES</span></span>

### <span data-ttu-id="70c6e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="70c6e-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="70c6e-109">Bu komut, yeniden yazma kuralı üst bilgisi yapılandırması oluşturur ve sonucu $hc değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="70c6e-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="70c6e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70c6e-110">PARAMETERS</span></span>

### <span data-ttu-id="70c6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c6e-111">-DefaultProfile</span></span>
<span data-ttu-id="70c6e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70c6e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70c6e-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="70c6e-113">-HeaderName</span></span>
<span data-ttu-id="70c6e-114">Yeniden yazma başlığı adı</span><span class="sxs-lookup"><span data-stu-id="70c6e-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="70c6e-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="70c6e-115">-HeaderValue</span></span>
<span data-ttu-id="70c6e-116">Belirtilen başlık adı için kümenin başlık değeri.</span><span class="sxs-lookup"><span data-stu-id="70c6e-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="70c6e-117">Bu atlanırsa üstbilgi silinir</span><span class="sxs-lookup"><span data-stu-id="70c6e-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="70c6e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c6e-118">CommonParameters</span></span>
<span data-ttu-id="70c6e-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70c6e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c6e-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70c6e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c6e-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70c6e-121">INPUTS</span></span>

### <span data-ttu-id="70c6e-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="70c6e-122">None</span></span>

## <span data-ttu-id="70c6e-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70c6e-123">OUTPUTS</span></span>

### <span data-ttu-id="70c6e-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="70c6e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="70c6e-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70c6e-125">NOTES</span></span>

## <span data-ttu-id="70c6e-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70c6e-126">RELATED LINKS</span></span>

[<span data-ttu-id="70c6e-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70c6e-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="70c6e-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70c6e-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="70c6e-129">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70c6e-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="70c6e-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70c6e-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="70c6e-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70c6e-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="70c6e-132">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="70c6e-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="70c6e-133">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="70c6e-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)