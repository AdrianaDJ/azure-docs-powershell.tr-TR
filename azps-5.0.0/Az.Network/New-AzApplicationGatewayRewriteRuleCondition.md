---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278562"
---
# <span data-ttu-id="622a2-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="622a2-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="622a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="622a2-102">SYNOPSIS</span></span>
<span data-ttu-id="622a2-103">Uygulama ağ geçidi için bir koşul ekler.</span><span class="sxs-lookup"><span data-stu-id="622a2-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="622a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="622a2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="622a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="622a2-105">DESCRIPTION</span></span>
<span data-ttu-id="622a2-106">**AzApplicationGatewayRewriteRuleCondition** cmdlet 'ı bir Azure uygulama ağ geçidi için yeniden yazma kuralı koşulunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="622a2-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="622a2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="622a2-107">EXAMPLES</span></span>

### <span data-ttu-id="622a2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="622a2-108">Example 1</span></span>
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
<span data-ttu-id="622a2-109">Bu komut yeniden yazma kuralında bir koşul oluşturur ve sonucu $condition adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="622a2-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="622a2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="622a2-110">PARAMETERS</span></span>

### <span data-ttu-id="622a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622a2-111">-DefaultProfile</span></span>
<span data-ttu-id="622a2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="622a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="622a2-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="622a2-113">-IgnoreCase</span></span>
<span data-ttu-id="622a2-114">Desende büyük/küçük harf işareti</span><span class="sxs-lookup"><span data-stu-id="622a2-114">Set this flag to ignore case on the pattern</span></span>

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

### <span data-ttu-id="622a2-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="622a2-115">-Negate</span></span>
<span data-ttu-id="622a2-116">Koşul doğrulamayı Negate olarak ayarlayın</span><span class="sxs-lookup"><span data-stu-id="622a2-116">Set this flag to negate the condition validation</span></span>

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

### <span data-ttu-id="622a2-117">-Desen</span><span class="sxs-lookup"><span data-stu-id="622a2-117">-Pattern</span></span>
<span data-ttu-id="622a2-118">Değişken üst bilgisinde arama deseni</span><span class="sxs-lookup"><span data-stu-id="622a2-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="622a2-119">Değişkenli</span><span class="sxs-lookup"><span data-stu-id="622a2-119">-Variable</span></span>
<span data-ttu-id="622a2-120">Koşul ayarlanacak üst bilginin adı</span><span class="sxs-lookup"><span data-stu-id="622a2-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="622a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622a2-121">CommonParameters</span></span>
<span data-ttu-id="622a2-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="622a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="622a2-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622a2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622a2-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="622a2-124">INPUTS</span></span>

### <span data-ttu-id="622a2-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="622a2-125">None</span></span>

## <span data-ttu-id="622a2-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="622a2-126">OUTPUTS</span></span>

### <span data-ttu-id="622a2-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="622a2-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="622a2-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="622a2-128">NOTES</span></span>

## <span data-ttu-id="622a2-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="622a2-129">RELATED LINKS</span></span>
[<span data-ttu-id="622a2-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="622a2-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="622a2-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="622a2-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="622a2-132">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="622a2-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="622a2-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="622a2-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="622a2-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="622a2-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="622a2-135">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="622a2-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="622a2-136">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="622a2-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
