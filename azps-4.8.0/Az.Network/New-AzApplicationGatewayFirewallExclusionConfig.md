---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 370965325a265ef4c2b7fa5e0070ae705099e2c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109479"
---
# <span data-ttu-id="70696-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="70696-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="70696-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70696-102">SYNOPSIS</span></span>
<span data-ttu-id="70696-103">Uygulama ağ geçidi için yeni bir dışlama kuralı listesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="70696-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="70696-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70696-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70696-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70696-105">DESCRIPTION</span></span>
<span data-ttu-id="70696-106">**New-Azapplicationgatewayfirewallexclusıonconfig** cmdlet 'i, Application Gateway WAF için yeni bir dışlama kuralı listesi.</span><span class="sxs-lookup"><span data-stu-id="70696-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="70696-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70696-107">EXAMPLES</span></span>

### <span data-ttu-id="70696-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="70696-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="70696-109">Bu komut, Ertheadernames ve WITH xyz adlı ad ve işleç adındaki işleç adlı değişken için yeni bir dışlama kuralı listesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70696-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="70696-110">Dışlama listesi yapılandırması $exclusion 1 ' de kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="70696-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="70696-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70696-111">PARAMETERS</span></span>

### <span data-ttu-id="70696-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70696-112">-DefaultProfile</span></span>
<span data-ttu-id="70696-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70696-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70696-114">-İşleç</span><span class="sxs-lookup"><span data-stu-id="70696-114">-Operator</span></span>
<span data-ttu-id="70696-115">Değişken bir koleksiyon olduğunda, bu dışlama koleksiyonundaki hangi öğelerin uygulanacağını belirtmek için seçici üzerinde işlem yapın.</span><span class="sxs-lookup"><span data-stu-id="70696-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="70696-116">-Seçici</span><span class="sxs-lookup"><span data-stu-id="70696-116">-Selector</span></span>
<span data-ttu-id="70696-117">Değişken bir koleksiyon olduğunda, bu dışlama koleksiyonundaki hangi öğelerin uygulanacağını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="70696-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="70696-118">Değişkenli</span><span class="sxs-lookup"><span data-stu-id="70696-118">-Variable</span></span>
<span data-ttu-id="70696-119">Dışlanacak değişken.</span><span class="sxs-lookup"><span data-stu-id="70696-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="70696-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70696-120">CommonParameters</span></span>
<span data-ttu-id="70696-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70696-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70696-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70696-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70696-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70696-123">INPUTS</span></span>

### <span data-ttu-id="70696-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="70696-124">None</span></span>

## <span data-ttu-id="70696-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70696-125">OUTPUTS</span></span>

### <span data-ttu-id="70696-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="70696-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="70696-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70696-127">NOTES</span></span>

## <span data-ttu-id="70696-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70696-128">RELATED LINKS</span></span>
