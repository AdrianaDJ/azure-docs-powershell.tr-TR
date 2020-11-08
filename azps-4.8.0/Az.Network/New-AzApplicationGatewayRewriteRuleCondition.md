---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108915"
---
# <span data-ttu-id="054fa-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="054fa-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="054fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="054fa-102">SYNOPSIS</span></span>
<span data-ttu-id="054fa-103">Uygulama ağ geçidi için bir koşul ekler.</span><span class="sxs-lookup"><span data-stu-id="054fa-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="054fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="054fa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="054fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="054fa-105">DESCRIPTION</span></span>
<span data-ttu-id="054fa-106">**AzApplicationGatewayRewriteRuleCondition** cmdlet 'ı bir Azure uygulama ağ geçidi için yeniden yazma kuralı koşulunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="054fa-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="054fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="054fa-107">EXAMPLES</span></span>

### <span data-ttu-id="054fa-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="054fa-108">Example 1</span></span>
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
<span data-ttu-id="054fa-109">Bu komut yeniden yazma kuralında bir koşul oluşturur ve sonucu $condition adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="054fa-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="054fa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="054fa-110">PARAMETERS</span></span>

### <span data-ttu-id="054fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="054fa-111">-DefaultProfile</span></span>
<span data-ttu-id="054fa-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="054fa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="054fa-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="054fa-113">-IgnoreCase</span></span>
<span data-ttu-id="054fa-114">Desende büyük/küçük harf işareti</span><span class="sxs-lookup"><span data-stu-id="054fa-114">Set this flag to ignore case on the pattern</span></span>

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

### <span data-ttu-id="054fa-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="054fa-115">-Negate</span></span>
<span data-ttu-id="054fa-116">Koşul doğrulamayı Negate olarak ayarlayın</span><span class="sxs-lookup"><span data-stu-id="054fa-116">Set this flag to negate the condition validation</span></span>

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

### <span data-ttu-id="054fa-117">-Desen</span><span class="sxs-lookup"><span data-stu-id="054fa-117">-Pattern</span></span>
<span data-ttu-id="054fa-118">Değişken üst bilgisinde arama deseni</span><span class="sxs-lookup"><span data-stu-id="054fa-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="054fa-119">Değişkenli</span><span class="sxs-lookup"><span data-stu-id="054fa-119">-Variable</span></span>
<span data-ttu-id="054fa-120">Koşul ayarlanacak üst bilginin adı</span><span class="sxs-lookup"><span data-stu-id="054fa-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="054fa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="054fa-121">CommonParameters</span></span>
<span data-ttu-id="054fa-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="054fa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="054fa-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="054fa-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="054fa-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="054fa-124">INPUTS</span></span>

### <span data-ttu-id="054fa-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="054fa-125">None</span></span>

## <span data-ttu-id="054fa-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="054fa-126">OUTPUTS</span></span>

### <span data-ttu-id="054fa-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="054fa-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="054fa-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="054fa-128">NOTES</span></span>

## <span data-ttu-id="054fa-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="054fa-129">RELATED LINKS</span></span>
[<span data-ttu-id="054fa-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="054fa-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="054fa-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="054fa-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="054fa-132">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="054fa-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="054fa-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="054fa-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="054fa-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="054fa-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="054fa-135">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="054fa-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="054fa-136">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="054fa-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
