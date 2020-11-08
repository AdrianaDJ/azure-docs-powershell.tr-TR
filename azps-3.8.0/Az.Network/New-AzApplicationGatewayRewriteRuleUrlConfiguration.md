---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104772"
---
# <span data-ttu-id="026fe-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="026fe-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="026fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="026fe-102">SYNOPSIS</span></span>
<span data-ttu-id="026fe-103">Uygulama ağ geçidi için yeniden yazma kuralı URL yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="026fe-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="026fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="026fe-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="026fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="026fe-105">DESCRIPTION</span></span>
<span data-ttu-id="026fe-106">**AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet 'ı bir Azure uygulama ağ geçidi için yeniden yazma kuralı URL yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="026fe-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="026fe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="026fe-107">EXAMPLES</span></span>

### <span data-ttu-id="026fe-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="026fe-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="026fe-109">Bu komut yeniden yazma kuralı URL yapılandırması oluşturur ve sonucu $urlConfiguration adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="026fe-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="026fe-110">Var olan herhangi bir URL yapılandırmasını güncelleştirmek istiyorsanız, bunu yeni bir Urlyapılandırması oluşturarak ve yeni Urlyapılandırmasını yeniden yazma kuralı eylem kümesinin UrlConfiguration özelliğine atayarak yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="026fe-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="026fe-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="026fe-111">PARAMETERS</span></span>

### <span data-ttu-id="026fe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="026fe-112">-DefaultProfile</span></span>
<span data-ttu-id="026fe-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="026fe-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="026fe-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="026fe-114">-ModifiedPath</span></span>
<span data-ttu-id="026fe-115">URL yol değeri.</span><span class="sxs-lookup"><span data-stu-id="026fe-115">Url path value.</span></span>

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

### <span data-ttu-id="026fe-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="026fe-116">-ModifiedQueryString</span></span>
<span data-ttu-id="026fe-117">URL sorgu dizesi değeri.</span><span class="sxs-lookup"><span data-stu-id="026fe-117">Url query string value.</span></span>

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

### <span data-ttu-id="026fe-118">-Yeniden yönlendir</span><span class="sxs-lookup"><span data-stu-id="026fe-118">-Reroute</span></span>
<span data-ttu-id="026fe-119">Yol tabanlı istek yönlendirme kurallarında sağlanan URL yol eşlemesini değiştirilmiş yol kullanılarak yeniden değerlendirmek için bayrak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="026fe-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="026fe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="026fe-120">CommonParameters</span></span>
<span data-ttu-id="026fe-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="026fe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="026fe-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="026fe-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="026fe-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="026fe-123">INPUTS</span></span>

### <span data-ttu-id="026fe-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="026fe-124">None</span></span>

## <span data-ttu-id="026fe-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="026fe-125">OUTPUTS</span></span>

### <span data-ttu-id="026fe-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="026fe-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="026fe-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="026fe-127">NOTES</span></span>

## <span data-ttu-id="026fe-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="026fe-128">RELATED LINKS</span></span>

[<span data-ttu-id="026fe-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="026fe-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="026fe-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="026fe-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="026fe-131">Yeni-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="026fe-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="026fe-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="026fe-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="026fe-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="026fe-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="026fe-134">Yeni-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="026fe-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="026fe-135">Yeni-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="026fe-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)