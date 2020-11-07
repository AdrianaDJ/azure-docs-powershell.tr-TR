---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 7d6b8ec3e42ce34cc5652893e56fa272ce710c9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931916"
---
# <span data-ttu-id="7472a-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="7472a-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="7472a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7472a-102">SYNOPSIS</span></span>
<span data-ttu-id="7472a-103">Uygulama ağ geçidi için bir koşul ekler.</span><span class="sxs-lookup"><span data-stu-id="7472a-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="7472a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7472a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7472a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7472a-105">DESCRIPTION</span></span>
<span data-ttu-id="7472a-106">**AzApplicationGatewayRewriteRuleCondition** cmdlet 'ı bir Azure uygulama ağ geçidi için yeniden yazma kuralı koşulunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7472a-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="7472a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7472a-107">EXAMPLES</span></span>

### <span data-ttu-id="7472a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7472a-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="7472a-109">Bu komut yeniden yazma kuralında bir koşul oluşturur ve sonucu $condition adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="7472a-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="7472a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7472a-110">PARAMETERS</span></span>

### <span data-ttu-id="7472a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7472a-111">-DefaultProfile</span></span>
<span data-ttu-id="7472a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7472a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7472a-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="7472a-113">-IgnoreCase</span></span>
<span data-ttu-id="7472a-114">Desende büyük/küçük harf işareti</span><span class="sxs-lookup"><span data-stu-id="7472a-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7472a-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="7472a-115">-Negate</span></span>
<span data-ttu-id="7472a-116">Koşul doğrulamayı Negate olarak ayarlayın</span><span class="sxs-lookup"><span data-stu-id="7472a-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7472a-117">-Desen</span><span class="sxs-lookup"><span data-stu-id="7472a-117">-Pattern</span></span>
<span data-ttu-id="7472a-118">Değişken üst bilgisinde arama deseni</span><span class="sxs-lookup"><span data-stu-id="7472a-118">Pattern to look for in the Variable Header</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7472a-119">Değişkenli</span><span class="sxs-lookup"><span data-stu-id="7472a-119">-Variable</span></span>
<span data-ttu-id="7472a-120">Koşul ayarlanacak üst bilginin adı</span><span class="sxs-lookup"><span data-stu-id="7472a-120">Name of the Header to set condition on it</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7472a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7472a-121">CommonParameters</span></span>
<span data-ttu-id="7472a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7472a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7472a-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7472a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7472a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7472a-124">INPUTS</span></span>

### <span data-ttu-id="7472a-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7472a-125">None</span></span>

## <span data-ttu-id="7472a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7472a-126">OUTPUTS</span></span>

### <span data-ttu-id="7472a-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="7472a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="7472a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7472a-128">NOTES</span></span>

## <span data-ttu-id="7472a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7472a-129">RELATED LINKS</span></span>
[<span data-ttu-id="7472a-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7472a-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7472a-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7472a-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7472a-132">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7472a-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7472a-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7472a-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7472a-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7472a-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7472a-135">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7472a-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="7472a-136">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7472a-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
