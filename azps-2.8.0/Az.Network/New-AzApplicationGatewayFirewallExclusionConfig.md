---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 58060c488e778510822d9bc86a21de216447e0f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931936"
---
# <span data-ttu-id="b6619-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="b6619-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="b6619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6619-102">SYNOPSIS</span></span>
<span data-ttu-id="b6619-103">Uygulama ağ geçidi için yeni bir dışlama kuralı listesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="b6619-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="b6619-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6619-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6619-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6619-105">DESCRIPTION</span></span>
<span data-ttu-id="b6619-106">**New-Azapplicationgatewayfirewallexclusıonconfig** cmdlet 'i, Application Gateway WAF için yeni bir dışlama kuralı listesi.</span><span class="sxs-lookup"><span data-stu-id="b6619-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="b6619-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6619-107">EXAMPLES</span></span>

### <span data-ttu-id="b6619-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b6619-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="b6619-109">Bu komut, Ertheadernames ve WITH xyz adlı ad ve işleç adındaki işleç adlı değişken için yeni bir dışlama kuralı listesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b6619-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="b6619-110">Dışlama listesi yapılandırması $exclusion 1 ' de kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="b6619-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="b6619-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6619-111">PARAMETERS</span></span>

### <span data-ttu-id="b6619-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6619-112">-DefaultProfile</span></span>
<span data-ttu-id="b6619-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6619-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6619-114">-İşleç</span><span class="sxs-lookup"><span data-stu-id="b6619-114">-Operator</span></span>
<span data-ttu-id="b6619-115">Değişken bir koleksiyon olduğunda, bu dışlama koleksiyonundaki hangi öğelerin uygulanacağını belirtmek için seçici üzerinde işlem yapın.</span><span class="sxs-lookup"><span data-stu-id="b6619-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="b6619-116">-Seçici</span><span class="sxs-lookup"><span data-stu-id="b6619-116">-Selector</span></span>
<span data-ttu-id="b6619-117">Değişken bir koleksiyon olduğunda, bu dışlama koleksiyonundaki hangi öğelerin uygulanacağını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b6619-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="b6619-118">Değişkenli</span><span class="sxs-lookup"><span data-stu-id="b6619-118">-Variable</span></span>
<span data-ttu-id="b6619-119">Dışlanacak değişken.</span><span class="sxs-lookup"><span data-stu-id="b6619-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="b6619-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6619-120">CommonParameters</span></span>
<span data-ttu-id="b6619-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6619-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6619-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6619-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6619-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6619-123">INPUTS</span></span>

### <span data-ttu-id="b6619-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b6619-124">None</span></span>

## <span data-ttu-id="b6619-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6619-125">OUTPUTS</span></span>

### <span data-ttu-id="b6619-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="b6619-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="b6619-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6619-127">NOTES</span></span>

## <span data-ttu-id="b6619-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6619-128">RELATED LINKS</span></span>
