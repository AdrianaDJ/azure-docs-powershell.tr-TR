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
ms.locfileid: "93760415"
---
# <span data-ttu-id="56e8e-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="56e8e-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="56e8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="56e8e-103">Uygulama ağ geçidi için yeni bir dışlama kuralı listesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="56e8e-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="56e8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56e8e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56e8e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="56e8e-105">DESCRIPTION</span></span>
<span data-ttu-id="56e8e-106">**New-Azapplicationgatewayfirewallexclusıonconfig** cmdlet 'i, Application Gateway WAF için yeni bir dışlama kuralı listesi.</span><span class="sxs-lookup"><span data-stu-id="56e8e-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="56e8e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56e8e-107">EXAMPLES</span></span>

### <span data-ttu-id="56e8e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="56e8e-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="56e8e-109">Bu komut, Ertheadernames ve WITH xyz adlı ad ve işleç adındaki işleç adlı değişken için yeni bir dışlama kuralı listesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="56e8e-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="56e8e-110">Dışlama listesi yapılandırması $exclusion 1 ' de kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="56e8e-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="56e8e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56e8e-111">PARAMETERS</span></span>

### <span data-ttu-id="56e8e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e8e-112">-DefaultProfile</span></span>
<span data-ttu-id="56e8e-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56e8e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56e8e-114">-İşleç</span><span class="sxs-lookup"><span data-stu-id="56e8e-114">-Operator</span></span>
<span data-ttu-id="56e8e-115">Değişken bir koleksiyon olduğunda, bu dışlama koleksiyonundaki hangi öğelerin uygulanacağını belirtmek için seçici üzerinde işlem yapın.</span><span class="sxs-lookup"><span data-stu-id="56e8e-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="56e8e-116">-Seçici</span><span class="sxs-lookup"><span data-stu-id="56e8e-116">-Selector</span></span>
<span data-ttu-id="56e8e-117">Değişken bir koleksiyon olduğunda, bu dışlama koleksiyonundaki hangi öğelerin uygulanacağını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="56e8e-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="56e8e-118">Değişkenli</span><span class="sxs-lookup"><span data-stu-id="56e8e-118">-Variable</span></span>
<span data-ttu-id="56e8e-119">Dışlanacak değişken.</span><span class="sxs-lookup"><span data-stu-id="56e8e-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="56e8e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e8e-120">CommonParameters</span></span>
<span data-ttu-id="56e8e-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56e8e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e8e-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e8e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e8e-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56e8e-123">INPUTS</span></span>

### <span data-ttu-id="56e8e-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="56e8e-124">None</span></span>

## <span data-ttu-id="56e8e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56e8e-125">OUTPUTS</span></span>

### <span data-ttu-id="56e8e-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="56e8e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="56e8e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56e8e-127">NOTES</span></span>

## <span data-ttu-id="56e8e-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56e8e-128">RELATED LINKS</span></span>
